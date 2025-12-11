---
layout: default
title: Percentage of Indirect Impact Items
nav_order: 2
parent: Product Management
permalink: /metrics-and-impact/product-management/percentage-of-indirect-impact-items
---

# Percentage of Indirect Impact Items

environmental  
{: .label .label-green }
social  
{: .label .label-green }

indirect 
{: .label .label-purple }

This metric captures the **percentage of backlog items** that enable users or the organization to adopt more sustainable behaviors. It reflects how strongly a product contributes to **indirect sustainability impact** by influencing user decisions, promoting resource‑efficient usage patterns, or reducing avoidable environmental footprints. As a **reporting metric**, it does not define a fixed target value; the desirable share depends on the product’s nature, maturity, and sustainability strategy.

An item is considered indirect when it does not directly reduce energy, compute, emissions, or resource use within the system, but instead **influences user choices or organizational actions** that lead to sustainability improvements. Examples include features that encourage low‑impact usage patterns, provide data transparency, or offer sustainability‑oriented configuration modes. Because indirect effects depend heavily on product context and user behavior, this metric is **context‑dependent** and should be interpreted as a descriptive indicator rather than a target metric.

{: .classification }
> 
> - **Category:** Impact Beyond the Product  
> - **Measurement Frequency:** per release  
> - **Responsible Role:** GPO  

## Impact
The purpose of this metric is to highlight how much of the planned work contributes to **sustainability through user behavior** rather than internal technical optimization. It helps teams understand the balance between direct efficiency improvements and more strategic sustainability impact via user empowerment. This visibility enables better product strategy discussions and supports the creation of features that foster **long‑term, behavior‑driven impact**.

## Calculation
 
$$
\frac{\text{Items classified as indirect}}{\text{All items with an Impact classification}} \times 100
$$

The metric is calculated by dividing the number of backlog items labeled as having an indirect sustainability effect by the total number of items for which an Impact classification exists. The result is then multiplied by **100** to express the value as a percentage. A higher percentage may indicate a strategic focus on user‑empowering sustainability features, while a lower percentage suggests that the team is currently prioritizing more direct or technical improvements. Since the optimal ratio varies between products, this metric is primarily used for **reporting and analysis**, rather than for defining a target threshold.

## Example

An online shop wants to reduce **product returns** and the associated emissions caused by unnecessary shipping and reverse logistics. To achieve this, the shop introduces a new **Size & Fit Guidance Feature** that provides customers with personalized recommendations based on their body measurements, preferred fit, and past purchases. This feature does not directly change the system’s energy consumption or compute usage, but it **enables customers to make more informed purchasing decisions**, thereby reducing the likelihood of incorrect orders and avoidable returns. Because the sustainability effect depends on user behavior rather than system‑internal optimization, the feature is classified as **indirect**.

Among these, **7 items** are marked as indirect because they all relate to the new Size & Fit Guidance Feature and its supporting functionality. Each of these items contributes to reducing incorrect orders by improving customer decision‑making, which means their sustainability impact arises from **user behavior change** rather than system‑internal optimization.

$$
\frac{7}{22} \times 100 \approx 31.8\%
$$

This means that **31.8%** of the items in this release contribute to sustainability indirectly. The result gives the team insight into how much of their planned work promotes behavior‑driven impact and whether they want to increase or rebalance this proportion in future iterations.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/product-management/percentage-of-backlog-items-with-impact-block" style="text-small">← Percentage of Backlog Items with Impact Block</a>
  <a href="/metrics-and-impact/product-management/number-of-item-to-goal-links" style="text-small">Number of Item-to-Goal Links →</a>
</div>