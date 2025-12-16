---
layout: default
title: Compute Time per Deployment
nav_order: 1
parent: Operations & Observability
permalink: /metrics-and-impact/operations-and-observability/compute-per-deploy
---

# Compute Time per Deployment

environmental  
{: .label .label-green }

governance  
{: .label .label-green }

direct  
{: .label .label-purple }

This metric measures the **total compute time consumed during a deployment**, expressed as aggregated CPU time across all deployment steps. It captures how resource‑intensive the delivery process is and makes operational overhead during releases visible.

In a Green Agile context, Compute Time per Deployment connects **delivery efficiency with operational sustainability**. Frequent or inefficient deployments can silently consume significant compute resources through build steps, infrastructure provisioning, migrations, and verification tasks. Making this effort explicit supports conscious trade‑offs between deployment frequency, automation, and resource usage.

## Classification

{: .classification }
>
> - **Category:** Operations & Observability  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team

## Impact
Tracking compute time per deployment helps teams understand the **operational cost of delivery**. A decreasing trend indicates more efficient deployment pipelines, better automation, and reduced overhead. An increasing trend may point to overly complex deployment processes, redundant checks, or inefficient infrastructure operations.

Because this metric measures compute consumption directly caused by deployment activities, it represents a **direct environmental impact**. At the same time, it acts as a governance lever by encouraging teams to design lean, reliable, and energy‑aware delivery processes.

## Calculation

Compute Time per Deployment is calculated as the **sum of CPU time consumed by all deployment steps**:

$$
\text{Compute Time per Deployment} =
\sum \text{CPU Time of all deployment steps}
$$

Teams should define clearly which steps are included (e.g. infrastructure provisioning, configuration, migrations, smoke tests) to ensure consistent measurement across releases. A **falling trend** is the desired direction.

## Example

Assume a deployment consists of the following steps:

- Infrastructure provisioning: 420 CPU‑seconds  
- Application rollout: 310 CPU‑seconds  
- Database migration: 180 CPU‑seconds  
- Post‑deployment checks: 90 CPU‑seconds  

The total compute time for the deployment is:

$$
420 + 310 + 180 + 90 = 1\,000 \text{ CPU‑seconds}
$$

If subsequent releases reduce this value through streamlined pipelines or improved automation, the metric confirms improved delivery efficiency and lower operational resource consumption.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/operations-and-observability" style="text-small">← Operations & Observability</a>
  <a href="/metrics-and-impact/operations-and-observability/cpu-time-per-transaction" style="text-small">CPU Time per Transaction →</a>
</div>