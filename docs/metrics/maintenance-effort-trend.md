---
layout: default
title: Maintenance Effort Trend
nav_order: 5
parent: Governance, Reporting & Compliance
permalink: /metrics-and-impact/governance-reporting-and-compliance/maintenance-effort-trend
---

# Maintenance Effort Trend

governance  
{: .label .label-green }

environmental  
{: .label .label-green }

systemic  
{: .label .label-purple }

This metric tracks the **trend of maintenance and fixing effort per release**, expressed as the total number of hours spent on corrective and preventive maintenance activities. It makes visible how sustainable a system is to operate and evolve over time.

In a Green Agile context, the Maintenance Effort Trend links **technical quality, long-term maintainability, and economic sustainability**. Rising maintenance effort often signals accumulating technical debt, architectural erosion, or insufficient automation, while a falling trend indicates improving code health and more sustainable delivery practices.

## Classification

{: .classification }
>
> - **Category:** Governance, Reporting & Compliance  
> - **Measurement Frequency:** per release  
> - **Responsibility:**  
>   - **Engineering Team:** measurement  
>   - **Product Lead:** steering and prioritization

## Impact
A decreasing maintenance effort trend indicates that systems become easier and cheaper to maintain, freeing capacity for value-adding work. An increasing trend highlights growing operational friction and long-term risk, as more effort is required to keep the system stable and functional.

Because maintenance effort accumulates across releases and teams, this metric represents a **systemic impact**. It supports governance by enabling informed trade-offs between feature delivery, refactoring, and long-term sustainability of the product.

## Calculation

The Maintenance Effort Trend is calculated as the **change in maintenance effort compared to the previous release**:

$$
\Delta \text{Maintenance Effort} =
\text{Maintenance Hours}_{\text{current release}} -
\text{Maintenance Hours}_{\text{previous release}}
$$

Maintenance hours typically include bug fixing, refactoring, corrective actions, and routine upkeep tasks. The desired direction is a **falling trend** over time.

## Example

Assume the following maintenance effort was recorded:

- Previous release: 180 hours  
- Current release: 140 hours  

The change is:

$$
140 - 180 = -40 \text{ hours}
$$

This negative delta indicates an improvement in maintainability. If future releases show increasing maintenance effort, teams can use this metric to justify refactoring, architectural improvements, or process changes.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/governance-reporting-and-compliance/tco-estimation" style="text-small">← Total Cost of Ownership (TCO)</a>
  <a href="/metrics-and-impact/" style="text-small">Metrics & Impact →</a>
</div>