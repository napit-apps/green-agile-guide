---
layout: default
title: #ToDo
nav_order: #ToDo
parent: #ToDo
permalink: #ToDo
---

# Power Usage Effectiveness (PUE) per Region

This metric tracks the **Power Usage Effectiveness (PUE)** of the data center region in which a product or workload is hosted. PUE is a widely used industry standard that reflects how efficiently a data center uses energy. A lower PUE indicates that a larger share of consumed electricity powers actual compute resources rather than overhead such as cooling or facility operations. Since PUE varies significantly between regions, this metric helps teams make **sustainable location choices** and understand the environmental footprint of their infrastructure.

## Summary
This metric captures the **energy efficiency of a data center region** by using its published PUE value. PUE expresses the ratio between total energy consumed by the data center and the energy delivered to IT equipment. Lower PUE values correspond to more efficient data centers and therefore reduce indirect emissions from infrastructure usage. Tracking PUE supports more sustainable architecture decisions and encourages conscious regional placement of workloads.

## Classification
- **Scope:** Architecture & Infrastructure / Region Selection  
- **Category:** Infrastructure Efficiency & Sustainability  
- **Effect Type:** indirect (infrastructure)  
- **Dimension(s):** ecological / economic  
- **Measurement Frequency:** per release  
- **Responsible Role:**  
  - **GPO:** region selection  
  - **GDT:** documentation  

## Purpose
The purpose of this metric is to ensure that infrastructure choices take **data center efficiency** into account. Since the same workload can have vastly different environmental impacts depending on where it is hosted, PUE serves as a key indicator for choosing **low-impact cloud regions**. It helps teams make informed decisions when selecting or migrating regions and encourages the use of energy-efficient facilities provided by cloud vendors.

## Description
PUE is published by cloud providers for each of their data center regions. It is calculated as the ratio between the facility’s **total energy consumption** and the energy delivered to computing hardware. A PUE close to **1.0** indicates exceptional efficiency; typical regions range between **1.1 and 1.6**, depending on climate, data center design, and operational maturity. This metric does not require teams to compute PUE themselves but to **track and document the PUE of the region they operate in**. A lower value reduces the environmental footprint of any compute performed in that region. As a general guideline, teams should aim for hosting in regions with a PUE of **< 1.3**, while considering regulatory, latency, and compliance constraints.

## Calculation

**Formula:**  
\[
\text{PUE} = \frac{\text{Total data center energy consumption}}{\text{Energy delivered to IT equipment}}
\]

PUE is not calculated by the team but retrieved from the cloud provider’s published data. The metric requires documenting the PUE value for the selected region during each release cycle. A **lower PUE is better**, as it reflects more efficient infrastructure usage and therefore contributes to reducing the overall environmental impact of the system.