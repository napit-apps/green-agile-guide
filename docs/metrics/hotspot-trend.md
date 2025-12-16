---
layout: default
title: Hotspot Trend
nav_order: 5
parent: Code, Build & CI/CD
permalink: /metrics-and-impact/code-build-and-cicd/hotspot-trend
---

# Hotspot Trend

environmental  
{: .label .label-green }

governance  
{: .label .label-green }

systemic  
{: .label .label-purple }

This metric tracks the **development of efficiency and sustainability hotspots over time**, focusing on whether identified problem areas are being systematically reduced or continue to accumulate. Hotspots may include inefficient code paths, energy‑intensive jobs, oversized infrastructure components, or process bottlenecks in the delivery pipeline.

In a Green Agile context, the Hotspot Trend shifts attention from isolated optimizations to **continuous improvement at system level**. It encourages teams to not only identify hotspots, but also to actively close them and prevent new ones from emerging unnoticed.

{: .classification }
>
> - **Category:** Code, Build & CI/CD  
> - **Measurement Frequency:** per iteration  
> - **Responsibility:** Engineering Team

## Impact
A falling Hotspot Trend indicates that teams are effectively addressing known inefficiencies and reducing the overall sustainability risk of the system. A rising trend suggests that new hotspots are being created faster than existing ones are resolved, pointing to structural issues in architecture, processes, or prioritization.

Because hotspots typically span multiple components, teams, or pipeline stages, this metric represents a **systemic impact**. It supports governance by making continuous improvement visible and by highlighting whether sustainability work keeps pace with ongoing development.

## Calculation

The Hotspot Trend is calculated as the **difference between open and closed hotspots within an iteration**:

$$
\text{Hotspot Trend} =
\text{Number}_{\text{open}} -
\text{Number}_{\text{closed}}
$$

A **negative or decreasing value** indicates progress, as more hotspots are being resolved than created. A positive value signals accumulating inefficiencies that require attention.

## Example

Assume that during one iteration:

- 6 new efficiency hotspots are identified  
- 10 existing hotspots are resolved  

The Hotspot Trend is:

$$
6 - 10 = -4
$$

This negative result shows that the team reduced the overall number of hotspots. If future iterations show a positive trend, teams may need to invest more deliberately in refactoring, process improvements, or architectural cleanup.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/code-build-and-cicd/cicd-resources-per-change" style="text-small">← CI/CD Resources per Change</a>
  <a href="/metrics-and-impact/code-build-and-cicd/energy-per-transaction-or-job" style="text-small">Energy per Compute per Transaction or Job →</a>
</div>