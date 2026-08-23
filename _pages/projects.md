---
layout: default
title: Research
permalink: /research/
description: Research on reliable long-horizon agents, structured memory, and robust learning under distribution shift.
nav: true
nav_order: 2
---

<link rel="stylesheet" href="{{ '/assets/css/research-page.css' | relative_url }}">

<main class="research-overview">
  <aside class="research-overview__toc" aria-labelledby="research-contents-title">
    <p id="research-contents-title">Contents</p>
    <nav aria-label="Research page contents">
      <ol>
        <li><a href="#research-overview-top">Overview</a></li>
        <li><a href="#research-perspective-title">Current direction</a></li>
        <li><a href="#memsif-overview-title">MemSIF</a></li>
        <li><a href="#steganalysis-title">Linguistic steganalysis</a></li>
        <li><a href="#industry-experience-title">Additional experience</a></li>
      </ol>
    </nav>
  </aside>

  <header id="research-overview-top" class="research-overview__hero">
    <p class="research-overview__eyebrow">Research</p>
    <h1>Reliable execution of complex, long-horizon tasks in real-world environments</h1>
    <p class="research-overview__lead">
      My broader research interest is how AI agents can sustain reliable execution as their tasks, state, and environment evolve over time.
    </p>
    <p class="research-overview__intro">
      Long-horizon tasks involve dependent actions, evolving state, and feedback that may arrive late or with noise. These properties make failures structural: an early mistake can enter the system state and influence many later decisions. I study the mechanisms and evaluation principles that help agents remain reliable under these conditions, rather than assuming that reliability will emerge automatically from increasingly capable base models.
    </p>
  </header>

  <section class="research-overview__section" aria-labelledby="research-perspective-title">
    <div class="research-overview__section-header">
      <p>01 · Current direction</p>
      <h2 id="research-perspective-title">State organization and maintenance</h2>
    </div>

    <div class="research-overview__section-body research-prose">
      <p>
        Within this broader agenda, my current entry point is the organization and maintenance of execution state: an inspectable external representation of task state and the evidence supporting an agent’s decisions. Rather than treating the entire interaction history as an undifferentiated context, an agent should be able to preserve what remains relevant as a task and its environment evolve.
      </p>
      <p>
        I view this maintained state as a candidate foundation for recognizing execution deviations and making recovery decisions. Reliable experience reuse is a longer-term extension: an agent must determine when experience from an earlier task remains applicable to a new one. Together, these questions offer one focused path into the broader challenge of reliable execution over longer and more dynamic tasks.
      </p>
    </div>

    <div class="research-direction-summary">
      <div>
        <span>Current focus</span>
        <h3>Dynamic execution state</h3>
      </div>
      <p>A focused entry point into verification and recovery, with reliable experience reuse as a longer-term extension.</p>
    </div>

  </section>

  <section class="research-overview__section" aria-labelledby="memsif-overview-title">
    <div class="research-overview__section-header">
      <p>02 · Initial step</p>
      <h2 id="memsif-overview-title">MemSIF: structuring interaction history into reusable memory</h2>
    </div>

    <div class="research-feature">
      <figure class="research-feature__figure">
        <img
          src="{{ '/assets/img/publication_preview/memsif-framework.png' | relative_url }}"
          alt="Overview of MemSIF, combining Structured Interaction Memory with Dual-Track Fact Memory"
          loading="eager"
        >
        <figcaption>MemSIF organizes long-term interactions and turns emerging information utility into reusable facts.</figcaption>
      </figure>

      <div class="research-feature__content">
        <p>
          MemSIF is an initial exploration along this direction. It addresses two problems in long-term memory: related evidence may be distributed across distant interactions, and information that appears unimportant when first observed may become useful only later.
        </p>
        <p>
          The framework combines <strong>Structured Interaction Memory</strong> with <strong>Dual-Track Fact Memory</strong> to organize interactions by their underlying relationships and construct reusable facts both proactively and when their utility emerges through queries.
        </p>
        <p class="research-evidence">
          Across LoCoMo and LongMemEval-S with five backbone LLMs, MemSIF achieved the highest Total ACC in every evaluated setting, outperforming the strongest baseline by 2.29%–8.79% and 2.87%–6.15%, respectively.
        </p>
        <p>
          MemSIF focuses on organizing what an agent has experienced. It provides an empirical starting point for my future work on maintaining the evolving execution state that guides what an agent should do next.
        </p>

        <div class="research-actions" aria-label="MemSIF resources">
          <a class="research-action research-action--primary" href="{{ '/research/memsif/' | relative_url }}">Explore MemSIF <span aria-hidden="true">→</span></a>
          <a class="research-action" href="https://arxiv.org/abs/2608.01742">arXiv <span aria-hidden="true">↗</span></a>
          <a class="research-action" href="https://github.com/luoyufeihaha/MemSIF">Code <span aria-hidden="true">↗</span></a>
        </div>
      </div>
    </div>

  </section>

  <section class="research-overview__section" aria-labelledby="steganalysis-title">
    <div class="research-overview__section-header">
      <p>03 · Previous research</p>
      <h2 id="steganalysis-title">Toward reliable linguistic steganalysis under realistic deployment constraints</h2>
    </div>

    <div class="research-overview__section-body research-narrative">
      <p>
        Linguistic steganography conceals secret information in text designed to appear ordinary. Text without a hidden payload is called <strong>cover text</strong>, while text carrying hidden information is called <strong>stego text</strong>. <strong>Linguistic steganalysis</strong> is the defensive task of determining whether a given text is cover or stego, usually without needing to recover the hidden message itself.
      </p>
      <p>
        This detection capability matters because text can serve as a difficult-to-observe channel for covert communication. However, a detector developed under controlled conditions may not remain dependable after deployment: text domains, steganographic algorithms, embedding rates, and class proportions can change, while labeled target data, original source data, or stego training samples may be unavailable.
      </p>

      <h3>Research trajectory across deployment constraints</h3>
      <p>
        Rather than following a single progression of difficulty, these studies examine complementary constraints that arise in practice: distribution shift, restricted access to source data, scarce stego examples, and the complete absence of stego training samples.
      </p>

      <div class="research-trajectory">
        <article class="research-stage">
          <div class="research-stage__meta">
            <span>01</span>
            <p>Cross-domain adaptation</p>
          </div>
          <div class="research-stage__content">
            <h4>Transferring a detector to an unlabeled target domain</h4>
            <div class="research-stage__split">
              <div class="research-stage__copy">
                <p>
                  I first studied settings in which labeled source data remain available but the target domain is unlabeled. <strong>PDTS</strong> combines shared and task-specific representations with progressive pseudo-label self-training; across six corpus-transfer tasks and five embedding rates, it improved the average accuracy and F1 over the compared domain-adaptation baselines. Building on this work, <strong>CADA</strong> addresses class misalignment and ambiguous target boundaries through class-aware adversarial alignment and balanced progressive pseudo-label fine-tuning, improving average detection accuracy by 2.78%, 2.47%, and 0.38% on VLC, AC, and ADG, respectively.
                </p>
                <div class="research-stage__papers" aria-label="Cross-domain adaptation publications">
                  <a href="https://doi.org/10.1007/978-3-031-82907-9_10"><strong>PDTS</strong><span>ICCES 2024 · First author</span></a>
                  <a href="https://doi.org/10.1109/TIFS.2025.3569409"><strong>CADA</strong><span>IEEE TIFS 2025 · Equal contribution</span></a>
                </div>
              </div>
              <figure class="research-stage__figure">
                <a href="{{ '/assets/img/publication_preview/class-aware-domain-mismatch.png' | relative_url }}" target="_blank" rel="noopener" aria-label="Open the domain mismatch figure at full size">
                  <img src="{{ '/assets/img/publication_preview/class-aware-domain-mismatch.png' | relative_url }}" alt="Source and target cover and stego distributions before and after adaptation, with class-misaligned target samples highlighted." width="1260" height="788" loading="lazy" decoding="async">
                </a>
                <figcaption>
                  Domain mismatch can leave target samples aligned with the wrong source class.
                  <a href="{{ '/assets/img/publication_preview/class-aware-domain-mismatch.png' | relative_url }}" target="_blank" rel="noopener">View full size <span aria-hidden="true">↗</span></a>
                </figcaption>
              </figure>
            </div>
          </div>
        </article>

        <article class="research-stage">
          <div class="research-stage__meta">
            <span>02</span>
            <p>Source-free adaptation</p>
          </div>
          <div class="research-stage__content">
            <h4>Adapting without retaining the original source data</h4>
            <div class="research-stage__split">
              <div class="research-stage__copy">
                <p>
                  I then removed access to source data during adaptation. <strong>CPSLS</strong> uses clustering structure in the unlabeled target domain to generate pseudo-labels, weights classification by prediction uncertainty, and maintains prediction diversity to limit noisy-label accumulation and posterior collapse. It achieved the strongest average accuracy among the tested cross-domain methods, exceeding the best competing averages by 1.24, 0.82, and 0.53 percentage points on VLC, AC, and ADG.
                </p>
                <div class="research-stage__papers" aria-label="Source-free adaptation publication">
                  <a href="https://doi.org/10.1145/3733102.3733114"><strong>CPSLS</strong><span>ACM IH&amp;MMSec 2025 · First author</span></a>
                </div>
              </div>
              <figure class="research-stage__figure">
                <a href="{{ '/assets/img/publication_preview/cpsls-source-free-domain-adaptation-setting.png' | relative_url }}" target="_blank" rel="noopener" aria-label="Open the source-free domain adaptation figure at full size">
                  <img src="{{ '/assets/img/publication_preview/cpsls-source-free-domain-adaptation-setting.png' | relative_url }}" alt="Comparison between traditional domain adaptation, which accesses source data, and source-free domain adaptation, which retains only the trained source model." width="1110" height="709" loading="lazy" decoding="async">
                </a>
                <figcaption>
                  Source-free adaptation retains the trained source model rather than the source data.
                  <a href="{{ '/assets/img/publication_preview/cpsls-source-free-domain-adaptation-setting.png' | relative_url }}" target="_blank" rel="noopener">View full size <span aria-hidden="true">↗</span></a>
                </figcaption>
              </figure>
            </div>
          </div>
        </article>

        <article class="research-stage">
          <div class="research-stage__meta">
            <span>03</span>
            <p>Few-shot learning</p>
          </div>
          <div class="research-stage__content">
            <h4>Learning with scarce stego examples and class imbalance</h4>
            <p>
              In collaborative work, I also studied settings where stego samples are scarce while cover text is abundant. <strong>DAF-Stega</strong> uses multi-domain cover text to pretrain a transferable target-domain boundary, then combines few-shot fine-tuning with MC-dropout-based dynamic voting for pseudo-label self-training. It outperformed both reported few-shot baselines across every tested shot count from 30 to 200 on three corpora.
            </p>
            <div class="research-stage__papers" aria-label="Few-shot learning publication">
              <a href="https://doi.org/10.1109/LSP.2025.3553427"><strong>DAF-Stega</strong><span>IEEE SPL 2025 · Collaborative work</span></a>
            </div>
          </div>
        </article>

        <article class="research-stage">
          <div class="research-stage__meta">
            <span>04</span>
            <p>One-class learning</p>
          </div>
          <div class="research-stage__content">
            <h4>Detecting stego text after training on cover text alone</h4>
            <div class="research-stage__split">
              <div class="research-stage__copy">
                <p>
                  Finally, I considered cover-only training with no stego samples. <strong>CHLS</strong> builds a hypersphere around cover representations, generates contrastive negatives by applying word-level random swaps to boundary samples, and uses a boundary-aware contrastive objective to learn a compact cover region. Across three corpora and two steganographic algorithms, it achieved the strongest overall average AUC, accuracy, and F1 among the compared methods.
                </p>
                <div class="research-stage__papers" aria-label="One-class learning publication">
                  <a href="https://doi.org/10.1109/ICASSP55912.2026.11462507"><strong>CHLS</strong><span>IEEE ICASSP 2026 · First author</span></a>
                </div>
              </div>
              <figure class="research-stage__figure">
                <a href="{{ '/assets/img/publication_preview/contrastive-hypersphere-framework.png' | relative_url }}" target="_blank" rel="noopener" aria-label="Open the CHLS framework figure at full size">
                  <img src="{{ '/assets/img/publication_preview/contrastive-hypersphere-framework.png' | relative_url }}" alt="CHLS framework for generating contrastive-negative samples, optimizing a cover-text hypersphere, and classifying unseen text by its position relative to the hypersphere." width="1575" height="788" loading="lazy" decoding="async">
                </a>
                <figcaption>
                  CHLS learns a hypersphere for cover-only detection.
                  <a href="{{ '/assets/img/publication_preview/contrastive-hypersphere-framework.png' | relative_url }}" target="_blank" rel="noopener">View full size <span aria-hidden="true">↗</span></a>
                </figcaption>
              </figure>
            </div>
          </div>
        </article>
      </div>

      <h3>What this line of work taught me</h3>
      <p>
        This research taught me to begin with the assumptions that fail at deployment and to reformulate the learning problem around the evidence that remains available. It also showed me why distribution alignment must preserve class separation, and why methods based on pseudo-labels must control the accumulation of their own errors.
      </p>
      <p>
        Linguistic steganalysis and agent memory involve different tasks and methods, but they share a question that continues to shape my research: how can an intelligent system remain reliable when its operating conditions depart from the assumptions available during training or design?
      </p>
    </div>

    <div class="research-overview__section-actions" aria-label="Linguistic steganalysis resources">
      <a class="research-action" href="{{ '/publications/' | relative_url }}">View all publications <span aria-hidden="true">→</span></a>
      <a class="research-action" href="{{ '/research/linguistic-steganalysis/' | relative_url }}">Research summary <span aria-hidden="true">→</span></a>
    </div>

  </section>

  <section class="research-overview__section research-overview__section--compact" aria-labelledby="industry-experience-title">
    <div class="research-overview__section-header">
      <p>04 · Additional experience</p>
      <h2 id="industry-experience-title">Multimodal and multi-turn intent recognition</h2>
    </div>
    <div class="research-overview__section-body research-prose">
      <p>
        During a research internship at Lenovo Research Institute, I studied how multimodal and multi-turn dialogue systems can select relevant context and appropriate reasoning strategies across extended interactions. This experience broadened my interest from model-level prediction toward system-level reliability.
      </p>
      <a class="research-action" href="{{ '/research/intent-recognition/' | relative_url }}">Project summary <span aria-hidden="true">→</span></a>
    </div>
  </section>
</main>
