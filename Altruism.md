
# Importing necessary libraries
```python
import matplotlib.pyplot as plt
import pandas as pd
import pylab as pl
import numpy as np
%matplotlib inline

```
# Loading the dataset
```python
!curl /content/sample_data/Altruism_Binary.csv
```
# Loading the dataset for display
```python
df = pd.read_csv("/content/sample_data/Altruism_Binary.csv")
```
# Displaying the first few rows of the dataset
```python
df.head()
```
# Descriptive statistics of the dataset
```python
print("\nDescriptive statistics of the dataset:")
print(df.describe())
```
# Selecting specific columns for analysis
```python
selected_columns = ['Year of Study', 'Age', 'Gender', 'Native Place']
cdf = df[selected_columns]
```
# Displaying the first few rows of the selected columns
```python
print("\nSelected columns for analysis:")
print(cdf.head(9))
```

# Visualizing histograms of selected columns
```python
print("\nHistograms of selected columns:")
cdf.hist()
plt.show()
```
# Scatter plot of Gender vs Age
```python
plt.scatter(cdf['Gender'], cdf['Age'], color='blue')
plt.xlabel("Gender")
plt.ylabel("Age")
plt.title("Scatter plot of Gender vs Age")
plt.show()
```
# Scatter plot of Year of Study vs Age
```python
plt.scatter(cdf['Year of Study'], cdf['Age'], color='blue')
plt.xlabel("Year of Study")
plt.ylabel("Age")
plt.title("Scatter plot of Year of Study vs Age")
plt.show()
```
