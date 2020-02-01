---
layout: default
title: What are thresholds?
parent: Configuration
nav_order: 2
---

Some sensors are able to generate an interupt when a certain metric value is exceeded.
When enabled, you will receive an update of the metric value if the threshold is exceeded.

We allow to define two thresholds, i.e., threshold low and threshold high. 
When a metric value exceeds the `threshold high (TH)` an interrupt is generated.
In contrast, only when a metric value goes below `threshold low (TL)` an interrupt occurs.
This allow us to get updates in three distinct manners.

In all cases an interrupt is generated when the metric value exceeds `TH` or when is falls below `TL`. When playing with the `TH` and `TL` configuration we can manipulate when we want an update.


1. If we are interested when a value is higher than `TH` or lower than `TL`, we define: `TH` with a higher value as `TL`.

2. If we are interested when a value enters the area between `TH` and `TL`,  `TL` has a higher value than `TH`.

3. If we want to know when a metric value crosses a specific value, we can define `TH` equal to `TL`.

![](../assets/images/tl-th-thresholds.svg)