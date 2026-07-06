---
layout: page
title: BGPO
description: Block-level geometric policy optimization for deep research agents (EMNLP Under Review)
importance: 2
category: research
related_publications: true
---

**BGPO (Block-wise Geometric Policy Optimization)** re-thinks credit assignment in agentic RL by treating each `(think, toolcall)` assistant turn as a minimal semantic decision block. Length is normalized within a block; blocks are aggregated with equal geometric weights across turns. Credit now flows by *research decision* rather than token length.

### Why it matters

In long-horizon web-agent / deep-research trajectories, GRPO and DAPO assign credit per token, so a few long reasoning tokens dominate the gradient. This produces high ratio variance, frequent clipping, and unstable updates. BGPO eliminates both issues by changing the aggregation unit.

### Key results

- **Training stability**: ratio variance drops ~17× vs GRPO/DAPO; clip events essentially vanish.
- **Minimax optimality**: we prove block-equal aggregation is first-order optimal under heteroscedastic policy gradient variance, strictly better than token-level and sequence-level objectives.
- **Performance**: 7B Qwen2.5 + BGPO averages 0.708 across 7 QA tasks (vs 0.664 for Search-R1-7B); 14B reaches 0.767. With fixed prior, BGPO attains 0.527/0.395 EM/F1, beating DAPO and GRPO, and leads on BrowseComp+, HoVer, SealQA.
- **Prior-guided warm start**: a hybrid action space (decomposition, keyword extraction, synonym replacement, HyDE, rewrite_by_myself) is seeded with human priors, then BGPO learns the action composition from environment feedback. Controlled attribution shows prior and optimizer contribute complementarily.

### My role

First author. Proposed the block-level geometric aggregation, proved the variance bound, implemented the trainer, and ran all evaluations.

{% cite mei2025bgpo %}
