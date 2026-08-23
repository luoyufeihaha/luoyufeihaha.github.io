---
layout: default
permalink: /publications/
title: Publications
description: Peer-reviewed publications and current manuscripts.
nav: false
---

<link rel="stylesheet" href="{{ '/assets/css/publications-page.css' | relative_url }}">

<main class="publication-archive">
  <header class="publication-archive__hero">
    <p class="publication-archive__eyebrow">Publications</p>
    <h1>Research publications and manuscripts</h1>
    <p class="publication-archive__lead">
      A complete record of my work on reliable LLM agents, linguistic steganalysis, and related learning problems.
    </p>
    <p class="publication-archive__note">
      Publications are listed in reverse chronological order. My name is highlighted, and contribution notes appear with the corresponding entry.
    </p>
    <div class="publication-archive__actions" aria-label="Publication and CV links">
      <a href="https://scholar.google.com/citations?user=w7A8DdIAAAAJ" target="_blank" rel="noopener noreferrer">Google Scholar <span aria-hidden="true">↗</span></a>
      <a href="{{ '/assets/pdf/Yufei_Luo_CV.pdf' | relative_url }}" target="_blank" rel="noopener">CV <span aria-hidden="true">↗</span></a>
    </div>
  </header>

  <section class="publication-archive__catalog" aria-labelledby="publication-list-title">
    <div class="publication-archive__catalog-heading">
      <p>Publication record</p>
      <h2 id="publication-list-title">All publications</h2>
    </div>

    {% include bib_search.liquid %}

    <div class="publications">
      {% bibliography %}
    </div>

  </section>
</main>
