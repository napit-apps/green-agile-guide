---
layout: default
title: CO₂e Emissions per Job
nav_order: 4
parent:  Data & AI
permalink: /metrics-and-impact/data-and-ai/co2e-per-job
---

# CO₂e Emissions per Job

environmental  
{: .label .label-green }

direct  
{: .label .label-purple }

This metric measures the **greenhouse gas emissions produced by a single batch or machine‑learning job**, expressed in grams of CO₂‑equivalent (gCO₂e). It translates compute effort into climate impact by combining energy consumption with the grid carbon intensity of the electricity used in the execution region. This makes emissions from data processing and ML workloads explicit and comparable.

In a Green Agile context, CO₂e Emissions per Job supports **emissions‑aware steering** of Data & AI workloads. While metrics such as Compute Hours per Job focus on efficiency, this metric directly reflects climate impact and highlights the influence of both workload design and hosting location.

## Classification

{: .classification }
>
> - **Category:** Data & AI  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team

## Impact
Tracking emissions per job enables teams to identify which data or ML workloads contribute most to their carbon footprint. A decreasing trend indicates that jobs are executed more climate‑efficiently — either through reduced energy consumption, cleaner electricity, or both. An increasing trend highlights the need to reassess model complexity, job frequency, scheduling, or deployment region.

Because emissions are directly tied to energy use, this metric represents a **direct environmental impact**. It complements Compute Hours per Job by adding a carbon perspective and connects operational decisions to climate outcomes.

## Calculation

CO₂e emissions per job are calculated by multiplying the energy consumed during job execution by the **regional grid carbon intensity**:

$$
\text{CO₂e per Job} =
\text{Energy}_{\text{kWh}} \times \text{Carbon Intensity}_{\text{region}}
$$

where:
- **Energy** is the electricity consumed by the job (in kWh)  
- **Carbon Intensity** is the published grid carbon intensity of the execution region (in gCO₂e/kWh)

A **lower value is better**, indicating lower climate impact per job.

## Example

Assume a machine‑learning training job consumes **25 kWh** of electricity during execution. The job runs in a region with a published grid carbon intensity of **180 gCO₂e/kWh**.

Using the formula:

$$
\text{CO₂e per Job} =
25 \times 180
= 4\,500 \,\text{gCO₂e}
$$

If the same job is optimized to consume **18 kWh**, or is moved to a region with a lower carbon intensity, the emissions per job decrease accordingly. This demonstrates how both **technical optimization** and **region‑aware deployment** contribute to emissions reduction.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/data-and-ai/compute-hours-per-job" style="text-small">← Compute Hours per Job</a>
  <a href="/metrics-and-impact/ux-accessibility-and-frontend-performance" style="text-small">UX, Accessibility & Frontend Performance →</a>
</div>