# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Sriram Sankar's personal academic/portfolio/blog site (sriramsankar.in), built with **Jekyll** and deployed via **GitHub Pages** (custom domain via the root `CNAME` file). It was migrated from Hugo/Netlify; the git history's early commits ("Initial commit of existing Hugo site", "Scaffold Jekyll site...") document that cutover and the Hugo→Jekyll field mappings if something looks unported.

## Commands

- Install deps: `bundle install`
- Local dev server: `bundle exec jekyll serve` (add `--drafts` to include drafts)
- Build only: `bundle exec jekyll build` — output goes to `_site/`
- Uses the `github-pages` gem (see `Gemfile`), which pins Jekyll and plugin versions to match what GitHub Pages actually runs in production — don't add gems/plugins outside what that gem whitelists, or the GitHub-side build will diverge from local builds.
- No test suite or linter exists in this repo.

## Architecture

**Two-file site config split** (mirrors the old Hugo config.yaml/data/config.json split, kept for continuity):
- `_config.yml` — Jekyll build config: url/baseurl, collections, permalinks, plugins (`jekyll-sitemap`), and a `social.share.*` block (exposed as `site.social.share.*`, used by `_includes/socialshare.html`).
- `_data/config.json` — site *content* config, exposed in templates as `site.data.config`: site title, color `palette` name, header nav/social links, footer text, and `domain`. Nav/social links are data-driven lists rendered by `_includes/navigation.html`.

**Layout selection is front-matter-driven.** Every page/collection doc sets an explicit `layout:` field (`post`, `blog`, `projects`, `page`) resolved against `_layouts/*.html`. There's no reliance on Jekyll's directory-based defaults beyond the `defaults:` block in `_config.yml`, which only fills in `layout: post` for the two custom collections as a safety net.

**Content model:**
- `_thoughts/` (poems/blog posts) and `_sideprojects/` (project write-ups) are custom Jekyll collections (`output: true`, permalink `/:collection/:path/`), not `_posts` — filenames are plain slugs (no `YYYY-MM-DD-` prefix), sorting/date display is handled manually in the layouts via `{{ site.thoughts | sort: "date" | reverse }}` etc. rather than Jekyll's automatic `_posts` chronological behavior.
- `_layouts/blog.html` and `projects.html` render those two collections' index pages (`thoughts.md` / `sideprojects.md` at repo root) by iterating `site.thoughts` / `site.sideprojects` directly.
- Root-level `.md` files (e.g. `contact.md`, `research.md`, `msc_thesis.md`, `index.md`) are plain Jekyll Pages, each with an explicit `permalink:` front matter field set to match the site's original clean URLs (e.g. `/contact/`) — Jekyll doesn't give plain pages clean URLs by default, so don't remove these `permalink:` lines without checking the URL still resolves the same way.
- Category/tag **archive pages were intentionally dropped** in the Jekyll port (Hugo's `taxonomy.html` had no Jekyll equivalent ported) — `categories:` front matter still exists on content as metadata, but nothing renders an archive page from it. `robots.txt` still disallows `/tags/`/`/categories/` defensively even though nothing generates those paths today.

**Front matter drives SEO/social meta directly**, not a fixed schema: each page includes a `seo.extra` array of arbitrary `{name, value, keyName, relativeUrl}` objects, looped over in `_layouts/default.html` to emit `<meta>` tags (`og:*`/`twitter:*` today). `seo.metatitle`/`seo.description` set the title/description tags. `relativeUrl: true` entries are resolved with Jekyll's `absolute_url` filter.

**Styling:** `assets/css/main.scss` is the Sass entry point (needs the empty `---\n---` front-matter stub at the top so Jekyll's Sass converter processes it) — Jekyll's built-in `jekyll-sass-converter` compiles it, no separate CSS build tool. Partials live in `_sass/imports/` (`_general`, `_header`, `_footer`, `_posts-pages`, `_palettes`, etc.), imported by basename from `main.scss`. The `palette-{name}` class on `<body>` (from `_data/config.json`'s `palette` field) is how `_palettes.scss` themes the site.

**KaTeX math rendering is opt-in per page** via a `math: true` front matter param (`msc_thesis.md`, `research.md`, `meerrings.md`); it conditionally includes `_includes/katex.html`, which pulls KaTeX from a CDN.

**`contact.md` has no form** — it uses the plain `page` layout and embeds the CV PDF (`ssankar_Nov2023_cv.pdf`) directly via an `<iframe>` instead. There's no form backend/Formspree wiring in this repo; if a contact form gets reintroduced later, remember GitHub Pages can't run server-side form handling (the old Netlify Forms integration was removed during the Hugo→Jekyll migration).

**No CMS admin UI.** The old Netlify CMS (Decap) admin at `static/admin/` relied on Netlify Identity + git-gateway, neither of which exists on GitHub Pages, and was dropped rather than reconfigured. Content is edited directly as Markdown files in the repo (or via GitHub's web editor).
