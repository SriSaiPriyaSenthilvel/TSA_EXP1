# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 19.8.2024
<BR>

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity temperature.
<BR>

# ALGORITHM:
1. Import the required packages like pandas and matplot
<BR>

2. Read the dataset using the pandas
<BR>

3. Calculate the mean for the respective column.
<BR>

4. Plot the data according to need and can be altered monthly, or yearly.
<BR>

5. Display the graph.
<BR>
   
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
plt.plot(data.index, data['Temperature'], label='Temperature')
plt.title("Daily Minimum Temperature")
plt.xlabel("Date")
plt.xticks(rotation=45)
plt.ylabel("Temperature")
plt.grid(True)
plt.legend()
plt.show()

```

# OUTPUT:
![image](https://github.com/user-attachments/assets/57609a0f-ffe7-4560-8246-0a6f25b4df99)

<BR>

# RESULT:
Thus we have created the python code for plotting the time series of given data.
