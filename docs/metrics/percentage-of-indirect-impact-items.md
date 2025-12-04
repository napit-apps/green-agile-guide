---
layout: default
title: Percentage of Indirect Impact Items
nav_order: 2
parent: Green-Product-Backlog
permalink: /metrics/green-product-backlog/percentage-of-indirect-impact-items
---

# Percentage of Indirect Impact Items

This metric measures the **percentage of backlog items** that enable users or the organization to adopt more sustainable behaviors. It highlights how strongly a product contributes to **indirect sustainability impact**, going beyond purely technical improvements by influencing user decisions, promoting resource-efficient usage patterns, or reducing avoidable environmental footprints. This metric is intended as a **reporting metric** and does not define a fixed target value, as the desirable share of indirect-impact items depends strongly on the product's nature, maturity, and sustainability strategy.

## Summary
This metric captures how many backlog items are classified as having an **indirect sustainability effect**. Indirect effects occur when a feature empowers users or the organization to behave more sustainably—for example, by enabling lower‑impact choices, promoting transparency, or nudging toward efficient usage habits. Tracking this percentage supports a better understanding of the product's broader sustainability influence and fosters deliberate decision‑making regarding user‑facing sustainability features.

- **Scope:** Green Product Backlog / Impact Beyond the Product**
- **Category:** Impact Beyond the Product  
- **Effect Type:** indirect  
- **Dimension(s):** ecological / economic / social  
- **Measurement Frequency:** per release  
- **Responsible Role:** GPO  

## Purpose
The purpose of this metric is to highlight how much of the planned work contributes to **sustainability through user behavior** rather than internal technical optimization. It helps teams understand the balance between direct efficiency improvements and more strategic sustainability impact via user empowerment. This visibility enables better product strategy discussions and supports the creation of features that foster **long‑term, behavior‑driven impact**.

## Description
This metric reflects the proportion of backlog items that are marked as having an **indirect sustainability effect**, based on the Impact Block classification. An item is considered indirect when it does not directly reduce energy, compute, emissions, or resource use within the system, but instead **influences user choices or organizational actions** that lead to sustainability improvements. Examples include features that encourage low‑impact usage patterns, provide data transparency, or offer sustainability‑oriented configuration modes. Because indirect effects depend heavily on product context and user behavior, this metric is **context‑dependent** and should be interpreted as a descriptive indicator rather than a target metric.

## Calculation

**Formula:**  
\[
\frac{\text{Items classified as indirect}}{\text{All items with an Impact classification}} \times 100
\]

The metric is calculated by dividing the number of backlog items labeled as having an indirect sustainability effect by the total number of items for which an Impact classification exists. The result is then multiplied by **100** to express the value as a percentage. A higher percentage may indicate a strategic focus on user‑empowering sustainability features, while a lower percentage suggests that the team is currently prioritizing more direct or technical improvements. Since the optimal ratio varies between products, this metric is primarily used for **reporting and analysis**, rather than for defining a target threshold.