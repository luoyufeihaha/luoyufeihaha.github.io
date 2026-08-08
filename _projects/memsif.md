---
layout: page
title: MemSIF — Long-Horizon Memory for LLM Agents
description: Structured interaction-to-fact memory for reliable long-horizon LLM agents.
importance: 1
permalink: /research/memsif/
---

## Research Question

Long-horizon agents accumulate interaction histories in which useful evidence is often fragmented across time. Temporally adjacent turns may be unrelated, while evidence about the same event may recur much later. Information that appears unimportant when it is first observed may also become valuable only after a future query.

MemSIF characterizes these challenges as **Temporal–Structural Misalignment (TSM)** and **Delayed Utility Manifestation (DUM)**.

## Approach

MemSIF organizes raw interactions into **Structured Interaction Memory**. Topical Segments preserve local topical coherence, while Event Trajectories connect related evidence distributed across time.

It then maintains a **Dual-Track Fact Memory**. CoreFact consolidates stable, schema-guided information at write time; ActiveFact forms candidate facts when their utility emerges through queries and promotes repeatedly supported candidates for future reuse.

## Results

Across LoCoMo and LongMemEval-S with five backbone LLMs, MemSIF achieves the highest Total ACC in every evaluated setting. It outperforms the strongest baseline by 2.29%–8.79% on LoCoMo and 2.87%–6.15% on LongMemEval-S.

## Publication

**MemSIF: From Structured Interactions to Dual-Track Fact Memory for LLM Agents**

Yufei Luo, Xiucheng Xu, and Zhen Yang. arXiv preprint, 2026.

[arXiv](https://arxiv.org/abs/2608.01742) · [PDF](https://arxiv.org/pdf/2608.01742) · [Code](https://github.com/luoyufeihaha/MemSIF) · [All publications](/publications/)
