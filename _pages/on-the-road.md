---
layout: default
title: On the Road
permalink: /beyond-research/on-the-road/
section: on-the-road
kicker: Journeys & Rides
---

<div class="beyond-module">
  <header class="beyond-module__hero">
    <a class="beyond-module__back" href="{{ '/beyond-research/' | relative_url }}">← Beyond Research</a>
    <p>{{ page.kicker }}</p>
    <h1>{{ page.title }}</h1>
    <div>Rides, journeys, and places encountered slowly. This collection is for motorcycle trips, travel photographs, routes, weather, and the small details that make a place memorable.</div>
  </header>
  {% assign entries = site.beyond_entries | where: "section", page.section | sort: "date" | reverse %}
  {% if entries.size > 0 %}
    <div class="beyond-entry-list">{% for entry in entries %}<article class="beyond-entry-card"><a href="{{ entry.url | relative_url }}" aria-label="Read {{ entry.title | escape }}"><div class="beyond-entry-card__cover{% unless entry.cover %} beyond-entry-card__cover--placeholder{% endunless %}"{% if entry.cover %} style="background-image: url('{{ entry.cover | relative_url }}');"{% endif %}></div><div class="beyond-entry-card__body"><p>{{ entry.date | date: "%b %-d, %Y" }}{% if entry.type %} · {{ entry.type }}{% endif %}</p><h2>{{ entry.title }}</h2>{% if entry.excerpt %}<span>{{ entry.excerpt }}</span>{% endif %}</div></a></article>{% endfor %}</div>
  {% else %}
    <section class="beyond-module__empty"><p>First entry pending</p><h2>This collection is ready when you are.</h2><span>Add a photograph, a short note, or a full story using the shared entry template.</span></section>
  {% endif %}
</div>
