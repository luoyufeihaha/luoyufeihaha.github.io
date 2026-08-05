---
layout: about
title: Home
permalink: /
nav: false # the theme renders Home separately in the navbar
nav_order: 1
subtitle: Reliable Long-Horizon LLM Agents · Structured Memory · Experience Reuse

profile: false
selected_papers: false # rendered explicitly below so the section title stays site-controlled
social: false # contact links are integrated into the homepage hero

announcements:
  enabled: false # enable after there is a verified public update to share
  scrollable: true
  limit: 5

latest_posts:
  enabled: false # enable when blog content is ready
  scrollable: true
  limit: 3
---

<link rel="stylesheet" href="{{ '/assets/css/research-home.css' | relative_url | bust_file_cache }}">

<div class="research-home">
  <section class="research-hero" aria-labelledby="researcher-name">
    <div class="research-hero__copy">
      <img class="research-hero__avatar" src="{{ '/assets/img/profile_avatar.jpg' | relative_url | bust_file_cache }}" alt="Portrait of Yufei Luo" width="800" height="800" loading="eager">
      <p class="research-eyebrow">LLM Agents · Structured Memory · Experience Reuse</p>
      <h1 id="researcher-name">Yufei Luo</h1>
      <p class="research-hero__lede">
        I study how to build reliable LLM agents for long-horizon tasks.
      </p>
      <p class="research-hero__summary">
        My research develops external mechanisms—including structured memory, execution-state modeling, and experience reuse—that help agents preserve task-relevant information and act consistently across extended interactions. My current work,
        <a href="{{ '/research/memsif/' | relative_url }}">MemSIF</a>, transforms long-term interaction histories into structured representations and query-adaptive fact memories.
      </p>
      <p class="research-hero__background">
        Previously, I developed robust learning methods for linguistic steganalysis under distribution shift and worked on multimodal and multi-turn intent recognition at Lenovo Research. I completed an M.S. in Cyberspace Security at Beijing University of Posts and Telecommunications.
      </p>

      <div class="research-hero__actions" aria-label="Primary links">
        <a class="research-button research-button--primary" href="{{ '/research/memsif/' | relative_url }}">
          Explore MemSIF <span aria-hidden="true">→</span>
        </a>
        <a class="research-button research-button--secondary" href="mailto:luoyf@bupt.edu.cn">Email me</a>
      </div>

      <nav class="research-hero__links" aria-label="Academic profiles">
        <a href="https://scholar.google.com/citations?user=w7A8DdIAAAAJ">Google Scholar</a>
        <a href="https://github.com/luoyufeihaha">GitHub</a>
        <a href="https://orcid.org/0009-0005-4791-1228">ORCID</a>
        <span>Beijing, China</span>
      </nav>
    </div>

    <aside class="research-hero__visual" aria-label="MemSIF research concept">
      <div class="research-visual__header">
        <span>Current research</span>
        <span class="research-visual__status">2026</span>
      </div>
      <div class="research-visual__flow">
        <div class="research-visual__node research-visual__node--source">
          <span class="research-visual__label">Input</span>
          <strong>Interaction history</strong>
          <small>long-term · multi-session</small>
        </div>
        <span class="research-visual__arrow" aria-hidden="true">↓</span>
        <div class="research-visual__node research-visual__node--core">
          <span class="research-visual__label">Structure</span>
          <strong>Interaction memory</strong>
          <small>organized · state-aware</small>
        </div>
        <span class="research-visual__arrow" aria-hidden="true">↓</span>
        <div class="research-visual__branches">
          <div class="research-visual__branch">
            <span>CoreFact</span>
            <small>stable facts</small>
          </div>
          <div class="research-visual__branch">
            <span>ActiveFact</span>
            <small>query-adaptive</small>
          </div>
        </div>
      </div>
      <p class="research-visual__caption">Structured memory for reliable long-horizon behavior</p>
    </aside>

  </section>

  <section class="research-section research-agenda" aria-labelledby="research-agenda-title">
    <div class="research-section__heading">
      <div>
        <p class="research-kicker">Research agenda</p>
        <h2 id="research-agenda-title">Three foundations for reliable agents</h2>
      </div>
      <p>
        I investigate how external memory and reusable experience can improve reliability beyond a model's immediate context window.
      </p>
    </div>

    <div class="research-agenda__grid">
      <article class="research-interest-card">
        <span class="research-interest-card__number">01</span>
        <h3>Reliable long-horizon agents</h3>
        <p>Maintaining coherent decisions and behavior across extended tasks and interactions.</p>
      </article>
      <article class="research-interest-card">
        <span class="research-interest-card__number">02</span>
        <h3>Structured memory</h3>
        <p>Preserving relevant facts, context, and execution progress in explicit representations.</p>
      </article>
      <article class="research-interest-card">
        <span class="research-interest-card__number">03</span>
        <h3>Experience reuse</h3>
        <p>Turning prior interactions into reusable knowledge, strategies, and capabilities.</p>
      </article>
    </div>

  </section>

  <section class="research-section research-selected" aria-labelledby="selected-publications-title">
    <div class="research-section__heading research-section__heading--publications">
      <div>
        <p class="research-kicker">Selected work</p>
        <h2 id="selected-publications-title">Selected Publications</h2>
      </div>
      <a class="research-section__link" href="{{ '/publications/' | relative_url }}">
        View all publications <span aria-hidden="true">→</span>
      </a>
    </div>

    {% include selected_papers.liquid %}

  </section>

  <section class="research-contact" aria-label="Contact">
    <div>
      <p class="research-kicker">Contact</p>
      <h2>Interested in reliable and memory-augmented agents?</h2>
    </div>
    <div class="research-contact__details">
      <p>I am seeking Ph.D. opportunities beginning in Fall 2027.</p>
      <a href="mailto:luoyf@bupt.edu.cn">luoyf@bupt.edu.cn <span aria-hidden="true">↗</span></a>
    </div>
  </section>
</div>
