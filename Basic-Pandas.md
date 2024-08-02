# Introdction to Pandas [Pandas Documentation](https://pandas.pydata.org/docs/index.html)
Customarily, we import as follows:
```
import pandas as pd
```

## Essential basic functionality
* Head and tail
  To view a small sample of a Series or DataFrame object, use the head() and tail() methods. The default number of elements to display is five, but you may pass a custom number.
  ```
  df_sample.head()
  df_sample.tail(3)
  ```
* Descriptive statistics
  There exists a large number of methods for computing descriptive statistics and other related operations on Series, DataFrame.
  - Series: no axis argument needed
  - DataFrame: "index" (axis=0, default), "columns" (axis=1)
  ```
  sum(): sum of values
  mean(0): mean of values
  std(): Bessel-corrected sample standard deviation
  median(): arithmetic median of values
  cumsum(): cumulative sum
  ```
* Summarizing data
  There is a convenient describe() function which computes a variety of summary statistics about a Series or the columns of a DataFrame (excluding NAs of course):
  ```
  df_sample.describe()
  ```
  .columns provides access to the column labels of a data frame. It returns an index object representing the names of the columns in the DataFrame.
  ```
  df_sample.columns
  ```
* Data cleaning: working with missing data
  dropna() drops rows or columns with missing data
  DataFrame.dropna(*, axis=0, how=_NoDefault.no_default, thresh=_NoDefault.no_default, subset=None, inplace=False, ignore_index=False)
  ```
  df_sample.dropna() 
  df_sample.dropna(axis=1)
  
  
.shape()
.head()
.drop_duplicates()

