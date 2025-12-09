---
layout: default
title: Percentage of Backlog Items with Impact Block
nav_order: 1
parent: Product Management
permalink: /metrics/product-management/percentage-of-backlog-items-with-impact-block
math: katex
---

# Percentage of Backlog Items with Impact Block
ecological
{: .label .label-green }
economic
{: .label .label-green }
social
{: .label .label-green }
direct 
{: .label .label-purple }
indirect 
{: .label .label-purple }

This metric shows the **percentage of backlog items** that contain a fully completed Impact Block. By making the intended **ecological, economic, and social effects** of each item explicit, it strengthens **transparency** and supports **value‑based prioritization** throughout the Green Agile workflow. A high coverage ensures that both **direct and indirect sustainability impacts** are identified early, enabling more informed decisions during planning, refinement, and delivery.

Each Impact Block specifies:
- **the effect type** (direct or indirect)  
- **the sustainability dimensions** involved (ecological, economic, and/or social)  
- **the selected metric**, including its **baseline and target**  
- **the verification method** that will be used to measure and validate the outcome  

A high coverage rate indicates that sustainability considerations are systematically incorporated into **backlog refinement** and **product decision‑making**. As a guideline, teams should aim for at least **90% Impact Block coverage** to ensure meaningful transparency and consistency across items.

{: .classification }
> 
> - **Category:** Transparency & Prioritization  
> - **Measurement Frequency:** per iteration  
> - **Responsible Role:**  Product Lead (primary), Engineering Team (supporting verification & feasibility), Green Agile Coach (coaching & quality enablement)

## Impact
This metric ensures that every backlog item clearly states its **intended sustainable effect**, making the impact of upcoming work visible and discussable. By requiring **measurable targets** rather than assumptions, it enables teams to prioritize based on real, evidence-supported value. The resulting transparency creates a **consistent and comparable basis** for planning, refinement, and trade-off decisions. In doing so, the metric embeds **sustainability thinking** directly into the product development flow and strengthens **impact-oriented decision-making** across the team.

## Calculation

$$
\frac{\text{Items with Impact Block}}{\text{All items in scope}} \times 100
$$

The metric is calculated by dividing the number of backlog items that contain a fully completed Impact Block by the total number of items considered in the current iteration or scope. The result is then multiplied by **100** to express the value as a percentage. A higher percentage reflects stronger integration of **sustainability criteria** into backlog refinement and planning.

## Example

To illustrate this metric, consider a backlog containing **15 items** for an iteration.  
Among these items is a user story focused on **improving accessibility** by introducing a *High‑Contrast Mode* for users with visual impairments. This story includes a complete Impact Block, making its sustainable and inclusive effect transparent.

### Example Impact Block — “High‑Contrast Mode for Accessibility”
- **Effect Type:** indirect  
- **Sustainability Dimensions:** social, ecological  
- **Selected Metric (Baseline → Target):**  
  - *WCAG Contrast Compliance:* 65% → ≥ 95% of UI elements meeting contrast ratio  
- **Verification Method:**  
  - Automated accessibility audits (AXE, Lighthouse)  
  - Manual UI contrast review  
  - Attached before/after screenshots demonstrating improved readability  

If **12 out of 15** backlog items include such a complete Impact Block, the metric is calculated as:

$$
\frac{12}{15} \times 100 = 80\%
$$

This result shows that **80% of the backlog** provides clear visibility into sustainability and accessibility considerations. A strong share of such items helps ensure that inclusive design and user‑centric sustainability goals are consistently integrated into planning and refinement.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics/product-management" style="text-small">← Product Management</a>
  <a href="/metrics/product-management/percentage-of-indirect-impact-items" style="text-small">Percentage of Indirect Impact Items →</a>
</div>