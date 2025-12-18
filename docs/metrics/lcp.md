---
layout: default
title: Largest Contentful Paint (LCP)
nav_order: 2
parent:  UX, Accessibility & Frontend Performance
permalink: /metrics-and-impact/ux-accessibility-and-frontend-performance/lcp
---

# Largest Contentful Paint (LCP)

environmental  
{: .label .label-green }

social  
{: .label .label-green }

governance  
{: .label .label-green }

direct  
{: .label .label-purple }

This metric measures the **Largest Contentful Paint (LCP)**, which represents the render time of the largest visible content element in the viewport. It reflects how quickly users perceive a page as loading and usable, making it a key indicator for user experience and frontend performance.

In a Green Agile context, LCP connects **user experience quality with energy efficiency**. Slow rendering times often indicate oversized assets, inefficient loading strategies, or unnecessary data transfer — all of which increase energy consumption on both client and server side.

## Classification

{: .classification }
>
> - **Category:** UX, Accessibility & Frontend Performance  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team

## Impact
A low LCP value improves perceived performance and reduces user frustration, especially on low-end devices or slow networks. Because teams often set LCP as a release KPI or performance budget, it also supports governance by making performance and sustainability trade-offs explicit and measurable. Faster rendering reduces the time devices spend at high power states, contributing to lower energy consumption during page load. Improving LCP therefore supports both **environmental sustainability** and **social sustainability** by enabling accessible, performant experiences for a broad range of users.

Because LCP directly reflects frontend delivery efficiency, it is a **direct-impact metric**. It encourages teams to optimize images, fonts, scripts, and loading strategies, and to prioritize meaningful content over decorative or blocking elements.

## Calculation

LCP is measured as a **time-based performance metric**, typically reported as the **98th percentile** of observed page loads to capture worst-case user experience.

$$
\text{LCP} = \text{Render time of the largest visible content element (98th percentile)}
$$

A value of **≤ 2.5 seconds** is considered *good* according to common web performance standards.

## Example

Assume real-user monitoring data shows the following LCP values for a product page over a release cycle:

- Median LCP: 1.9 s  
- 75th percentile: 2.2 s  
- **98th percentile: 2.8 s**

Because the 98th percentile exceeds the recommended threshold, the metric indicates a performance issue affecting a subset of users. By optimizing hero images and deferring non-critical scripts, the team reduces the 98th percentile LCP to **2.3 s**, bringing the page back into the *good* range.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/ux-accessibility-and-frontend-performance/wcag-compliance-rate" style="text-small">← WCAG 2.2 Compliance Rate</a>
  <a href="/metrics-and-impact/ux-accessibility-and-frontend-performance/inp" style="text-small">Interaction to Next Paint (INP) →</a>
</div>