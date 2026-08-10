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
        <a href="mailto:luoyf@bupt.edu.cn">
          <i class="fa-regular fa-envelope" aria-hidden="true"></i><span>Email</span>
        </a>
        <a href="https://scholar.google.com/citations?user=w7A8DdIAAAAJ">
          <i class="ai ai-google-scholar" aria-hidden="true"></i><span>Google Scholar</span>
        </a>
        <a href="https://github.com/luoyufeihaha">
          <i class="fa-brands fa-github" aria-hidden="true"></i><span>GitHub</span>
        </a>
        <a href="https://orcid.org/0009-0005-4791-1228">
          <i class="ai ai-orcid" aria-hidden="true"></i><span>ORCID</span>
        </a>
      </nav>
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
          Previously, I developed robust learning methods for linguistic steganalysis under distribution shift and worked on multimodal and multi-turn intent recognition at Lenovo Research. I completed an M.S. in Cyberspace Security at Beijing University of Posts and Telecommunications, after earning a B.S. in Mathematics and Applied Mathematics from Nanchang University.
        </p>
      </div>
    </section>

    <section class="research-section research-selected" aria-labelledby="selected-publications-title">
      <div class="research-section__heading research-section__heading--with-link">
        <h2 id="selected-publications-title">Selected Publications</h2>
        <a class="research-section__link" href="https://scholar.google.com/citations?user=w7A8DdIAAAAJ" target="_blank" rel="noopener noreferrer">
          Google Scholar <span aria-hidden="true">↗</span>
        </a>
      </div>

      {% include selected_papers.liquid %}
    </section>

    <section class="research-section research-agenda" aria-labelledby="research-agenda-title">
      <div class="research-section__heading">
        <h2 id="research-agenda-title">Research Agenda</h2>
      </div>

      <div class="research-agenda__intro">
        <h3>Research directions for reliable agents</h3>
        <p>I investigate how structured execution state, external memory, and reusable experience can improve agent reliability across long-horizon tasks.</p>
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
          <p>Organizing task-relevant facts, context, and execution progress into explicit state representations.</p>
        </article>
        <article class="research-interest-card">
          <span class="research-interest-card__number">03</span>
          <h3>Experience reuse</h3>
          <p>Turning prior interactions into reusable knowledge, strategies, and capabilities.</p>
        </article>
      </div>
    </section>

    <section class="research-section research-honors" aria-labelledby="selected-honors-title">
      <div class="research-section__heading">
        <h2 id="selected-honors-title">Selected Honors</h2>
      </div>

      <ol class="research-honors__list">
        <li>
          <span class="research-honors__year">2026</span>
          <div>
            <h3>Beijing Outstanding Graduate <span class="research-honors__note">(Top 5%)</span></h3>
            <p>Beijing Municipal Education Commission</p>
          </div>
        </li>
        <li>
          <span class="research-honors__year">2025</span>
          <div>
            <h3>National Scholarship for Graduate Students</h3>
            <p>Ministry of Education of China</p>
          </div>
        </li>
        <li>
          <span class="research-honors__year">2025</span>
          <div>
            <h3>Open Source Security Award <span class="research-honors__note">(Third Prize)</span></h3>
            <p>China Cybersecurity Association</p>
          </div>
        </li>
      </ol>
    </section>

    {% if site.posts.size > 0 %}
      <section class="research-section research-writing" aria-labelledby="recent-writing-title">
        <div class="research-section__heading research-section__heading--with-link">
          <h2 id="recent-writing-title">Recent Writing</h2>
          <a class="research-section__link" href="{{ '/blog/' | relative_url }}">
            View all <span aria-hidden="true">→</span>
          </a>
        </div>

        <ol class="research-writing__list">
          {% for post in site.posts limit: 3 %}
            <li>
              <p class="research-writing__meta">{{ post.date | date: "%B %-d, %Y" }}</p>
              <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
              {% if post.description %}<p>{{ post.description }}</p>{% endif %}
            </li>
          {% endfor %}
        </ol>
      </section>
    {% endif %}

    <section class="research-section research-beyond" aria-labelledby="beyond-research-title">
      <div class="research-section__heading research-section__heading--with-link">
        <h2 id="beyond-research-title">Beyond Research</h2>
        <a class="research-section__link" href="{{ '/beyond-research/' | relative_url }}">
          More about me <span aria-hidden="true">→</span>
        </a>
      </div>

      <div class="research-beyond__body">
        <p>
          Outside research, I enjoy motorcycle travel, reading, basketball, and badminton. I also keep notes on books, journeys, and everyday experiences that shape how I think.
        </p>
      </div>
    </section>

    <section class="research-section research-contact" aria-labelledby="contact-title">
      <div class="research-section__heading">
        <h2 id="contact-title">Contact</h2>
      </div>

      <div class="research-contact__body">
        <p class="research-contact__prompt">Interested in reliable long-horizon agents?</p>
        <p>I am seeking Ph.D. opportunities beginning in Fall 2027.</p>
        <a href="mailto:luoyf@bupt.edu.cn">luoyf@bupt.edu.cn <span aria-hidden="true">↗</span></a>
      </div>
    </section>

  </div>
</div>
