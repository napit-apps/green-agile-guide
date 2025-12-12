---
layout: default
title: Metrics & Impact
nav_order: 3
parent: 
permalink: /metrics-and-impact/
---

# Green Agile Metrics

Sustainable product development requires more than good intentions — it requires **visibility**. In Green Agile, we quantify what matters, because meaningful change is only possible when teams understand **where they stand** and **how their decisions shift impact over time**. Metrics help teams recognize progress, identify obstacles, and continuously improve ecological, economical und sozial sustainability.

## Why Quantification Matters

Improvement requires measurement. Without a baseline, there is no way to understand whether a feature, architectural decision, or workflow actually reduces environmental impact or increases long‑term sustainability. Metrics make sustainability **actionable**, **transparent**, and **comparable**, allowing teams to make informed decisions instead of assumptions.

At the same time, not everything can or should be measured with perfect precision. In complex sociotechnical systems, some effects are hard to quantify directly — for example, changes in user behavior, emerging architectural complexity, or long‑term operational impacts. This is where **proxies** become essential.

## Proxies for Sustainable Impact

A **proxy** is a simplified indicator that approximates a sustainability effect when direct measurement would be too complex, costly, or impossible. Proxies allow teams to stay pragmatic while still making sustainability measurable.

Common examples include:

{: .example }
> 
- **Bytes per View** as a proxy for energy usage in frontend rendering  
- **Build minutes per change** as a proxy for CI/CD compute consumption  
- **Retention days** as a proxy for data minimization and storage footprint  
- **Accessibility compliance rates** as a proxy for inclusive user experience  
- **CPU time per transaction** as a proxy for backend efficiency  

Proxies can be **very simple**, as long as they are consistent and meaningful. Even a basic trend — such as “number of architectural decisions documented with ADR‑Light” — provides insight and helps guide better decisions over time.

## Navigating Trade‑Offs in Sustainable Development

Sustainability in software is never one‑dimensional. Teams must often balance **competing requirements** across ecological, economic, and social dimensions — and sometimes even between sustainability and other quality attributes such as security or usability.

Trade‑offs are not a sign of failure; they are a natural part of designing real systems. Metrics help teams make these trade‑offs **explicit**, discuss them openly, and document them transparently.

### Examples of Common Trade‑Offs

{: .example }
> 
**Longer device support vs. security risks**  
Extending software support for older devices is *ecologically beneficial* because it reduces hardware replacement and electronic waste.  
However, older devices may no longer receive critical security updates, creating **social and security risks**.  
Teams must weigh the ecological benefit against user safety and regulatory compliance.

{: .example }
> 
**Energy savings vs. measurement overhead**  
Sometimes the effort to measure a particular impact precisely (e.g., exact GPU energy consumption for small workloads) produces more complexity, cost, or engineering effort than the expected savings justify.  
In such cases, teams may choose a **simplified proxy metric** instead of precise measurement — prioritizing pragmatism and value over perfection.

{: .example }
> 
**Heavy caching vs. data freshness**  
Increasing cache hit rates can reduce backend compute and energy consumption, but may negatively affect **data accuracy** or **user experience** when stale data becomes visible.

These examples highlight that sustainability decisions must be made with **full context**, not in isolation. Green Agile encourages teams to use metrics to guide discussions — not to enforce purity, but to support *informed, balanced decision‑making*.

## Metric Categories

This section is **work in progress**. The Green Agile Metrics framework is continuously evolving, and additional metrics and categories are being added over time. The structure below reflects the current state and will expand as new insights, practices, and sustainability needs emerge.

The Green Agile framework organizes its metrics into clear categories to support different aspects of sustainable product development:

- **[Product Management](/metrics-and-impact/product-management)**
- **[Architecture & Infrastructure](/metrics-and-impact/architecture-and-infrastructure)**  
- **[Code, Build & CI/CD](/metrics-and-impact/code-build-and-cicd)**  
- **Data & AI**  
- **UX, Accessibility & Frontend Performance**  
- **Operations & Observability**  
- **Governance, Reporting & Compliance**  

Explore each category to understand how quantitative insights can guide more sustainable choices throughout the entire product lifecycle.

---

<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/product-management" style="text-small">Product Management →</a>
</div>