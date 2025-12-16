---
layout: default
title: ADR-Light Coverage
nav_order: 1
parent: Architecture & Infrastructure
permalink: /metrics-and-impact/architecture-and-infrastructure/adr-light-coverage
---

# ADR-Light Coverage

governance  
{: .label .label-green }

systemic
{: .label .label-purple }

This metric measures the **percentage of significant architecture and data decisions** that are documented using **ADR-Light**, a lightweight and structured decision record format. A high coverage improves **traceability**, strengthens **team alignment**, and supports **sustainable architectural evolution** by ensuring that critical decisions are explicit, reviewable, and transparent over time.

ADR-Light captures the context, reasoning, alternatives, and expected impact of a decision, helping teams understand trade-offs and maintain long-term system health. By documenting decisions clearly, teams reduce architectural drift, avoid knowledge silos, and ensure continuity in decision-making. This supports sustainable system evolution and aligns with Green Agile principles such as **Value Focus**, **Lean**, **Flow**, **Transparency**, and **Systems Thinking**.

{: .classification }
>
> - **Category:** Architecture & Infrastructure  
> - **Measurement Frequency:** per iteration  
> - **Responsibility:** Engineering Team (primary), Product Lead (strategic alignment), Green Agile Coach (enablement)

## Impact
This metric improves architectural sustainability by ensuring that important decisions are not implicit but **explicitly documented**. It supports long-term maintainability, reduces rework, prevents architectural drift, and creates organizational clarity. By capturing reasoning and trade-offs, it helps teams make more deliberate architecture choices aligned with ecological, economic, and social sustainability goals.

## Calculation
 
$$
\frac{\text{Decisions documented with ADR-Light}}{\text{All significant architecture or data decisions}} \times 100
$$

The metric is calculated by dividing the number of significant architectural or data decisions documented using ADR-Light by the total number of such decisions within the iteration. The result is multiplied by **100** to represent the coverage as a percentage. Teams should aim for **≥ 80% coverage**, ensuring that most important decisions are captured while allowing flexibility where documentation adds limited value.

## Example

During an iteration, the engineering team makes a total of **10 significant architectural or data decisions** — for example, selecting a caching strategy, defining service boundaries, choosing an indexing approach, or setting data retention rules. Out of these 10 decisions, **8 are documented using ADR-Light**.

Using the formula:

$$
\frac{8}{10} \times 100 = 80\%
$$

The ADR-Light Coverage for this iteration is **80%**, which meets the recommended target. This demonstrates that most important decisions are explicit, reviewable, and transparent, while still allowing flexibility for low-impact decisions that do not require formal documentation.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/architecture-and-infrastructure" style="text-small">← Architecture & Infrastructure</a>
  <a href="/metrics-and-impact/architecture-and-infrastructure/pue-per-region" style="text-small">Power Usage Effectiveness (PUE) per Region →</a>
</div>