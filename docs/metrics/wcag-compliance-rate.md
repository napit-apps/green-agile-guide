---
layout: default
title: WCAG 2.2 Compliance Rate
nav_order: 1
parent:  UX, Accessibility & Frontend Performance
permalink: /metrics-and-impact/ux-accessibility-and-frontend-performance/wcag-compliance-rate
---

# WCAG 2.2 Compliance Rate

social  
{: .label .label-green }

governance  
{: .label .label-green }

direct  
{: .label .label-purple }

systemic  
{: .label .label-purple }

This metric measures the **percentage of applicable WCAG 2.2 success criteria that are fulfilled**, with a focus on achieving at least **Level AA** compliance. It makes the accessibility level of a digital product explicit and comparable, supporting inclusive user experiences for people with disabilities and diverse access needs.

In a Green Agile context, the WCAG 2.2 Compliance Rate is a **direct inclusion metric with systemic implications**. Improving compliance reduces barriers for users immediately, while sustained progress depends on long‑term design decisions, development practices, testing processes, and governance structures.

## Classification

{: .classification }
>
> - **Category:** UX, Accessibility & Frontend Performance  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Engineering Team (testing), Green Agile Coach (review and guidance)

## Impact
A high WCAG compliance rate indicates that accessibility requirements are consistently integrated into the product lifecycle. Improving this metric directly enhances **social sustainability** by reducing barriers for users with visual, auditory, motor, or cognitive impairments.

Because accessibility is shaped by cross‑functional decisions and long‑term practices, improving this metric combines a **direct social effect** with a **systemic effect** over time. It encourages teams to embed accessibility into design systems, coding standards, testing pipelines, and review processes. Failing to meet WCAG requirements can exclude users, create legal risk, and undermine trust — making accessibility a core sustainability concern rather than an optional enhancement.

## Calculation

The WCAG 2.2 Compliance Rate is calculated as the ratio of fulfilled criteria to all applicable criteria:

$$
\text{WCAG Compliance Rate} =
\frac{\text{Passed WCAG Criteria}}{\text{Applicable WCAG Criteria}} \times 100
$$

Only criteria that are relevant to the product context are included in the denominator.  
The recommended target is **Level AA compliance**, which typically corresponds to **close to 100% of applicable criteria fulfilled**.

## Example

Assume a web application is evaluated against **48 applicable WCAG 2.2 success criteria**. Automated tests and manual reviews confirm that **45 criteria are fulfilled**.

Using the formula:

$$
\frac{45}{48} \times 100 = 93.75\%
$$

The product does not yet meet full Level AA compliance. The remaining criteria highlight concrete improvement areas, such as color contrast, keyboard navigation, or focus visibility. Addressing these gaps increases inclusiveness and strengthens the overall quality and sustainability of the user experience.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/ux-accessibility-and-frontend-performance" style="text-small">← UX, Accessibility & Frontend Performance</a>
  <a href="/metrics-and-impact/ux-accessibility-and-frontend-performance/lcp" style="text-small">Largest Contentful Paint (LCP) →</a>
</div>