---
layout: default
title: Time to First Byte (TTFB)
nav_order: 4
parent:  UX, Accessibility & Frontend Performance
permalink: /metrics-and-impact/ux-accessibility-and-frontend-performance/ttfb
---

# Time to First Byte (TTFB)

environmental  
{: .label .label-green }

social  
{: .label .label-green }

direct  
{: .label .label-purple }

This metric measures **Time to First Byte (TTFB)**, which represents the time between a client request and the receipt of the first byte of the server response. It captures **server-side processing time and network latency**, making it a core indicator for backend performance and perceived responsiveness.

In a Green Agile context, TTFB connects **backend efficiency, user experience, and energy consumption**. High TTFB values often indicate slow server logic, inefficient database queries, cold starts, or suboptimal infrastructure placement — all of which increase resource usage and energy demand on both server and client side.

## Classification

{: .classification }
>
> - **Category:** UX, Accessibility & Frontend Performance  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team

## Impact
A low TTFB improves perceived loading speed and reduces waiting time before meaningful rendering can begin. Faster server responses shorten high-load periods on backend systems and reduce idle waiting on client devices, contributing to lower overall energy consumption.

Because TTFB directly reflects backend and network performance characteristics, it is a **direct-impact metric**. Improving this metric encourages efficient server-side computation, optimized data access, effective caching, and region-aware infrastructure choices.

## Calculation

TTFB is measured as a **time-based performance metric**, typically reported as an **average value** or the **95th percentile** to reflect slower user experiences.

$$
\text{TTFB} = \text{Time from request start to first response byte}
$$

A value of **≤ 0.8 seconds** is commonly used as a *good* reference threshold, depending on application context and network conditions.

## Example

Assume monitoring data for an API endpoint shows the following TTFB values over a release cycle:

- Average TTFB: 420 ms  
- **95th percentile TTFB: 920 ms**

Because the 95th percentile exceeds the reference threshold, the metric indicates backend or network performance issues affecting a subset of users. After introducing query optimization and enabling response caching, the 95th percentile TTFB improves to **650 ms**, bringing backend response times into an acceptable range.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/ux-accessibility-and-frontend-performance/inp" style="text-small">← Interaction to Next Paint (INP)</a>
  <a href="/metrics-and-impact/ux-accessibility-and-frontend-performance/bytes-per-view" style="text-small">Bytes per View →</a>
</div>