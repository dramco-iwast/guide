---
layout: default
title: Data Manipulation in Python
parent: Data Manipulation
nav_order: 2
has_toc: true
---


## Read CSV File

```python
# Import pandas (if no module named pandas -> pip install pandas)
import pandas as pd 

# Read csv file 
sensor_data = pd.read_csv("iwast.csv") 

# Show the first 5 entries
print(sensor_data.head(5))
```

## Filtering Data

```python
# replacing blank spaces with '_' because programming language do not like blank spaces!
sensor_data.columns =[column.replace(" ", "_") for column in sensor_data.columns] 

print(sensor_data.head(5))
  
# filter out data so we only keep the sensor dat coming from motherboard Marge with metric Temperature
marge_data = sensor_data.query('Motherboard_Name == "Marge" and metric=="Temperature"') 

print(marge_data.head(5))
```

## Plot Some Sensor Data
```python
import seaborn as sns; sns.set()
import matplotlib.pyplot as plt

# convert raw timestamps to datetime that pandas can understand
# raw: 2020-01-22T15:34:48.000Z
marge_data['timestamp'] =  pd.to_datetime(marge_data['timestamp'])
# ensure the values are interpreted as floats 
marge_data["value"] = marge_data["value"].astype(float)

# plot the temperature data and group based on the sensor_ID
ax = sns.scatterplot(x="timestamp", y="value", hue="Sensor_ID", data=marge_data)
plt.show()
```