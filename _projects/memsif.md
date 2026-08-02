---
layout: page
title: MemSIF — Long-Horizon Memory for LLM Agents
description: Structuring interaction histories and maintaining facts with different temporal and utility profiles.
importance: 1
permalink: /research/memsif/
---

## Research Question

Long-horizon agents accumulate interaction histories in which useful evidence is often fragmented across time. Information that appears unimportant when it is first observed may also become valuable only after a later query. These properties make it difficult for a memory system to decide how interactions should be organized and what should be retained.

## Approach

MemSIF organizes raw interactions into **Structured Interaction Memory**, using complementary views of the interaction history to preserve both topical context and event development. It then maintains a **Dual-Track Fact Memory**: CoreFact supports stable consolidation, while ActiveFact enables query-driven activation of facts whose utility may emerge later.

This work studies how memory structure and retrieval-time reasoning can help LLM agents use experience more reliably over extended interactions.

## Publication

Preprint details are forthcoming. See the current manuscript entry on the [Publications page](/publications/).
