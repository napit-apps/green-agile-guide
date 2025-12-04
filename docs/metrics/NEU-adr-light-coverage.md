---
layout: default
title: ADR-Light Coverage
nav_order: 1
parent: architecture and infrastructure
permalink: metrics/architecture and infrastructure/adr-light-coverage
---

# ADR-Light Coverage

This metric measures the **percentage of significant architecture and data decisions** that are documented using **ADR-Light**, a lightweight, high-clarity format for architectural decision records. A higher coverage ensures improved traceability, transparency, and consistency in architectural reasoning, supporting sustainable and maintainable long-term system evolution.

## Summary
This metric reflects the proportion of important architectural or data-related decisions that have been documented using ADR-Light. By ensuring that critical decisions are recorded in a structured and accessible way, the metric strengthens **traceability**, improves **team alignment**, and supports **sustainable architectural practices** across iterations. High coverage indicates that architectural decisions can be easily understood, challenged, and evolved over time.

## Classification
- **Scope:** Architecture & Infrastructure / Traceability  
- **Category:** Decision Documentation & Transparency  
- **Effect Type:** indirect (structural)  
- **Dimension(s):** ecological / economic / social  
- **Measurement Frequency:** per iteration  
- **Responsible Role:** GDT  

## Purpose
The purpose of this metric is to ensure that architectural decisions are not implicitly carried forward but are **explicitly documented**, making the system more resilient and maintainable over time. ADR-Light improves decision quality by ensuring that reasoning, alternatives, trade-offs, and sustainability considerations are captured. This supports more informed discussions, reduces architectural drift, and improves the continuity of architectural knowledge within the team.

## Description
This metric measures how many significant architecture or data decisions within an iteration are recorded using the **ADR-Light** format. ADR-Light provides a concise, structured record of a decision, clarifying context, problem statement, chosen solution, alternatives, and expected impact. Documenting decisions in this way helps teams reason about system sustainability, understand trade-offs more clearly, and maintain transparency as the system evolves. The metric is intended as a **completeness and quality indicator**, targeting strong architectural hygiene rather than high quantity of decisions.

## Calculation

**Formula:**  
\[
\frac{\text{Decisions documented with ADR-Light}}{\text{All significant architecture or data decisions}} \times 100
\]

The metric is calculated by dividing the number of significant architectural or data decisions documented using ADR-Light by the total number of such decisions within the iteration. The result is multiplied by **100** to represent the coverage as a percentage. Teams should aim for **≥ 80% coverage**, ensuring that most important decisions are captured while allowing flexibility where documentation adds limited value.

