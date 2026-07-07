---
layout: about
title: about
permalink: /
subtitle: <a href="https://www.fudan.edu.cn/">Fudan University</a> · M.Eng. in AI · <a href="mailto:meiwangyi@foxmail.com">meiwangyi@foxmail.com</a>

profile:
  align: right
  image_circular: false
  more_info: >
    <p>Knowledge Works Lab</p>
    <p>Fudan University, Shanghai</p>

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

From Nov 2025 I've been a **LLM Agent post-training intern at Xiaohongshu**, building anti-reward-hacking Plan Judges and the Deep Research structured reward pipeline. Before that I spent two years at Lanzhong Asset Management as an AI engineer intern, where I built a multi-service financial RAG system and an automated US-equity growth-scoring pipeline.

Beyond research, I led [OpenHLE](https://meiotoufa.github.io/projects/openhle/), a benchmark of paper-level physics reasoning problems auto-synthesized from arXiv, and a multi-tool agent system with hierarchical HL/LL decoupling + failure-aware SFT that scored 0.282 on CRAG Task3 v5.

I read papers, write RL training code (Verl / LlamaFactory), and occasionally do Kaggle on the side — once top 18% on a high-frequency futures forecasting competition.
