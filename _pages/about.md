---
layout: about
title: Home
permalink: /
nav: true
nav_order: 1
subtitle: Reliable Long-Horizon LLM Agents · Structured Memory · Experience Reuse

profile:
  align: right
  # image: prof_pic.jpg  # TODO: add photo
  image_circular: true # crops the image to make it circular
  more_info: >
    <p>luoyf@bupt.edu.cn</p>
    <p>Beijing, China</p>

selected_papers: false # rendered explicitly below so the section title stays site-controlled
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # enable after there is a verified public update to share
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false # TODO: enable when blog content is ready
  scrollable: true
  limit: 3
---

I study how to build reliable LLM agents for long-horizon tasks. My research focuses on external mechanisms—including structured memory, execution-state modeling, and experience reuse—that help agents preserve task-relevant information and act consistently across extended interactions.

My current work, [MemSIF](/research/memsif/), investigates how long-term interaction histories can be transformed into structured representations and query-adaptive fact memories. Previously, I developed robust learning methods for linguistic steganalysis under distribution shift and worked on multimodal and multi-turn intent recognition at Lenovo Research. I completed an M.S. in Cyberspace Security at Beijing University of Posts and Telecommunications and am seeking Ph.D. opportunities beginning in Fall 2027.

## Research Interests

- **Reliable long-horizon LLM agents:** maintaining coherent behavior across extended tasks and interactions.
- **Structured memory and stateful execution:** preserving relevant facts, context, and execution progress.
- **Experience reuse and skill acquisition:** turning prior interactions into reusable knowledge and capabilities.

## Selected Publications

{% include selected_papers.liquid %}
