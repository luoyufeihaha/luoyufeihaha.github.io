---
layout: default
title: Reading Shelf
permalink: /beyond-research/reading-shelf/
section: reading-shelf
kicker: Books & Lines
---

<div class="beyond-module">
  <header class="beyond-module__hero">
    <a class="beyond-module__back" href="{{ '/beyond-research/' | relative_url }}">← Beyond Research</a>
    <p>{{ page.kicker }}</p>
    <h1>{{ page.title }}</h1>
    <div>Books in progress, authors I return to, and lines worth keeping. Entries may be a reading note, a short introduction to an author, or simply a passage that has stayed with me.</div>
  </header>
  {% assign entries = site.beyond_entries | where: "section", page.section | sort: "date" | reverse %}
  {% if entries.size > 0 %}
    <div class="beyond-entry-list">{% for entry in entries %}<article class="beyond-entry-card"><a href="{{ entry.url | relative_url }}" aria-label="Read {{ entry.title | escape }}"><div class="beyond-entry-card__cover{% unless entry.cover %} beyond-entry-card__cover--placeholder{% endunless %}"{% if entry.cover %} style="background-image: url('{{ entry.cover | relative_url }}');"{% endif %}></div><div class="beyond-entry-card__body"><p>{{ entry.date | date: "%b %-d, %Y" }}{% if entry.type %} · {{ entry.type }}{% endif %}</p><h2>{{ entry.title }}</h2>{% if entry.excerpt %}<span>{{ entry.excerpt }}</span>{% endif %}</div></a></article>{% endfor %}</div>
  {% else %}
    <section class="beyond-module__empty"><p>First entry pending</p><h2>This collection is ready when you are.</h2><span>Add a photograph, a short note, or a full story using the shared entry template.</span></section>
  {% endif %}
</div>
