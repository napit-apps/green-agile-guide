---
layout: default
title: CPU Time per Transaction
nav_order: 2
parent: Operations & Observability
permalink: /metrics-and-impact/operations-and-observability/cpu-time-per-transaction
---

# CPU Time per Transaction

environmental  
{: .label .label-green }

governance  
{: .label .label-green }

direct  
{: .label .label-purple }

systemic  
{: .label .label-purple }

This metric measures the **average CPU time consumed per transaction**, expressed in CPU milliseconds. It makes visible how much processing effort is required to handle a single business transaction and helps identify runtime inefficiencies and performance hotspots in production systems.

In a Green Agile context, CPU Time per Transaction links **runtime efficiency, operational sustainability, and system scalability**. High CPU usage per transaction often indicates inefficient code paths, expensive database operations, or missing caching, all of which increase energy consumption and infrastructure demand.

## Classification

{: .classification }
>
> - **Category:** Operations & Observability  
> - **Measurement Frequency:** per iteration  
> - **Responsibility:** Engineering Team

## Impact
Tracking CPU time per transaction enables teams to pinpoint **hotspots in runtime behavior** that disproportionately consume compute resources. A decreasing trend indicates that transactions are processed more efficiently, reducing energy use and allowing systems to scale with lower infrastructure overhead. An increasing trend highlights regressions that may lead to higher operational costs and environmental impact.

Because this metric directly measures compute usage during real transactions, it represents a **direct environmental impact**. At the same time, it supports governance by providing a factual basis for prioritizing performance optimizations and architectural improvements.

## Calculation

CPU Time per Transaction is calculated as the **average CPU time per processed transaction**:

$$
\text{CPU Time per Transaction} =
\frac{\sum \text{CPU Time (ms)}}{\text{Number of Transactions}}
$$

Teams should define clearly which transaction types are included and ensure consistent measurement across iterations. A **falling trend** is the desired direction.

## Example

Assume monitoring data shows a total of **48,000 ms of CPU time** consumed while processing **1,200 transactions** during an iteration.

Using the formula:

$$
\frac{48\,000}{1\,200} = 40 \text{ ms per transaction}
$$

If a subsequent iteration reduces this value to **28 ms per transaction** through query optimization or improved caching, the metric confirms reduced runtime overhead and improved operational efficiency.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/operations-and-observability/compute-per-deploy" style="text-small">← Compute Time per Deployment</a>
  <a href="/metrics-and-impact/operations-and-observability/cache-hit-rate" style="text-small">Cache Hit Rate →</a>
</div>