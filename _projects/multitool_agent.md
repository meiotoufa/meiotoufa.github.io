---
layout: page
title: Multi-Tool Agent Process Supervision
description: Hierarchical HL/LL agent with tool-graph SFT and failure-aware training
importance: 3
category: research
related_publications: false
---

A **multi-tool agent supervision system** that combines (a) process-level SFT data synthesized from a Tool Graph, (b) failure-trajectory augmentation for robustness, and (c) a hierarchical planner/executor architecture. Final system reaches **0.282 avg accuracy on CRAG Task3 v5**, beating the multi-agent SFT baseline (0.238).

### Process supervision via Tool Graph

Multi-tool agents need to compose tools in a specific dependency order, but prompt-only or skill-based controllers drop steps or mis-order them in long chains. We model the tool-call flow explicitly as a **Tool Graph**, sample graph paths, inject entities, and reverse-generate queries to produce SFT trajectories covering 13 complex question types. The model learns stable tool-combination procedures, reducing reliance on strong-model prompt adherence or hand-crafted rules.

### Failure-aware robustness

Standard multi-tool SFT over-weights successful call chains; the model never sees recovery behavior. We construct failure trajectories across **6 typical error types** — parameter perturbation, schema mismatch, empty return, mis-call, evidence insufficient, path infeasible — each labeled with cause and correction. The model learns to self-check, fall back, and refuse with calibrated abstention.

### Hierarchical HL/LL decoupling

Long-chain multi-tool tasks suffer from interference between high-level planning and low-level tool-call details. We split the system into:
- **Upper-layer Planner Agent (SFT-trained)**: task decomposition, tool-intent selection, stop judgment.
- **Lower-layer Tool Executor (non-trained)**: dispatches sub-goals to SQL / KG / Web Search tool agents in parallel.

End-to-end result: **0.282** average accuracy on CRAG Task3 v5, vs **0.238** for a multi-agent trajectory-synthesis SFT baseline.
