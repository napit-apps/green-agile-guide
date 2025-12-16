---
layout: default
title: CI/CD Resources per Change
nav_order: 4
parent: Code, Build & CI/CD
permalink: /metrics-and-impact/code-build-and-cicd/cicd-resources-per-change
---

# CI/CD Resources per Change

environmental  
{: .label .label-green }

governance  
{: .label .label-green }

direct  
{: .label .label-purple }

systemic  
{: .label .label-purple }

This metric measures the **compute resources consumed by CI/CD pipelines per change**, expressed as aggregated compute time (and optionally cost) divided by the number of changes. It makes delivery-process overhead visible and supports conscious optimization of build, test, and deployment automation.

In a Green Agile context, CI/CD Resources per Change highlights how **process design and automation choices** influence energy consumption, infrastructure usage, and delivery efficiency. Excessive pipeline execution, redundant steps, or overly broad test stages can silently create significant overhead even when individual builds appear fast.

## Classification

{: .classification }
>
> - **Category:** Code, Build & CI/CD  
> - **Measurement Frequency:** per iteration  
> - **Responsibility:** Engineering Team

## Impact
A decreasing value indicates that the delivery pipeline becomes more efficient, consuming fewer resources for the same amount of change. An increasing value signals growing overhead caused by duplicated pipeline runs, missing caching, inefficient test setups, or unnecessary environments.

Because this metric reflects the cumulative effect of process decisions across the delivery system, it represents a **systemic impact**. It supports governance by providing transparency into CI/CD efficiency and by enabling teams to steer pipeline complexity deliberately rather than letting it grow unnoticed.

## Calculation

CI/CD Resources per Change are calculated as the **average CI/CD compute time per change**:

$$
\text{CI/CD Resources per Change} =
\frac{\sum \text{CI/CD Compute Minutes}}{\text{Number of Changes}}
$$

Where *changes* may include commits, merge requests, or deployed change sets, depending on the team’s workflow. The desired direction is a **falling trend**, while maintaining build quality, test coverage, and delivery reliability.

## Example

Assume that during one iteration:

- Total CI/CD compute time: **3,600 minutes**  
- Number of changes (merge requests): **120**

Using the formula:

$$
\frac{3\,600}{120} = 30 \text{ minutes per change}
$$

If earlier iterations averaged **45 minutes per change**, this reduction indicates a more efficient pipeline, for example through improved caching, selective test execution, or consolidated build stages.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/code-build-and-cicd/technical-debt-trend" style="text-small">← Technical Debt Trend</a>
  <a href="/metrics-and-impact/code-build-and-cicd/hotspot-trend" style="text-small">Hotspot Trend →</a>
</div>