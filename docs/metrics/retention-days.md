---
layout: default
title: Retention Days
nav_order: 2
parent:  Data & AI
permalink: /metrics-and-impact/data-and-ai/retention-days
---

# Retention Days (Weighted)

environmental  
{: .label .label-green }
governance  
{: .label .label-green }

systemic  
{: .label .label-purple }

This metric measures the **effective data retention duration across data domains**, expressed as a weighted average of how long different data volumes are stored. It makes visible how long data is kept in practice — not just what retention policies define — and supports data minimization by highlighting long-lived or over-retained datasets.

In a Green Agile context, Retention Days helps teams balance **compliance requirements**, business value, and sustainability. Retaining data longer than necessary increases storage footprint, backup volume, operational complexity, and long-term environmental impact. Tracking effective retention duration enables informed decisions about deletion, aggregation, anonymization, or tiered storage.

## Classification

{: .classification }
>
> - **Category:** Data & AI  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team

## Impact
Monitoring retention days supports sustainable data lifecycle management. High or increasing retention values may indicate missing deletion processes, overly conservative defaults, or unclear ownership of data domains. Reducing retention duration — while remaining compliant — lowers storage demand, reduces long-term energy consumption, and simplifies data governance.

Because retention decisions are influenced by regulatory constraints, product strategy, and user expectations, this metric reflects a **systemic impact** across processes, teams, and long-term system behavior.

## Calculation

Retention Days are calculated as a **weighted average** based on data volume per domain:

$$
\text{Retention Days} =
\frac{\sum (V_i \times D_i)}{\sum V_i}
$$

where:
- \(V_i\) = data volume of domain *i*  
- \(D_i\) = retention duration (in days) of domain *i*  

A **lower value is better**, as long as legal, regulatory, and business requirements are met.

## Example

Assume a system stores data in three domains:

- User profiles: 100 GB retained for 1 095 days (3 years)  
- Transaction logs: 300 GB retained for 365 days (1 year)  
- Debug logs: 50 GB retained for 30 days  

The weighted retention is:

$$
\frac{(100 \times 1\,095) + (300 \times 365) + (50 \times 30)}
{100 + 300 + 50}
=
\frac{219\,500}{450}
\approx 488 \,\text{days}
$$

This result shows that most data is retained for well over a year on average. The team may explore shortening retention for low-value data (e.g. logs) or aggregating historical records to reduce long-term footprint while staying compliant.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/data-and-ai/data-volume" style="text-small">← Data Volume</a>
  <a href="/metrics-and-impact/data-and-ai/compute-hours-per-job" style="text-small">Compute Hours per Job →</a>
</div>