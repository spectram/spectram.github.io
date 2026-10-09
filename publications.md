---
permalink: /publications/
title: Publications & Talks
subtitle: >-
  Papers and talks on gas accretion, resolved HI, and the multiphase gas around galaxies, from analytic theory and hydrodynamic simulations to MeerKAT, ASKAP, HST, and Keck data.
img_path: images/pub+cv-bg.jpg
seo:
  metatitle: Publications & Talks | Sriram Sankar
  description: >-
    Publications and talks by Sriram Sankar on gas accretion, resolved HI 21 cm observations, and the multiphase gas around galaxies.
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: Publications & Talks | Sriram Sankar
      keyName: property
    - name: 'og:description'
      value: >-
        Publications and talks by Sriram Sankar on gas accretion, resolved HI 21 cm observations, and the multiphase gas around galaxies.
      keyName: property
    - name: 'og:image'
      value: images/sci/hot_accretion_warp.png
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: Publications & Talks | Sriram Sankar
    - name: 'twitter:description'
      value: >-
        Publications and talks by Sriram Sankar on gas accretion, resolved HI 21 cm observations, and the multiphase gas around galaxies.
    - name: 'twitter:image'
      value: images/sci/hot_accretion_warp.png
      relativeUrl: true
layout: page
---
{% assign pubs = site.data.publications %}

<div class="sr-stats">
  <div class="sr-stat"><span class="num">{{ pubs.summary.refereed }}</span><span class="lbl">refereed papers</span></div>
  <div class="sr-stat"><span class="num">{{ pubs.summary.h_index }}</span><span class="lbl">h-index (NASA ADS)</span></div>
  <div class="sr-stat"><span class="num"><a href="{{ pubs.summary.ads_library }}">SciX</a></span><span class="lbl">full list in my <a href="{{ pubs.summary.ads_library }}">SciX library</a></span></div>
  <div class="sr-stat"><span class="num"><a href="{{ pubs.summary.orcid }}">iD</a></span><span class="lbl"><a href="{{ pubs.summary.orcid }}">ORCID 0000-0002-7607-081X</a></span></div>
</div>

## Highlights

{% for h in pubs.highlights %}{% assign p = pubs.papers | where: "key", h.key | first %}
<div class="sr-highlight{% if h.wide %} wide{% endif %}">
  <a href="{{ p.url }}"><img src="{{ h.image }}" alt="{{ h.image_alt }}" loading="lazy"></a>
  <div>
    <p class="title"><strong>{{ h.heading }}</strong></p>
    <p>{{ h.summary }}</p>
    <p class="sr-meta">{{ p.authors }}, “<a href="{{ p.url }}">{{ p.title }}</a>”, {{ p.venue }}</p>
  </div>
</div>
{% endfor %}

## Refereed

<ul class="sr-list">
{% for p in pubs.papers %}{% if p.status == "refereed" %}
  <li>{{ p.authors }}, “<a class="title" href="{{ p.url }}">{{ p.title }}</a>”, {{ p.venue }}{% if p.role %}<span class="role">{{ p.role }}</span>{% endif %}</li>
{% endif %}{% endfor %}
</ul>

## Submitted, to be submitted, and in preparation

<ul class="sr-list">
{% for p in pubs.papers %}{% if p.status != "refereed" %}
  <li>{{ p.authors }}, “<span class="title">{{ p.title }}</span>” <span class="sr-pill">{{ p.status_label }}</span>{% if p.role %}<span class="role">{{ p.role }}</span>{% endif %}</li>
{% endif %}{% endfor %}
</ul>

{% assign t = site.data.talks %}

## Talks and posters {#talks}

<ul class="sr-list">
{% for x in t.talks %}
  <li><span class="sr-meta">{{ x.date }} · {{ x.type }}</span><br>
  <span class="title">{{ x.title }}</span>{% if x.event %}<br>{% if x.event_url %}<a href="{{ x.event_url }}">{{ x.event }}</a>{% else %}{{ x.event }}{% endif %}{% if x.place %}, {{ x.place }}{% endif %}{% endif %}{% for l in x.links %} · <a href="{{ l.url }}">{{ l.label }}</a>{% endfor %}</li>
{% endfor %}
</ul>

## Schools and workshops

<ul class="sr-list">
{% for sc in t.schools %}
  <li><a class="title" href="{{ sc.url }}">{{ sc.name }}</a><br><span class="sr-meta">{{ sc.detail }}</span></li>
{% endfor %}
</ul>

Telescope proposals and the full CV are on the [Contact & CV](/contact/) page.
