---
layout: default
title: Software Carbon Intensity (SCI) Score
nav_order: 7
parent: Code, Build & CI/CD
permalink: /metrics-and-impact/code-build-and-cicd/sci
---

# Software Carbon Intensity (SCI) Score

environmental  
{: .label .label-green }

systemic  
{: .label .label-purple }

The Software Carbon Intensity (SCI) Score, defined by the **Green Software Foundation**, measures the **carbon emissions associated with a software system per functional unit (FU)**. The SCI has been standardized as an **ISO standard**, making it the internationally recognized reference for quantifying and comparing the carbon efficiency of software systems.  
More details and the official specification are available from the [Green Software Foundation](https://sci.greensoftware.foundation).

It provides a comparable and transparent metric for understanding the environmental impact of software components across versions, architectures, or deployment environments. Because SCI normalizes emissions by a functional unit, it allows teams to track carbon efficiency independently of workload volume or user growth.

The SCI Score integrates three core elements:
- **E** — the energy consumed by the software  
- **I** — the grid carbon intensity of the electricity used  
- **M** — the embedded (manufacturing) emissions of hardware amortized across its lifetime  

Software with a lower SCI Score is more carbon‑efficient. Tracking SCI across releases enables sustainable architectural decision‑making, supports carbon‑aware prioritization, and makes environmental trade‑offs visible.

{: .classification }
>
> - **Category:** Code, Build & CI/CD  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team (measurement), Product Lead (goal‑setting), Green Agile Coach (enablement)

## Impact
The SCI Score helps teams understand how design choices — such as compute intensity, hosting region, model selection, data handling, or caching — affect the ecological footprint of their software. A decreasing SCI Score indicates that the system is becoming more carbon‑efficient.

By making emissions quantifiable, the metric supports sustainable architecture, carbon‑aware engineering, and responsible scaling. It also enables meaningful comparisons: between services, between releases, and between deployment regions. Because SCI incorporates both operational and embodied emissions, it encourages long‑term thinking and avoids shifting impact elsewhere in the system.

## Embedded Emissions (M)

Embedded emissions describe the **carbon footprint of the hardware** used to run the software, including manufacturing, transport, and end‑of‑life processing. These emissions occur **before the software is executed**, but must be considered to avoid underestimating total impact.

In the SCI context, embedded emissions are typically **amortized over the hardware’s lifetime** and attributed proportionally to workloads (e.g. by CPU hours or capacity share). Even rough estimates help teams avoid shifting emissions from software efficiency gains to excessive or short‑lived hardware usage.

## Calculation

The SCI Score follows the official formula defined by the Green Software Foundation:

$$
\text{SCI} = \frac{(E \times I) + M}{R}
$$

where:
- **E** = energy consumed by the software  
- **I** = grid carbon intensity (gCO₂e per kWh) of the region or provider  
- **M** = embedded emissions of hardware (amortized)  
- **R** = functional unit (e.g., per request, per job, per session)

A **lower SCI is better**, and teams aim for a decreasing trend across releases.

---

## Example

Consider a backend service that processes API requests. During one release cycle, the following values are estimated:

- **Energy consumption (E):** 1 200 kWh  
- **Grid carbon intensity (I):** 180 gCO₂e/kWh  
- **Embedded emissions (M):** 60 000 gCO₂e (amortized share of server manufacturing emissions for this release)  
- **Functional unit (R):** 40 000 API requests  

Using the SCI formula with the measured values inserted directly:

$$
\text{SCI} =
\frac{(1\,200 \,\text{kWh} \times 180 \,\text{gCO₂e/kWh}) + 60\,000 \,\text{gCO₂e}}
{40\,000}
= 6.9 \,\text{gCO₂e per request}
$$

This value represents the average carbon intensity per API request for the current release.  
If the team later improves caching and reduces energy consumption to **900 kWh** while keeping the same functional output, the SCI Score decreases accordingly — demonstrating how efficiency improvements directly reduce carbon intensity per functional unit.

---

<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/code-build-and-cicd/technical-debt-trend" style="text-small">← Technical Debt Trend</a>
  <a href="/metrics-and-impact/data-and-ai" style="text-small">Data & AI →</a>
</div>