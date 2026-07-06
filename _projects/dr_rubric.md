---
layout: page
title: DR-Rubric
description: Verifiable rubric-based reward for deep research RL (NeurIPS Under Review)
importance: 1
category: research
related_publications: true
---

**DR-Rubric** is a reward construction framework that makes RL trainable on open-ended reasoning and long-form generation tasks where no reference answer exists. The key idea: split reward design into two stages — *task-relevant fact collection* followed by *fine-grained rubric generation* — and auto-generate per-query evaluation criteria that plug into GRPO.

### Why it matters

Open-ended tasks (agentic deep research, expert reasoning) cannot be verified by string match or scalar reward. Existing approaches either rely on expensive frontier-model judges or coarse generic rubrics. DR-Rubric synthesizes task-specific rubrics from agentic search evidence, providing a dense, decomposable reward signal.

### Key results

- **Sample efficiency**: 8B model trained on only 1K–3K rubric-based RL instances matches or beats baselines trained on 16K–90K instances. On agentic research and expert reasoning benchmarks, relative gains reach +3.8 / +3.2 and +3.7 / +1.5.
- **Self-bootstrapping**: the trained policy itself takes over evidence collection and rubric synthesis, eliminating the dependence on frontier models. We track multi-round bootstrap dynamics and identify a *reasoning specialization → task rebalancing* capability migration.
- **Reward polarization diagnostic**: on a 30B-A3B run we define a metric that captures reward concentrating toward a few high-confidence modes; it predicts subsequent agentic score decline, enabling early stopping and data filtering.

### My role

First author. Designed the rubric construction pipeline, ran all RL/bootstrapping experiments, and wrote the paper.

{% cite mei2025drrubric %}
