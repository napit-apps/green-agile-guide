---
layout: default
title: Cache Hit Rate
nav_order: 3
parent: Operations & Observability
permalink: /metrics-and-impact/operations-and-observability/cache-hit-rate
---

# Cache Hit Rate (%)

environmental  
{: .label .label-green }

governance  
{: .label .label-green }

direct  
{: .label .label-purple }

This metric measures the **percentage of requests that are served from cache instead of being processed by the underlying system**. It makes visible how effectively caching mechanisms reduce load on databases, services, and infrastructure.

In a Green Agile context, Cache Hit Rate connects **performance optimization with energy and resource efficiency**. Serving requests from cache typically requires significantly less compute, memory access, and network traffic than processing them end‑to‑end, resulting in lower latency and reduced energy consumption.

## Classification

{: .classification }
>
> - **Category:** Operations & Observability  
> - **Measurement Frequency:** per iteration  
> - **Responsibility:** Engineering Team

## Impact
A high cache hit rate indicates that repeated or predictable requests are efficiently reused instead of recomputed. This reduces system load, improves response times, and lowers energy consumption across the runtime environment. It also increases system resilience under high traffic by protecting backend services from unnecessary load.

Because this metric directly reflects how many requests avoid full processing, it represents a **direct environmental impact**. At the same time, it acts as a governance lever by encouraging thoughtful cache strategies, data freshness rules, and invalidation policies.

## Calculation

The Cache Hit Rate is calculated as the ratio of cache hits to all cache lookups:

$$
\text{Cache Hit Rate} =
\frac{\text{Cache Hits}}{\text{Cache Hits} + \text{Cache Misses}} \times 100
$$

A value of **≥ 90%** is often considered a good reference point, though the appropriate target depends on the specific use case, data volatility, and correctness requirements.

## Example

Assume a service processes **50,000 cache lookups** during an iteration. Monitoring shows:

- Cache Hits: 46,000  
- Cache Misses: 4,000  

Using the formula:

$$
\frac{46\,000}{46\,000 + 4\,000} \times 100 = 92\%
$$

This result indicates an effective caching strategy. If the hit rate drops in subsequent iterations, the team may investigate cache invalidation logic, data freshness constraints, or newly introduced request patterns.

---
<div style="display: flex; justify-content: space-between;">
  <a href="/metrics-and-impact/operations-and-observability/cpu-time-per-transaction" style="text-small">← CPU Time per Transaction</a>
  <a href="/metrics-and-impact/operations-and-observability/energy-per-release" style="text-small">Energy Consumption per Release →</a>
</div>