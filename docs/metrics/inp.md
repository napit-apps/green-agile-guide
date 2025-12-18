---
layout: default
title: Interaction to Next Paint (INP)
nav_order: 3
parent:  UX, Accessibility & Frontend Performance
permalink: /metrics-and-impact/ux-accessibility-and-frontend-performance/inp
---

# Interaction to Next Paint (INP)

environmental  
{: .label .label-green }

social  
{: .label .label-green }

direct  
{: .label .label-purple }

This metric measures **Interaction to Next Paint (INP)**, which captures the time between a user interaction (such as a click, tap, or key press) and the next visual update on the screen. It reflects how responsive and fluid a user interface feels during real interaction, making it a key indicator for frontend interactivity and perceived performance.

In a Green Agile context, INP links **responsiveness, usability, and energy efficiency**. Slow interaction feedback often points to heavy JavaScript execution, inefficient event handling, or blocking main‑thread work. These issues not only degrade user experience but also increase CPU usage and energy consumption on user devices.

## Classification

{: .classification }
>
> - **Category:** UX, Accessibility & Frontend Performance  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team

## Impact
A low INP value ensures that interfaces respond quickly to user input, reducing frustration and supporting accessible interaction for users with motor or cognitive impairments. From a sustainability perspective, faster interaction handling shortens periods of high CPU load on the client side, contributing to lower energy consumption during active use.

Because INP directly reflects the efficiency of frontend interaction handling, it is a **direct-impact metric**. Improving INP encourages teams to reduce main‑thread blocking, optimize JavaScript execution, and design interaction flows that remain responsive even on low‑end devices.

## Calculation

INP is reported as a **time-based performance metric**, typically using the **98th percentile** of observed interaction delays to reflect worst‑case user experience.

$$
\text{INP} = \text{Interaction-to-render delay (98th percentile)}
$$

A value of **≤ 200 milliseconds** is considered *good* according to current web performance guidance.

## Example

Assume real-user monitoring data shows the following INP values for a key interaction (e.g. opening a menu) during a release cycle:

- Median INP: 110 ms  
- 75th percentile: 160 ms  
- **98th percentile: 260 ms**

Because the 98th percentile exceeds the recommended threshold, the metric indicates interaction performance issues affecting some users. After optimizing JavaScript execution and removing unnecessary synchronous handlers, the 98th percentile INP improves to **180 ms**, bringing the interaction responsiveness into the *good* range.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/ux-accessibility-and-frontend-performance/lcp" style="text-small">← Largest Contentful Paint (LCP)</a>
  <a href="/metrics-and-impact/ux-accessibility-and-frontend-performance/ttfb" style="text-small">Time to First Byte (TTFB) →</a>
</div>