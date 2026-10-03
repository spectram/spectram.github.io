---
permalink: /talks/
title: Talks
subtitle: >-
  Conference talks, colloquia, and posters on gas accretion, resolved HI, and anomalous gas, and the schools that trained me in radio interferometry.
img_path: images/telescopes/sriram_wsrt.jpg
seo:
  metatitle: Talks | Sriram Sankar
  description: >-
    Talks and presentations by Sriram Sankar on gas accretion, resolved HI 21 cm observations, and anomalous gas in galaxies.
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: Talks | Sriram Sankar
      keyName: property
    - name: 'og:description'
      value: >-
        Talks and presentations by Sriram Sankar on gas accretion, resolved HI 21 cm observations, and anomalous gas in galaxies.
      keyName: property
    - name: 'og:image'
      value: images/telescopes/sriram_wsrt.jpg
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: Talks | Sriram Sankar
    - name: 'twitter:description'
      value: >-
        Talks and presentations by Sriram Sankar on gas accretion, resolved HI 21 cm observations, and anomalous gas in galaxies.
    - name: 'twitter:image'
      value: images/telescopes/sriram_wsrt.jpg
      relativeUrl: true
layout: page
---
{% assign t = site.data.talks %}

## Talks and posters

<ul class="sr-list">
{% for x in t.talks %}
  <li><span class="sr-meta">{{ x.date }} · {{ x.type }}</span><br>
  <span class="title">{{ x.title }}</span>{% if x.event %}<br>{% if x.event_url %}<a href="{{ x.event_url }}">{{ x.event }}</a>{% else %}{{ x.event }}{% endif %}{% if x.place %}, {{ x.place }}{% endif %}{% endif %}{% for l in x.links %} · <a href="{{ l.url }}">{{ l.label }}</a>{% endfor %}</li>
{% endfor %}
</ul>

## Schools and workshops

<ul class="sr-list">
{% for s in t.schools %}
  <li><a class="title" href="{{ s.url }}">{{ s.name }}</a><br><span class="sr-meta">{{ s.detail }}</span></li>
{% endfor %}
</ul>
