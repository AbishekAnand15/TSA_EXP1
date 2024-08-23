### Developed By: ABISHEK XAVIER A
### Register No: 212222230004
### Date:

# Ex.No: 01A PLOT A TIME SERIES DATA


## AIM:
To analyze and visualize the sales trends of a furniture store over time by creating a time series plot.

## ALGORITHM:


 1.Import the necessary libraries: Import pandas, numpy, and matplotlib.pyplot.
 
 2.Load the CSV data: Use pandas.read_csv to load the first 50 rows of the data from index.csv into a DataFrame.
 
 3.Preview the data: Use DataFrame.head() to display the first 10 rows of the DataFrame.
 
 4.Group and count data: Group the data by date and coffee_name, then count the occurrences for each group.
 
 5.Create the plot: Use matplotlib to create a line plot that shows the count of each coffee_name by date.
 
 6.Customize the plot: Add a title, labels, and rotate the x-axis labels for better readability.
 
 7.Display the plot: Use plt.show() to display the final plot.
  <br />
  <br />


## PROGRAM:


```python

import pandas as pd
import matplotlib.pyplot as plt


data = pd.read_csv('/content/Super_Store_data.csv',encoding='ISO-8859-1')  


data['Order Date'] = pd.to_datetime(data['Order Date'])

furniture_data = data[data['Category'] == 'Furniture']

furniture_sales = furniture_data.groupby('Order Date')['Sales'].sum().reset_index()

# Plot the time series
plt.figure(figsize=(14, 7))
plt.plot(furniture_sales['Order Date'], furniture_sales['Sales'], marker='o', color='b')
plt.title('Furniture Sales Over Time')
plt.xlabel('Date')
plt.ylabel('Sales')
plt.grid(True)
plt.show()
```
<br />
<br />
<br />
<br />

## OUTPUT:
![Screenshot 2024-08-23 215425](https://github.com/user-attachments/assets/4d158fc6-1c6d-4d44-a064-29a0eababb82)


# RESULT:
Thus we have created the python code for plotting the time series of given data.
