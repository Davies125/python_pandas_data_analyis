## Pandas Data Analysis and Manipulation

### Overview
Pandas is a powerful library for **data manipulation and analysis**. This project covers key concepts such as:
- Understanding **Series** and **DataFrames**
- Importing data from different formats (CSV, Excel, SQL)
- Indexing and selecting data using `loc` and `iloc`
- Handling missing data and data transformations
- Filtering data and applying conditions

### Why Choose Python for Data Analysis?
✅ Easy to learn and use  
✅ Handles real-world messy and incomplete data  
✅ Supports multiple data formats (CSV, JSON, Excel, SQL)  

## Core Data Structures in Pandas
### **1. Series**
A **one-dimensional labeled array** that can hold any data type.
```python
import pandas as pd
series = pd.Series([10, 20, 30, 20], index=['a', 'b', 'c', 'd'])
print(series)
```

### **2. DataFrame**
A **two-dimensional data structure** that holds multiple data types.
```python
# Creating a DataFrame
import pandas as pd

data = {
    'Name': ['Simon', 'Caroline', 'Bernice'],
    'Age': [34, 28, 21],
    'City': ['New York', 'Paris', 'London']
}
df = pd.DataFrame(data)
print(df)
```

## Data Import
Pandas supports importing data from various sources:
```python
# Read a CSV file
df = pd.read_csv('filename.csv')

# Read an Excel file
df = pd.read_excel('filename.xlsx')

# Read from SQL database
df = pd.read_sql('SELECT * FROM table_name', connection)
```

## Indexing and Data Selection
### **Using `iloc` (Integer-location based selection)**
```python
# Select third row
df.iloc[2]

# Select first three rows
df.iloc[0:3]
```

### **Using `loc` (Label-based selection)**
```python
# Select row by label
df.loc['Simon']

# Select multiple rows
df.loc[['Simon', 'Bernice']]
```

## Filtering Data
We use `&` instead of `and` when working with Pandas DataFrames because `&` is designed for **element-wise** operations.
```python
# Filter rows where Age > 25 and City is 'New York'
df_filtered = df[(df['Age'] > 25) & (df['City'] == 'New York')]
print(df_filtered)
```

## Additional Filtering Examples
Pandas allows for more complex filtering conditions.
```python
# Filtering rows where Age is greater than 25 or City is 'London'
df_filtered = df[(df['Age'] > 25) | (df['City'] == 'London')]
print(df_filtered)

# Filtering rows where Age is between 20 and 30
df_filtered = df[(df['Age'] >= 20) & (df['Age'] <= 30)]
print(df_filtered)
```

## Running the Project
To execute the notebook:
1. Install dependencies: `pip install pandas`
2. Run the Jupyter Notebook: `jupyter notebook`
3. Open and execute the cells.

## Conclusion
This project provides a solid foundation in **Pandas for data analysis**. It covers key **data manipulation techniques**, indexing, and filtering using `loc` and `iloc`. Feel free to **contribute** or **extend** the analysis further!

