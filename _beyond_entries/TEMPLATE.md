---
layout: default
title: "[Entry title]"
section: on-the-road # on-the-road | reading-shelf | field-notes | on-court | small-archive
type: "[Ride / Reading Note / Reflection / Basketball / Archive]"
date: 2026-08-08
excerpt: "[One sentence shown on the collection page.]"
cover: # /assets/img/beyond/[collection]/[filename].webp
cover_alt: "[A concise description of the cover image.]"
tags: []
published: false
---

<!--
Copy this file, rename it (for example: 2026-western-sichuan-ride.md), and set `published: true` when ready.
Use one heading level at a time; photographs can be added with standard Markdown image syntax.
Do not include exact real-time locations, vehicle license plates, or identifiable information about others without permission.
-->

<article class="beyond-entry">
  <header class="beyond-entry__header">
    <a class="beyond-module__back" href="{{ '/beyond-research/' | append: page.section | append: '/' | relative_url }}">← {{ page.section | replace: '-', ' ' | capitalize }}</a>
    <p>{{ page.date | date: "%B %-d, %Y" }}{% if page.type %} · {{ page.type }}{% endif %}</p>
    <h1>{{ page.title }}</h1>
    {% if page.excerpt %}<span>{{ page.excerpt }}</span>{% endif %}
    {% if page.cover %}<img src="{{ page.cover | relative_url }}" alt="{{ page.cover_alt | default: page.title | escape }}" class="beyond-entry__cover">{% endif %}
  </header>
  <div class="beyond-entry__content">
    <h2>[A short opening]</h2>
    <p>[Write a brief introduction here.]</p>
    <h2>[A section]</h2>
    <p>[Add text, images, quotations, or a short list.]</p>
  </div>
</article>
