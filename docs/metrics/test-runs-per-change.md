---
layout: default
title: Test Runs per Change
nav_order: 2
parent: Code, Build & CI/CD
permalink: /metrics-and-impact/code-build-and-cicd/test-runs-per-change
---

# Test Runs per Change

environmental  
{: .label .label-green }

direct  
{: .label .label-purple }

governance  
{: .label .label-green }

systemic  
{: .label .label-purple }

This metric measures the **number of relevant test executions triggered per code change** in the CI/CD pipeline. It highlights inefficiencies caused by redundant or unnecessary test runs and helps teams understand where pipeline over-testing consumes excessive compute resources, slows down feedback cycles, and increases energy usage. A high number of test runs per change often signals misconfigured pipelines, overly broad triggers, or insufficient test scoping.

Optimizing the number of test executions supports Green Agile principles by improving the efficiency of the CI/CD pipeline, reducing unnecessary compute load, and focusing resources where they create real value. While reducing redundant test runs is beneficial, it is essential that **test quality never decreases**. Any reduction in execution must preserve or improve confidence in system correctness — otherwise, the result is not an improvement but a degradation in product quality.

{: .classification }
>
> - **Category:** Code, Build & CI/CD  
> - **Measurement Frequency:** per iteration  
> - **Responsibility:** Engineering Team (primary), Product Lead (prioritization input), Green Agile Coach (enablement)

## Impact
Optimizing this metric reduces the overall compute load in CI/CD pipelines and minimizes energy consumption tied to automated testing. Lowering redundant test runs shortens pipeline duration, accelerates developer feedback loops, and reduces infrastructure costs. It also encourages better test strategy design — such as test impact analysis, selective testing, or improved test modularization — helping teams maintain high product quality while avoiding unnecessary execution overhead.

## Calculation

The metric is calculated by summing all relevant test executions during an iteration and dividing the total by the number of code changes processed by the pipeline.

$$
\text{Test Runs per Change} = 
\frac{\sum \text{Test Runs}}{\# \text{Changes}}
$$

A **lower value is better**, and teams should define target thresholds based on product complexity, test coverage requirements, and the desired balance between fast feedback and reliable validation.

## Example

During an iteration, the CI/CD pipeline executes **450 total test runs** across **30 code changes**.

Using the formula:

$$
\frac{450}{30} = 15
$$

The Test Runs per Change value for this iteration is **15**. If the team previously averaged **22**, this reduction may signal improved efficiency — **provided that test quality has been maintained or improved**. A lower number is only beneficial when it does not reduce confidence in product correctness. If the value increases, the team may investigate unnecessary triggers, overly broad suites, or missing selective test logic to avoid waste while preserving high-quality validation.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/code-build-and-cicd/build-minutes-per-change" style="text-small">← Build Minutes per Change</a>
  <a href="/metrics-and-impact/code-build-and-cicd/technical-debt-trend" style="text-small">Technical Debt Trend →</a>
</div>