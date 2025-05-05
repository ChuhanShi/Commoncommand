### 🔹 **1. Importing and Setup**

`import pandas as pd`

---

### 🔹 **2. Creating DataFrames**

`df = pd.DataFrame(data)           # From dict, list of dicts, etc.`
`df = pd.read_csv('file.csv', parse_dates = ['Time'])      # Load from CSV` 
`df = pd.read_excel('file.xlsx')   # Load from Excel`
`df = pd.DataFrame(np.array(...))  # From NumPy array`

---

### 🔹 **3. Viewing and Inspecting**

`df.head(n)            # First n rows` 
`df.tail(n)            # Last n rows` `
`df.info()             # Summary of DataFrame`
`df.describe()         # Summary statistics` 
`df.shape              # (rows, columns)` 
`df.columns            # Column names` 
`df.index              # Index range` 
`df.dtypes             # Data types`

---

### 🔹 **4. Selecting and Filtering**

`df['col']                     # Select column`
`df[['col1', 'col2']]          # Select multiple columns` 
`df.loc[row_label]             # By label`
`df.iloc[row_index]            # By index`
`df.loc[:, 'col']              # All rows, specific column` 
`df[df['col'] > value]         # Conditional filtering`

---

### 🔹 **5. Adding/Modifying/Deleting Columns**

`df['new_col'] = value              # Add column` 
`df['col'] = df['col'].apply(func)  # Modify with function` 
`df.drop('col', axis=1, inplace=True)  # Drop column`

---

### 🔹 **6. Handling Missing Data**

`df.isnull()               # Detect NaNs` 
`df.notnull() df.dropna()               # Drop rows with NaNs` 
`df.fillna(value)          # Fill NaNs with value` 
`df.interpolate()          # Fill NaNs via interpolation`

---

### 🔹 **7. Aggregation and Statistics**

`df.mean(), df.median() df.sum()`
`df.min(), df.max()` 
`df.std(), df.var()`
`df['col'].value_counts()`
`df.agg({'col1': 'mean', 'col2': 'sum'})  # Multiple aggregations`

---

### 🔹 **8. Grouping**

`df.groupby('col').mean()` 
`df.groupby(['col1', 'col2']).agg(['mean', 'sum'])`

---

### 🔹 **9. Sorting**

`df.sort_values('col')                # Ascending` 
`df.sort_values('col', ascending=False)  # Descending df.sort_index()`

---

### 🔹 **10. Merging & Joining**

`pd.merge(df1, df2, on='key')        # Merge on common key` 
`df1.join(df2, how='left')           # Join by index` 
`pd.concat([df1, df2], axis=0)       # Stack rows` `
`pd.concat([df1, df2], axis=1)       # Combine columns`

---

### 🔹 **11. Reshaping**

`df.pivot(index, columns, values)` 
`df.melt(id_vars, value_vars)` 
`df.stack(), df.unstack()` 
`df.transpose() or df.T`

---

### 🔹 **12. Date and Time**

`df['date'] = pd.to_datetime(df['date'])` 
`df['date'].dt.year, .dt.month` 
`df.set_index('date')` 
`df.resample('D').mean()             # Downsampling`

---

### 🔹 **13. String Operations**

`df['col'].str.lower(), .str.upper()`
`df['col'].str.contains('text')`
`df['col'].str.replace('old', 'new')`

---

### 🔹 **14. Exporting**

`df.to_csv('file.csv', index=False)` 
`df.to_excel('file.xlsx')`
`df.to_json('file.json')`

---