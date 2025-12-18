---
layout: default
title: Energy Consumption per Release
nav_order: 4
parent: Operations & Observability
permalink: /metrics-and-impact/operations-and-observability/energy-per-release
---

# Energy Consumption per Release (kWh)

environmental  
{: .label .label-green }

governance  
{: .label .label-green }

systemic  
{: .label .label-purple }

This metric estimates the **energy consumption caused by new or changed workloads introduced with a release**, expressed in kilowatt-hours (kWh). It makes the energy impact of deployment and operational changes visible at release level instead of focusing only on individual transactions or components.

In a Green Agile context, Energy Consumption per Release supports **energy-aware delivery decisions**. By aggregating the expected runtime energy demand of new features, infrastructure changes, or configuration updates, teams gain a holistic view of how releases influence the overall energy footprint of a system.

## Classification

{: .classification }
>
> - **Category:** Operations & Observability  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team

## Impact
Tracking energy consumption per release enables teams to assess whether new functionality increases or reduces the system’s operational energy footprint. A falling trend indicates that efficiency improvements, architectural optimizations, or cleaner infrastructure choices outweigh added workload. A rising trend highlights releases that introduce significant additional energy demand and may require explicit justification or mitigation measures.

Because this metric aggregates effects across multiple components and runtime behaviors, it represents a **systemic impact**. It supports governance by enabling release-level trade-offs between functionality, performance, and sustainability goals.

## Calculation

Energy Consumption per Release is estimated using the following formula:

$$
\text{Energy per Release (kWh)} =
(\text{Compute Time} \times \text{Effective Power Consumption}) \times \text{PUE}
$$

Where:
- **Compute Time** represents the aggregated runtime of new or changed workloads  
- **Effective Power Consumption** reflects the average power draw of the compute resources  
- **PUE (Power Usage Effectiveness)** accounts for data center overhead

Teams should document assumptions and system boundaries consistently to ensure comparability across releases. A **falling trend** is the desired direction.

## Example

Assume a release introduces a new background job and modifies an existing service, resulting in an estimated **120 compute-hours** per day. The average effective power consumption is **0.35 kW**, and the hosting region has a **PUE of 1.4**.

The estimated energy consumption per day is:

$$
(120 \times 0.35) \times 1.4 = 58.8 \text{ kWh}
$$

If a later release reduces compute time or improves efficiency, this value decreases, indicating a lower operational energy footprint for the system.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/operations-and-observability/cache-hit-rate" style="text-small">← Cache Hit Rate</a>
  <a href="/metrics-and-impact/governance-reporting-and-compliance" style="text-small">Governance, Reporting & Compliance →</a>
</div>