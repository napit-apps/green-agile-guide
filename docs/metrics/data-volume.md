---
layout: default
title: Data Volume
nav_order: 1
parent:  Data & AI
permalink: /metrics-and-impact/data-and-ai/data-volume
---

# Data Volume (GB)

environmental  
{: .label .label-green }
governance  
{: .label .label-green }

systemic
{: .label .label-purple }

This metric measures the **total volume of data stored for a product or system**, expressed in gigabytes. It captures how much persistent data is retained across databases, object storage, file systems, and other relevant data stores. Data volume is a foundational sustainability indicator because stored data continuously consumes resources through storage infrastructure, replication, backups, and long‑term maintenance.

For Green Agile, Data Volume makes the often invisible impact of data accumulation explicit. Growing data volumes increase energy consumption, storage costs, operational complexity, and long‑term environmental footprint. Tracking this metric enables teams to identify unnecessary data growth, validate data‑minimization strategies, and make informed decisions about retention, compression, aggregation, and deletion.

## Classification

{: .classification }
>
> - **Category:** Data & AI  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team

## Impact
Monitoring data volume supports sustainable data practices by revealing how storage footprint evolves over time. A continuously increasing data volume may indicate missing retention policies, overly verbose logging, redundant datasets, or uncontrolled feature growth. Reducing or stabilizing data volume lowers energy use in storage systems, decreases backup and replication overhead, and improves system maintainability.

Because data volume is influenced by product decisions, user behavior, and regulatory requirements, this metric reflects **indirect environmental impact**. It provides an essential baseline for related metrics such as Retention Days, Compute Hours per Job, and CO₂e Emissions per Job.

## Calculation

Data Volume is calculated as the **sum of all stored data** relevant to the product or system:

$$
\text{Data Volume (GB)} = \sum \text{Stored Data across relevant systems}
$$

This includes, for example:
- production databases  
- data lakes and object storage  
- backups and replicas (if in scope)  
- long‑lived logs and telemetry data  

Teams should clearly define the system boundary to ensure consistent measurement across releases. A **stable or decreasing trend** is generally desirable, taking compliance and business requirements into account.

## Example

Assume a product stores data in the following systems at the end of a release:

- Relational database: 420 GB  
- Object storage (user uploads): 260 GB  
- Log archive: 120 GB  

The total data volume is:

$$
420 + 260 + 120 = 800 \,\text{GB}
$$

If the previous release reported **950 GB**, the decrease indicates that data cleanup, retention limits, or aggregation measures were effective in reducing storage footprint.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/data-and-ai" style="text-small">← Data & AI</a>
  <a href="/metrics-and-impact/data-and-ai/retention-days" style="text-small">Retention Days →</a>
</div>