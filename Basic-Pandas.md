# Introdction to Pandas
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
  sum()
  mean(0)
  ``` 
.shape()
.head()
.drop_duplicates()
.dropna()
