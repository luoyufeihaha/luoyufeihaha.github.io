---
layout: page
title: Research
permalink: /research/
description: Research projects on LLM Agents, Structured Memory, and Steganalysis.
nav: true
nav_order: 2
horizontal: true
---

<link rel="stylesheet" href="{{ '/assets/css/research-page.css' | relative_url }}">

My research centers on reliable intelligent systems: how agents can retain and use experience over long horizons, and how learning systems can remain robust when data conditions change. The projects below summarize the public scope of my work and link to the corresponding publications where available.

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>

<section class="industry-experience" aria-labelledby="industry-experience-title">
  <h2 id="industry-experience-title">Industry Experience</h2>

  <article class="industry-experience__entry">
    <div class="industry-experience__header">
      <div>
        <p class="industry-experience__role">Research Intern</p>
        <h3>Lenovo Research</h3>
      </div>
      <p class="industry-experience__period">
        <time datetime="2025-07">Jul 2025</time> – <time datetime="2026-01">Jan 2026</time>
      </p>
    </div>

    <p class="industry-experience__summary">
      Worked on multimodal and multi-turn dialogue intent recognition, investigating policy learning and reasoning strategies for more reliable dialogue systems.
    </p>

    <ul class="industry-experience__topics" aria-label="Research topics">
      <li>Multimodal Learning</li>
      <li>Reinforcement Learning</li>
      <li>Dialogue Systems</li>
    </ul>

  </article>
</section>
