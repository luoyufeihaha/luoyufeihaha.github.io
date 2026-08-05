---
layout: about
title: Home
permalink: /
nav: false # the theme renders Home separately in the navbar
nav_order: 1
subtitle: Reliable Long-Horizon LLM Agents · Structured Memory · Experience Reuse

profile: false
selected_papers: false # rendered explicitly below so the section title stays site-controlled
social: false # academic links are integrated into the profile sidebar

announcements:
  enabled: false # enable after there is a verified public update to share
  scrollable: true
  limit: 5

latest_posts:
  enabled: false # enable when blog content is ready
  scrollable: true
  limit: 3
---

<link rel="stylesheet" href="{{ '/assets/css/research-home.css' | relative_url }}">

<div class="research-home">
  <aside class="profile-sidebar" aria-labelledby="researcher-name">
    <div class="profile-sidebar__inner">
      <img class="profile-sidebar__avatar" src="{{ '/assets/img/profile_avatar.jpg' | relative_url }}" alt="Portrait of Yufei Luo" width="800" height="800" loading="eager">

      <h1 id="researcher-name">Yufei Luo</h1>
      <p class="profile-sidebar__positioning">{{ page.subtitle }}</p>

      <nav class="profile-sidebar__links" aria-label="Academic profiles">
        <a href="https://scholar.google.com/citations?user=w7A8DdIAAAAJ" aria-label="Google Scholar" title="Google Scholar">
          <i class="ai ai-google-scholar" aria-hidden="true"></i>
        </a>
        <a href="https://github.com/luoyufeihaha" aria-label="GitHub" title="GitHub">
          <i class="fa-brands fa-github" aria-hidden="true"></i>
        </a>
        <a href="https://orcid.org/0009-0005-4791-1228" aria-label="ORCID" title="ORCID">
          <i class="ai ai-orcid" aria-hidden="true"></i>
        </a>
      </nav>

      <p class="profile-sidebar__location">
        <i class="fa-solid fa-location-dot" aria-hidden="true"></i>
        Beijing, China
      </p>

      <section class="profile-interests" aria-labelledby="research-interests-title">
        <h2 id="research-interests-title">Research Interests</h2>
        <ul>
          <li>Reliable long-horizon agents</li>
          <li>Structured memory</li>
          <li>Experience reuse</li>
        </ul>
      </section>
    </div>

  </aside>

  <div class="research-content">
    <section class="research-section research-about" aria-labelledby="about-title">
      <div class="research-section__heading">
        <h2 id="about-title">About</h2>
      </div>

      <div class="research-about__body">
        <p class="research-about__lede">
          I study how to build reliable LLM agents for long-horizon tasks.
        </p>
        <p>
          My research develops external mechanisms—including structured memory, execution-state modeling, and experience reuse—that help agents preserve task-relevant information and act consistently across extended interactions. My current work,
          <a href="{{ '/research/memsif/' | relative_url }}">MemSIF</a>, transforms long-term interaction histories into structured representations and query-adaptive fact memories.
        </p>
        <p>
          Previously, I developed robust learning methods for linguistic steganalysis under distribution shift and worked on multimodal and multi-turn intent recognition at Lenovo Research. I completed an M.S. in Cyberspace Security at Beijing University of Posts and Telecommunications.
        </p>
      </div>
    </section>

    <section class="research-section research-selected" aria-labelledby="selected-publications-title">
      <div class="research-section__heading research-section__heading--with-link">
        <h2 id="selected-publications-title">Selected Publications</h2>
        <a class="research-section__link" href="{{ '/publications/' | relative_url }}">
          View all <span aria-hidden="true">→</span>
        </a>
      </div>

      {% include selected_papers.liquid %}
    </section>

    <section class="research-section research-agenda" aria-labelledby="research-agenda-title">
      <div class="research-section__heading">
        <h2 id="research-agenda-title">Research Agenda</h2>
      </div>

      <div class="research-agenda__intro">
        <h3>Three foundations for reliable agents</h3>
        <p>I investigate how external memory and reusable experience can improve reliability beyond a model's immediate context window.</p>
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

    <section class="research-section research-contact" aria-labelledby="contact-title">
      <div class="research-section__heading">
        <h2 id="contact-title">Contact</h2>
      </div>

      <div class="research-contact__body">
        <p class="research-contact__prompt">Interested in reliable and memory-augmented agents?</p>
        <p>I am seeking Ph.D. opportunities beginning in Fall 2027.</p>
        <a href="mailto:luoyf@bupt.edu.cn">luoyf@bupt.edu.cn <span aria-hidden="true">↗</span></a>
      </div>
    </section>

  </div>
</div>
