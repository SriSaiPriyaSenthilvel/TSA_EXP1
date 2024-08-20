# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 19.8.2024
<HR>

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity temperature.
<HR>

# ALGORITHM:
1. Import the required packages like pandas and matplot
<HR>

2. Read the dataset using the pandas
<HR>

3. Calculate the mean for the respective column.
<HR>

4. Plot the data according to need and can be altered monthly, or yearly.
<HR>

5. Display the graph.
<HR>
   
# PROGRAM:
```
NAME: SRI SAI PRIYA S
REGISTER NUMBER: 212222240103
```
```
import pandas as pd
import zipfile
import matplotlib.pyplot as plt
with zipfile.ZipFile('/content/powerconsumption.csv (2).zip') as z:
    with z.open(z.namelist()[0]) as f:
        data = pd.read_csv(f)
print(data.columns)
data['Datetime'] = pd.to_datetime(data['Datetime'])
data.set_index('Datetime', inplace=True)
plt.figure(figsize=(10, 6))
plt.plot(data.index, data['PowerConsumption_Zone2'], label='Zone 1')
plt.title("Power Consumption - Zone 1")
plt.xlabel("Date")
plt.xticks(rotation=45)
plt.ylabel("Power Consumption")
plt.grid(True)
plt.legend()
plt.show()
```

# OUTPUT:
![image](https://github.com/user-attachments/assets/5d426f53-0096-4cc9-8687-b46cb4bf737b)

<HR>

# RESULT:
Thus we have created the python code for plotting the time series of given data.
