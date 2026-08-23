---
layout: default
title: MemSIF — Long-Horizon Memory for LLM Agents
description: Structured interaction-to-fact memory for reliable long-horizon LLM agents.
importance: 1
permalink: /research/memsif/
---

<link rel="stylesheet" href="{{ '/assets/css/research-page.css' | relative_url }}">

<article class="memsif-project">
  <a class="memsif-project__back" href="{{ '/research/' | relative_url }}">← Research</a>

  <header class="memsif-project__hero">
    <p class="memsif-project__eyebrow">Featured project · 2026</p>
    <h1>MemSIF</h1>
    <p class="memsif-project__subtitle">From Structured Interactions to Dual-Track Fact Memory for LLM Agents</p>
    <p class="memsif-project__lead">
      A structured interaction-to-fact memory framework that helps long-horizon agents preserve related evidence across time and turn information whose value emerges later into reusable facts.
    </p>
    <p class="memsif-project__meta">Yufei Luo, Xiucheng Xu, and Zhen Yang · arXiv, 2026</p>
    <p class="memsif-project__role">Self-led research project · Project lead and first author</p>

    <div class="research-actions" aria-label="MemSIF resources">
      <a class="research-action research-action--primary" href="https://arxiv.org/abs/2608.01742">Paper <span aria-hidden="true">↗</span></a>
      <a class="research-action" href="https://arxiv.org/pdf/2608.01742">PDF <span aria-hidden="true">↗</span></a>
      <a class="research-action" href="https://github.com/luoyufeihaha/MemSIF">Code <span aria-hidden="true">↗</span></a>
      <a class="research-action" href="{{ '/publications/' | relative_url }}">Publications <span aria-hidden="true">→</span></a>
    </div>

  </header>

  <figure class="memsif-project__figure">
    <img
      src="{{ '/assets/img/publication_preview/memsif-framework.png' | relative_url }}"
      alt="MemSIF framework with Structured Interaction Memory and Dual-Track Fact Memory"
      loading="eager"
    >
    <figcaption>Structured Interaction Memory and Dual-Track Fact Memory jointly organize interaction history and reusable facts.</figcaption>
  </figure>

  <section class="memsif-project__section" aria-labelledby="memsif-overview-title">
    <p class="memsif-project__section-label">Problem and idea</p>
    <h2 id="memsif-overview-title">Organizing long-term interactions beyond chronological order</h2>
    <div class="memsif-project__prose">
      <p>
        Long interaction histories are not naturally organized by time. Related evidence may be distributed across distant parts of a conversation, while information that appears unimportant when first observed may become valuable only after a later query. MemSIF characterizes these challenges as <strong>Temporal–Structural Misalignment (TSM)</strong> and <strong>Delayed Utility Manifestation (DUM)</strong>.
      </p>
      <p>
        To address them, MemSIF combines <strong>Structured Interaction Memory</strong> with <strong>Dual-Track Fact Memory</strong>. The first organizes interactions around their topical and event-level relationships; the second combines proactive fact consolidation with query-driven fact formation when information utility emerges later.
      </p>
    </div>
  </section>

  <section class="memsif-project__section" aria-labelledby="memsif-evidence-title">
    <p class="memsif-project__section-label">Evidence and continuity</p>
    <h2 id="memsif-evidence-title">An initial step toward reliable execution state</h2>
    <div class="memsif-project__prose">
      <p class="memsif-project__evidence">
        Across LoCoMo and LongMemEval-S with five backbone LLMs, MemSIF achieved the highest Total ACC in every evaluated setting, outperforming the strongest baseline by 2.29%–8.79% and 2.87%–6.15%, respectively.
      </p>
      <p>
        MemSIF studies how an agent organizes what it has experienced and preserves it for future use. My next step is to investigate how agents can maintain the evolving execution state that directly supports their next action, creating a path toward state-supported verification, recovery, and reliable experience reuse over longer tasks.
      </p>
    </div>
  </section>
</article>
