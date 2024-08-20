# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
NAME: SRI SAI PRIYA S
REGISTER NUMBER: 212222240103
```
```
import pandas as pd
import zipfile
import matplotlib.pyplot as plt

# Load the zipped CSV file directly
with zipfile.ZipFile('/content/powerconsumption.csv (2).zip') as z:
    with z.open(z.namelist()[0]) as f:
        data = pd.read_csv(f)

# Check the column names
print(data.columns)

# Use 'Datetime' instead of 'Date'
data['Datetime'] = pd.to_datetime(data['Datetime'])

# Set 'Datetime' as the index
data.set_index('Datetime', inplace=True)

# Plot the temperature data
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

![image](https://github.com/user-attachments/assets/58cb6ec8-6f54-44ba-97cd-5276822b5630)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
