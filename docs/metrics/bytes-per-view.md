---
layout: default
title: Bytes per View
nav_order: 5
parent:  UX, Accessibility & Frontend Performance
permalink: /metrics-and-impact/ux-accessibility-and-frontend-performance/bytes-per-view
---

# Bytes per View

environmental  
{: .label .label-green }

social  
{: .label .label-green }

direct  
{: .label .label-purple }

This metric measures the **amount of data transferred per page view**, expressed in bytes. It captures how much information is sent from servers to user devices during a single page load, making data efficiency and frontend payload size visible.

In a Green Agile context, Bytes per View links **frontend design decisions with energy consumption and accessibility**. Larger payloads increase network traffic, prolong loading times, and raise energy use on both server and client side. They can also negatively affect users on slow connections or low-end devices.

## Classification

{: .classification }
>
> - **Category:** UX, Accessibility & Frontend Performance  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team

## Impact
Reducing Bytes per View improves loading performance, lowers energy consumption for data transmission, and supports inclusive access for users with limited bandwidth or data caps. Smaller payloads reduce network overhead, shorten high-power states on devices, and contribute to a more sustainable and equitable user experience.

Because this metric directly reflects the amount of data transferred per interaction, it represents a **direct-impact metric**. Improvements typically come from optimizing images, reducing unused JavaScript and CSS, applying compression, and avoiding unnecessary third-party resources.

## Calculation

Bytes per View are calculated as the **average amount of data transferred per page view**:

$$
\text{Bytes per View} =
\frac{\sum \text{Transferred Bytes}}{\text{Number of Views}}
$$

Teams often define a **data budget** for this metric, for example **≤ 200 KB per view**, depending on product context and user needs.

## Example

Assume monitoring data for a page shows **500 page views** during a release cycle, with a total of **95 MB** of data transferred.

Converted to kilobytes:

$$
95 \text{ MB} = 97\,280 \text{ KB}
$$

Using the formula:

$$
\frac{97\,280}{500} = 194.6 \text{ KB per view}
$$

This result stays within a defined team budget of **200 KB per view**. If the value increases in future releases, the team may investigate oversized assets, unused scripts, or additional third-party requests.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/ux-accessibility-and-frontend-performance/ttfb" style="text-small">← Time to First Byte (TTFB)</a>
  <a href="/metrics-and-impact/ux-accessibility-and-frontend-performance/requests-per-view" style="text-small">Requests per View →</a>
</div>