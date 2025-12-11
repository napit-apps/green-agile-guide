---
layout: default
title: Build Minutes per Change
nav_order: 1
parent: Code, Build & CI/CD
permalink: /metrics-and-impact/code-build-and-cicd/build-minutes-per-change
---

# Build Minutes per Change

environmental  
{: .label .label-green }

direct  
{: .label .label-purple }

This metric measures the **total build time consumed per code change** within the CI/CD pipeline. It reflects how efficiently the build system uses compute resources and highlights unnecessary costs, delays, and energy consumption. High build times increase feedback cycles, slow down delivery flow, and consume excessive compute resources — all of which negatively impact sustainability and team productivity.

Build Minutes per Change acts as a direct indicator of pipeline efficiency. Reducing build time supports Green Agile principles such as **Flow**, **Lean**, **Value Focus**, and **Energy Awareness**, helping teams eliminate waste, shorten cycle times, and lower infrastructure load.

{: .classification }
>
> - **Category:** Code, Build & CI/CD  
> - **Measurement Frequency:** per iteration  
> - **Responsibility:** Engineering Team (primary), Product Lead (prioritization support), Green Agile Coach (enablement)

## Impact
A lower Build Minutes per Change value improves both ecological and economic sustainability by reducing compute consumption in CI/CD pipelines. Faster builds improve developer flow, shorten feedback loops, and reduce idle waiting time. This enables teams to iterate more effectively while also reducing the infrastructure cost and energy footprint of the development process. Tracking this metric exposes wasteful build steps, redundant dependencies, oversized containers, or inefficient compilation processes that slow down delivery and increase emissions.

## Calculation

The metric is calculated by summing all build minutes during an iteration and dividing the total by the number of code changes processed by the pipeline.

$$
\text{Build Minutes per Change} = 
\frac{\sum \text{Build Minutes}}{\# \text{Changes}}
$$

A **lower value is better**, and teams are encouraged to define their own target values based on historical performance and required build complexity.

## Example

During an iteration, the CI/CD pipeline executes **120 total build minutes** across **15 code changes**.

Using the formula:

$$
\frac{120}{15} = 8
$$

The Build Minutes per Change for the iteration is **8 minutes**. If the previous iteration had **10 minutes** per change, the team can see measurable improvement — or identify regression if the number increased. Optimizing this value helps reduce compute load, energy usage, and feedback latency while strengthening sustainable engineering practices.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/code-build-and-cicd" style="text-small">← Code, Build & CI/CD</a>
  <a href="/metrics-and-impact/code-build-and-cicd/test-runs-per-change" style="text-small">Test Runs per Change →</a>
</div>