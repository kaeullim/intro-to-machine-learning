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
  DataFrame.dropna(*, axis=0, how=_NoDefault.no_default, thresh=_NoDefault.no_default, subset=None, inplace=False, ignore_index=False): drops rows or columns with missing data
  - axis : {0 or 'index', 1 or 'columns'}, default 0
  - how : {'any', 'all'}, default 'any'
  - thresh : int, optional
  - subset : column label or sequence of labels, optional
  ```
  df_sample.dropna() 
  df_sample.dropna(axis=1)
  ```
* Data organization  
  Pandas groupby function is used to split the data into groups based on some criteria. It makes the task of splitting the DataFrame over some criteria really easy and efficient.
  '''
  DataFrame.groupby(by=None, axis=0, level=None, as_index=True, sort=True, group_keys=True, squeeze=False, **kwargs)
  - First grouping based on "Team"
  - Within each team we are grouping based on "Position"
  groups = df_sample.groupby(['Team', 'Position'])
  '''
  '''
  DataFrameGroupBy.agg(arg, *args, **kwargs)
  >>> df = pd.DataFrame({'A': [1, 1, 2, 2],
  ...                    'B': [1, 2, 3, 4],
  ...                    'C': np.random.randn(4)})
  >>> df
     A  B         C
  0  1  1  0.362838
  1  1  2  0.227877
  2  2  3  1.267767
  3  2  4 -0.562860
  >>> df.groupby('A').agg({'B': ['min', 'max'], 'C': 'sum'})
      B             C
    min max       sum
  A
  1   1   2  0.590716
  2   3   4  0.704907
  ```


