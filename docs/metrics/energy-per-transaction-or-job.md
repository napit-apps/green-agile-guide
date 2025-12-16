---
layout: default
title: Energy per Compute per Transaction or Job
nav_order: 6
parent: Code, Build & CI/CD
permalink: /metrics-and-impact/code-build-and-cicd/energy-per-transaction-or-job
---

# Energy per Compute per Transaction or Job

environmental  
{: .label .label-green }

direct  
{: .label .label-purple }

This metric measures the **energy consumption or compute effort required per business transaction or batch job**. It makes visible how efficiently a system converts compute resources into delivered functionality. By normalizing energy or compute usage to a functional unit (such as a transaction, request, or job), the metric enables meaningful comparisons across releases, workloads, and architectural variants.

Energy / Compute per Transaction or Job is a core efficiency metric for Green Agile, as it directly reflects how design and implementation choices translate into ecological impact. Improvements in this metric indicate that the system delivers the same value with fewer resources, while regressions point to hidden inefficiencies that increase energy use and emissions.

{: .classification }
>
> - **Category:** Code, Build & CI/CD  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team (measurement and optimization), Product Lead (prioritization)

## Impact
Tracking energy or compute usage per transaction or job supports **direct ecological impact reduction** by identifying inefficient code paths, oversized resource allocations, or suboptimal algorithms. A decreasing trend means that the system performs its core business functions more efficiently, reducing energy demand and associated emissions without sacrificing functionality.

This metric also supports continuous efficiency steering. By monitoring changes over time, teams can assess whether new features, refactorings, or infrastructure changes improve or degrade resource efficiency. It complements higher-level metrics such as SCI by providing a **granular, actionable view** on where energy and compute are actually consumed.

## Calculation

The metric can be expressed using either direct energy measurements or compute-based proxies, depending on data availability.

When energy data is available:

$$
\text{Energy per Txn/Job} =
\frac{\text{Total Energy Consumption (kWh)}}{\text{Number of Transactions or Jobs}}
$$

When energy measurements are not available, compute effort can be used as a proxy:

$$
\text{Compute per Txn/Job} =
\frac{\text{Total CPU Time (seconds)}}{\text{Number of Transactions or Jobs}}
$$

A **lower value is better**. Teams aim for a decreasing trend across releases, while ensuring that correctness, performance, and reliability are not compromised.

## Example

Consider an API-based service that processes customer requests. During one release cycle, monitoring shows the following values:

- **Total energy consumption:** 480 kWh  
- **Number of processed transactions:** 120 000 requests  

Using the energy-based formula:

$$
\text{Energy per Transaction} =
\frac{480 \,\text{kWh}}{120\,000}
= 0.004 \,\text{kWh per transaction}
$$

This means that each request consumes, on average, **4 Wh** of energy.

If direct energy measurements are not available, the team can use compute time as a proxy. For the same release, the service records:

- **Total CPU time:** 9 600 seconds  
- **Number of processed transactions:** 120 000 requests  

$$
\text{Compute per Transaction} =
\frac{9\,600 \,\text{s}}{120\,000}
= 0.08 \,\text{s per transaction}
$$

In the next release, after optimizing database queries and introducing caching, both energy consumption and CPU time per transaction decrease. This confirms that the system delivers the same functionality with fewer resources — a direct improvement in ecological efficiency.

---

<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/code-build-and-cicd/sci" style="text-small">← Software Carbon Intensity (SCI) Score</a>
  <a href="/metrics-and-impact/code-build-and-cicd/sci" style="text-small">Software Carbon Intensity (SCI) Score →</a>
</div>