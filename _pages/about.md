---
layout: about
title: about
permalink: /
subtitle: <a href="https://www.fudan.edu.cn/">Fudan University</a> · M.Eng. in AI · <a href="mailto:meiwangyi@foxmail.com">meiwangyi@foxmail.com</a>

selected_papers: true
social: true

announcements:
  enabled: false

latest_posts:
  enabled: false
---

I'm an M.Eng. student in Artificial Intelligence at Fudan University (2024–2027), advised by Prof. Deqing Yang in the Knowledge Works Lab. My research centers on **reinforcement learning for LLM agents**, with a focus on making open-ended reasoning and long-horizon deep research tasks trainable through **verifiable, structured rewards**.

Currently I work on three threads:

- **Block-level credit assignment** for agentic RL — the [BGPO](https://meiotoufa.github.io/projects/bgpo/) framework re-thinks GRPO at the `(think, toolcall)` block level and reduces training variance by ~17×.
- **Rubric-based verifiable rewards** for deep research — the [DR-Rubric](https://meiotoufa.github.io/projects/dr_rubric/) pipeline auto-generates per-query evaluation rubrics so policy optimization can run without reference answers, and bootstraps the rubric generator from the policy itself.
- **Logical consistency in retrieval** — [NS-IR](https://meiotoufa.github.io/projects/ns_ir/) (ACL 2025) re-ranks candidates by aligning first-order logic between queries and documents, fixing dense retrieval's blind spot for negative constraints.

Outside of academia, I interned at **Xiaohongshu** working on LLM agent post-training (anti-reward-hacking Plan Judges, Deep Research structured rewards), and at a **financial company** building RAG systems for research reports and structured financial data.
