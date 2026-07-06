---
layout: page
title: OpenHLE
description: Open-source benchmark for paper-level physics reasoning (towards Humanity's Last Exam)
importance: 4
category: research
related_publications: false
---

**OpenHLE** is an open-source benchmark targeting *paper-level* physics reasoning — problems that require long-chain symbolic derivation grounded in arXiv theorems. It evaluates whether tool-augmented LLMs can actually solve such problems, or merely retrieve surface-level matches.

### Automated problem synthesis

We design an arXiv-parsing pipeline that extracts **Definitions → Lemmas → Main Theorems** dependency chains and synthesizes 100+ physics derivation problems. Each problem has a unique answer and is time-independent (no factual drift), making the benchmark reproducible and stable.

### Hint-aware difficulty control

Auto-synthesized paper-level problems tend to be either *unanswerable* (no search hit possible) or *trivially answerable* (direct retrieval). We attach layered hints derived from theorem-dependency chains and define answerability via pass@8:

- pass@8 = 0 without hint → *unanswerable*
- pass@8 > 0 with hint → *successfully converted*

On 102 physics problems, ~50% of originally unanswerable samples are converted to answerable with hints.

### Tool-augmented evaluation

We evaluate models under **Direct** and **ToolCall** settings (search / visit / code). On the physics subset:

- ToolCall reduces pass@k=0 share from 49.1% → 29.2%
- But correct answers heavily depend on hitting specific formula line numbers in the source PDF
- Failure modes: long-PDF context misreading, retrieved-fragment misinterpretation, code misuse

**Takeaway**: tool augmentation does *not* reliably solve paper-level physics derivation — the benchmark exposes a real capability gap.
