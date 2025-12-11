---
layout: default
title: Grid Carbon Intensity
nav_order: 3
parent:  Architecture & Infrastructure
permalink: /metrics-and-impact/architecture-and-infrastructure/grid-carbon-intensity
---

# Grid Carbon Intensity (gCO₂e per kWh, Region)

environmental  
{: .label .label-green }

indirect  
{: .label .label-purple }

This metric captures the **carbon intensity of electricity** in the region where a workload is hosted. Grid Carbon Intensity (measured in gCO₂e per kWh) indicates how much greenhouse gas emissions are produced for each kilowatt-hour of electricity consumed. Since electricity generation varies significantly by region — depending on the mix of renewable, nuclear, and fossil energy sources — the same workload can have a drastically different carbon footprint depending on where it runs.

This metric is important for Green Agile because it makes the **environmental impact of regional hosting decisions** explicit. Understanding a region’s carbon intensity enables teams to select hosting locations that minimize emissions, consider sustainable migration strategies, and better estimate the ecological footprint of compute operations. The metric directly supports **Carbon Awareness**, **Energy Efficiency**, and **Impact Transparency**, encouraging teams to pair efficient infrastructure with low‑carbon energy sources for maximum sustainability benefit. Cloud providers and public energy agencies publish these values, allowing teams to base decisions on reliable external data.

## Classification

{: .classification }
>
> - **Category:** Architecture & Infrastructure  
> - **Measurement Frequency:** per release  
> - **Responsibility:** Product Lead (regional strategy), Engineering Team (documentation)

## Impact
Tracking grid carbon intensity supports more sustainable architectural choices by revealing how regional electricity generation affects overall emissions. It exposes the environmental consequences of region selection and helps teams evaluate whether alternatives — such as migrating workloads, scheduling flexible tasks to greener regions, or adopting carbon‑aware architectures — can reduce emissions. Because this metric reflects external energy infrastructure rather than internal system behavior, it highlights **indirect environmental impact** and ensures that hosting decisions are aligned with ecological sustainability goals.

## Calculation

The metric requires no internal computation. Teams document the published carbon‑intensity value for their hosting region, which cloud providers or public energy authorities derive from the regional electricity mix — the percentage share of different energy sources and their individual emission factors. A **lower value is better**, as it indicates a cleaner energy mix and lower greenhouse gas emissions for the workload running in that region.

The official formula is:

$$
\text{Carbon Intensity (CI)} = \frac{\text{Total CO₂ Emissions}}{\text{Total Electricity Generated}}
$$

When a region uses a mix of different electricity sources, the overall Grid Carbon Intensity (CI) is obtained by calculating the weighted sum of the carbon intensities of all sources in the mix:

$$
\text{CI}_{\text{region}} = \sum \left( \text{CI}_i \times \text{Share}_i \right)
$$

where  
• $$\text{CI}_i $$ is the carbon intensity of an individual energy source (e.g., wind, solar, gas, coal)  
• $$ \text{Share}_i $$ is its percentage in the regional electricity mix  

Teams do not calculate this value themselves — it is published by energy authorities or cloud providers.


## Example

To illustrate how Grid Carbon Intensity is used in practice, consider first a simplified case with a single energy source and then a regional electricity mix.

### Step 1: Carbon Intensity for Coal-Based Electricity

Assume a coal-fired power plant generates **1 000 MWh** of electricity during a reporting period and emits **900 t CO₂e** in that time. Using the formula we obtain:

$$
\text{CI}_\text{coal} = \frac{900\,\text{t CO₂e}}{1\,000\,\text{MWh}} = 0.9\,\text{t CO₂e/MWh} = 900\,\text{g CO₂e/kWh}
$$

This value represents a typical order of magnitude for coal-based electricity.

### Step 2: Weighted Carbon Intensity for a Regional Electricity Mix (Example Inspired by Germany)

Now consider a regional grid with a realistic mixed electricity supply, for example:

- 50% renewables (wind, solar, hydro, biomass) with an average CI of 50 g CO₂e/kWh  
- 20% natural gas with a CI of 400 g CO₂e/kWh  
- 25% coal (lignite and hard coal) with a CI of 900 g CO₂e/kWh  
- 5% other sources (imports/other fossil) with a CI of 500 g CO₂e/kWh  

Using the weighted-sum formula we calculate:

$$
\text{CI}_{\text{region}} =
(0.50 \times 50)
+ (0.20 \times 400)
+ (0.25 \times 900)
+ (0.05 \times 500)
$$

$$
= 25 + 80 + 225 + 25 = 355\,\text{g CO₂e/kWh}
$$

This example illustrates how strongly a region’s electricity mix influences its overall Grid Carbon Intensity.

---

<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/architecture-and-infrastructure/pue-per-region" style="text-small">← PUE per Region</a>
  <a href="" style="text-small"> →</a>
</div>