# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 20-04-2026

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
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("C:/Users/admin/Downloads/nifty50_2000_2025.csv")
df.columns = df.columns.str.strip()
# Convert date
df["Date"] = pd.to_datetime(df["Date"])
df.head()

df.info()
df.describe()

df_stock = df[df["Stock"] == "ITC.NS"]
plt.figure(figsize=(12,5))
plt.plot(df_stock["Date"], df_stock["Close"], linewidth=2)
plt.title("ITC Stock Price Trend")
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```







# OUTPUT:

<img width="1003" height="269" alt="image" src="https://github.com/user-attachments/assets/f855dd3d-a019-44f9-a913-2c92be5f0b23" />
<img width="1003" height="248" alt="image" src="https://github.com/user-attachments/assets/1b42027e-5bbf-4582-9690-ccf43c7e09d5" />
<img width="998" height="457" alt="image" src="https://github.com/user-attachments/assets/60b511f4-1e10-47dc-892c-2d4e464a501e" />



# RESULT:
Thus we have created the python code for plotting the time series of given data.
