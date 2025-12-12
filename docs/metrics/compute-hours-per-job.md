---
layout: default
title: Compute Hours per Job
nav_order: 3
parent:  Data & AI
permalink: /metrics-and-impact/data-and-ai/compute-hours-per-job
---

# Compute Hours per Job

environmental  
{: .label .label-green }
governance  
{: .label .label-green }

direct   
{: .label .label-purple }

This metric measures the **average compute time consumed per batch or machine‑learning job**, expressed in CPU or GPU hours. It captures how resource‑intensive data processing and ML workloads are in practice and makes heavy or inefficient jobs visible. Because batch and ML jobs often dominate compute usage in data‑driven systems, this metric is a key indicator for steering efficiency in Data & AI workloads.

In a Green Agile context, Compute Hours per Job supports conscious design and operation of data pipelines and models. Excessive compute time may indicate inefficient algorithms, oversized models, unnecessary re‑training, poor parallelization, or missing reuse of intermediate results.

## Classification

{: .classification }
>
> - **Category:** Data & AI  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team

## Impact
Tracking compute hours per job enables teams to identify the main drivers of energy consumption in data processing and AI systems. A decreasing trend indicates that jobs deliver the same analytical or predictive value with fewer resources, directly reducing energy use and emissions. An increasing trend highlights efficiency regressions that may silently inflate infrastructure demand and environmental impact.

Because this metric focuses on concrete workloads, it supports targeted optimization efforts such as model simplification, smarter scheduling, improved data sampling, or reuse of trained models instead of repeated full retraining.

## Calculation

Compute Hours per Job are calculated as the **average compute time per execution**:

$$
\text{Compute Hours per Job} =
\frac{\sum \text{CPU/GPU Hours across job runs}}{\text{Number of job runs}}
$$

Both CPU and GPU hours can be used, depending on the workload. Teams should measure consistently across releases and define clear system boundaries. A **lower value is better**, provided that result quality and model performance remain acceptable.

## Example

Assume a machine‑learning training job is executed **12 times** during a release cycle. Monitoring shows a total of:

- **360 GPU hours** consumed across all runs

The average compute time per job is:

$$
\frac{360}{12} = 30 \,\text{GPU hours per job}
$$

After introducing better feature selection and early‑stopping criteria, the same job requires only **240 GPU hours** across 12 runs:

$$
\frac{240}{12} = 20 \,\text{GPU hours per job}
$$

This reduction shows that the job produces the same outcome with significantly less compute, directly improving the efficiency and sustainability of the Data & AI workload.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/data-and-ai/retention-days" style="text-small">← Retention Days</a>
  <a href="/metrics-and-impact/data-and-ai/co2e-per-job" style="text-small">CO₂e Emissions per Job →</a>
</div>