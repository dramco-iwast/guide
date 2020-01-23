---
layout: default
title: Data Manipulation in Python
parent: Data Manipulation
nav_order: 2
has_toc: true
---

```python
# Import pandas 
import pandas as pd 

# Read csv file 
sensor_data = pd.read_csv("iwast.csv") 

# Show the first 5 entries
print(sensor_data.head(5))
```
