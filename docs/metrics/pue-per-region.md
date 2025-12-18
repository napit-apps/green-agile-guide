---
layout: default
title: Power Usage Effectiveness (PUE) per Region
nav_order: 2
parent: Architecture & Infrastructure
permalink: /metrics-and-impact/architecture-and-infrastructure/pue-per-region
---

# Power Usage Effectiveness (PUE) per Region

environmental  
{: .label .label-green }

governance  
{: .label .label-green }

systemic  
{: .label .label-purple }

direct  
{: .label .label-purple }


This metric captures the **Power Usage Effectiveness (PUE)** of the data center region in which a workload operates. PUE is an industry‑standard measure that reflects how efficiently a data center uses energy by comparing the **total facility energy consumption** with the **energy delivered to IT equipment**. **A lower PUE indicates** that more of the consumed electricity powers compute resources instead of cooling, lighting, or other facility overhead.

This makes PUE highly relevant for sustainable infrastructure choices, as identical workloads can have **substantially different environmental impacts** depending on the region in which they run.

By tracking PUE, teams gain insight into the **efficiency characteristics** of their hosting region and can make more conscious decisions about where to operate their systems. Cloud providers publish PUE values for their regions, allowing teams to document the efficiency of their infrastructure without needing to calculate PUE themselves.

A region with a low PUE reduces the indirect ecological footprint of workloads and can also influence cost efficiency.

While regulatory and latency requirements may constrain region choice, aiming for regions with a PUE of **below 1.3** generally supports more sustainable architecture. The metric thus supports Green Agile principles such as **Energy Efficiency**, **Impact Transparency**, **Sustainable Architecture**, and **Continuous Learning**, by making **infrastructure sustainability visible and actionable**.

## Classification

{: .classification }
>
> - **Category:** Architecture & Infrastructure  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Product Lead (region selection), Engineering Team (documentation), Green Agile Coach (enablement)

## Impact
Tracking PUE supports teams in selecting **energy‑efficient regions** and understanding the **infrastructure‑level sustainability impact** of their hosting choices. It exposes differences in regional data center performance, encourages migration to **more efficient regions** where feasible, and makes sustainability considerations explicit during architectural planning. The metric helps reveal whether infrastructure decisions align with ecological and economic sustainability goals and ensures that regional efficiency becomes a recurring part of release planning.

## Calculation

$$
\text{PUE} = \frac{\text{Total data center energy consumption}}{\text{Energy delivered to IT equipment}}
$$

PUE is published by cloud providers and not computed by the team. The metric requires documenting the PUE value of the region in which the workload operates for each release. A lower value indicates higher efficiency and contributes to reducing the environmental impact of compute operations.

## Example

Imagine a team is evaluating the efficiency of the region in which their workload operates.  
The cloud provider does **not** publish the raw facility energy values, but instead provides the **calculated PUE** for the region based on its internal reporting.


For the current release cycle, the provider reports:

Internally, this value is derived by the provider using:

$$
\text{PUE} = \frac{130\ \text{MWh (total facility energy)}}{100\ \text{MWh (energy delivered to IT equipment)}} = \mathbf{1.30}
$$

Although the provider normally does not expose these raw values publicly, this calculation illustrates how the reported PUE is obtained.

the team understands that for every 1 unit of energy used for compute, an additional 0.30 units are consumed for cooling, power distribution, and other overhead.

If another available region (Region B) reports a **PUE of 1.15**, migrating the workload could meaningfully **reduce indirect energy overhead** — even though the workload itself remains unchanged. This makes PUE a **valuable metric** for evaluating and improving infrastructure sustainability.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/architecture-and-infrastructure/adr-light-coverage" style="text-small">← ADR-Light Coverage</a>
  <a href="/metrics-and-impact/architecture-and-infrastructure/grid-carbon-intensity" style="text-small">Grid Carbon Intensity →</a>
</div>