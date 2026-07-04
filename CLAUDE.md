# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A personal site (Sriram Sankar's academic/portfolio/blog site, sriramsankar.in) built with **Hugo** and deployed on **Netlify**. There is no `.git` directory and no `package.json` in this checkout — it's a pure Hugo project with no Node/npm build step.

**Migration in progress:** the goal is to refactor this from Hugo to Jekyll so it can be deployed directly via GitHub Pages (no Netlify). Keep that target in mind — e.g. Jekyll's `_config.yml`, `_layouts`/`_includes`, and `_posts`/collections will replace the Hugo equivalents described below, and anything Netlify-specific (Identity widget, Netlify Forms, `netlify.toml`, the git-gateway CMS backend) will need a GitHub Pages-compatible replacement or removal.

## Commands

- Build: `hugo` (this is the exact command Netlify runs — see `netlify.toml`). Output goes to `public/`.
- Local dev server with drafts: `hugo server -D`
- Netlify pins `HUGO_VERSION = "0.81.0"` in `netlify.toml` — match this version locally to avoid template/function incompatibilities (Hugo isn't installed in this environment; install it separately to build/preview).
- No test suite, linter, or CI config exists in this repo.

## Architecture

**Two-file site config split:**
- `config.yaml` — Hugo build config: baseURL, taxonomies, markup (unsafe HTML in goldmark enabled), permalinks, related-content weights, sitemap settings.
- `data/config.json` — site *content* config, exposed in templates as `.Site.Data.config`: site title, color `palette` name, header nav links, social links, footer text, and `domain`. Nav/social links are data-driven lists rendered by `layouts/partials/navigation.html`.

**Layout selection is front-matter-driven, not type-driven.** There's no `archetypes` or Hugo "type" convention in use — every content page sets a `layout:` field in front matter (e.g. `layout: post`, `layout: blog`, `layout: projects`, `layout: contact`, `layout: page`), which Hugo resolves against `layouts/_default/*.html`. When porting to Jekyll, this maps naturally to Jekyll's own `layout:` front matter key, but the actual template logic inside each `.html` file will need to be rewritten from Go templates to Liquid.

**Content sections and their listing pattern:**
- `content/thoughts/` (poems/blog posts) and `content/sideprojects/` (project write-ups) are the two real content collections. Their index pages (`_index.md`) use `layout: blog` / `layout: projects`, and individual entries use `layout: post`.
- `layouts/_default/blog.html` and `projects.html` fetch their entries by hand via `(.Site.GetPage "section" "/thoughts").Pages` / `"/sideprojects"` rather than using Hugo's normal section/list page context — this is a hardcoded-path pattern to be aware of if adding a new section.
- `layouts/partials/list.html` + `layouts/partials/GetArticles.html` (which queries `where site.RegularPages "Type" "post"`) implement a different, paginated article-grid pattern with a `partialCached` call — this isn't wired into `blog.html`/`projects.html`'s actual rendering path today, so treat it as an alternate/in-progress listing implementation, not the live one, before extending it.
- `layouts/_default/taxonomy.html` is yet a third near-duplicate of this same listing pattern, used for category/tag archive pages.

**Front matter drives SEO/social meta directly**, not a fixed schema: each content page includes a `seo.extra` array of arbitrary `{name, value, keyName, relativeUrl}` objects, looped over in `layouts/_default/baseof.html` to emit `<meta>` tags (used for `og:*` and `twitter:*` tags today). `seo.metatitle`/`seo.description` set the title/description tags.

**Styling:** single Sass entry point `assets/sass/main.scss`, compiled inline via Hugo Pipes (`resources.ToCSS`) directly in `baseof.html` — there is no separate CSS build tool. Partial stylesheets live in `assets/sass/imports/` (`_general`, `_header`, `_footer`, `_posts-pages`, `_palettes`, etc.). The `palette-{name}` class on `<body>` (from `data/config.json`'s `palette` field) is how `_palettes.scss` themes the site.

**KaTeX math rendering is opt-in per page** via a `math: true` front matter param (only `content/msc_thesis.md`, `research.md`, `meerrings.md` use it); it conditionally includes `layouts/partials/katex.html`, which pulls KaTeX from a CDN.

**Netlify-specific coupling to remove/replace during the Jekyll migration:**
- `layouts/_default/baseof.html` loads the Netlify Identity widget script and redirects logged-in users to `/admin/`.
- `layouts/_default/contact.html` renders a form with `data-netlify="true" data-netlify-honeypot="bot-field"` (Netlify Forms) posting to `/success`, backed by `content/contact.md` and `content/success.md`.
- `static/admin/` is a Netlify CMS (Decap CMS) admin UI; `static/admin/config.yml` defines the `thoughts` and `sideprojects` collections (with a `git-gateway` backend) and must be kept in sync with whatever front-matter fields the templates actually read — if front matter fields change, update both the templates *and* this CMS schema (or drop the CMS entirely if it won't be carried over to Jekyll/GitHub Pages).
