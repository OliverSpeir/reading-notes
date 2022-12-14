# Pandas 

## Resources
- [Pandas in 10](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)
- [Pandas - Getting Started](https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/index.html)
- [Real Python - Pandas Tutorials](https://realpython.com/learning-paths/pandas-data-science/)
- [What is Pandas Video](https://www.youtube.com/watch?v=dcqPhpY7tWk)
- [Master Pandas](https://towardsdatascience.com/be-a-more-efficient-data-scientist-today-master-pandas-with-this-guide-ea362d27386)
- [pandas cookbook](https://pandas.pydata.org/pandas-docs/stable/user_guide/cookbook.html#cookbook)
- [intro to pandas data structures](https://pandas.pydata.org/pandas-docs/stable/user_guide/dsintro.html#dsintro)

## [Pandas in 10](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)

- [Object Creation](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#object-creation)
  - [Series](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.html#pandas.Series)
  - [DataFrame](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.html#pandas.DataFrame)
    - example features pandas built in [.date_range()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.date_range.html#pandas.date_range) method
- [Viewing Data](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#viewing-data)
  - [DataFrame.head()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.head.html#pandas.DataFrame.head) and [DataFrame.tail()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.tail.html#pandas.DataFrame.tail)
  -[.dtypes()]https://pandas.pydata.org/pandas-docs/stable/user_guide/basics.html#basics-dtypes)
    - passed value is index
    - view data from end or start
  - DaraFrame.index() and DataFrame.columns
    - index shows what seems to be primary key of data 
    - columns shows column names 
  - [DataFrame.to_numpy()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_numpy.html#pandas.DataFrame.to_numpy)
    - gives a NumPy representation of the underlying data
      - Note that this can be an expensive operation
    - NumPy arrays have one dtype for the entire array and pandas DataFrames have one dtype per column
  - [describe()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.describe.html#pandas.DataFrame.describe)
    - quick statistic summary of data
  - [DataFrame.sort_index()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.sort_index.html#pandas.DataFrame.sort_index)
    - sorts by axis
  - [DataFrame.sort_values()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.sort_values.html#pandas.DataFrame.sort_values)
    - sorts by value
- [Selection](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#selection)
  - DataFrame["column name"]
    - can also do DataFrame.column_name
  - Can [Select by Label](https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#indexing-label)
    - [DataFrame.loc()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.loc.html#pandas.DataFrame.loc)
      - `df.loc[label_name[0]]` or `df.loc["date_range_start":"date_range_end", ["column_a", "column_b"]]`
    - [DataFrame.at()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.at.html#pandas.DataFrame.at)
      - `df.at[label_name[0], "A"]`
  - [Selection by Position](https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#indexing-integer)
    - [DataFrame.iloc()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iloc.html#pandas.DataFrame.iloc)
    - [DataFrame.at()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.at.html#pandas.DataFrame.at)
  - Boolean indexing
    - condition
      - `df[df["A"] > 0]`
    - [ isin()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.isin.html#pandas.Series.isin)
- [Setting](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#setting)
    - set by label
    - set by position
    - assigning with NumPy array
    - can set with condition
- [Missing data](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#missing-data)
    - np.nan to fill in missing
    - [DataFrame.dropna()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.dropna.html#pandas.DataFrame.dropna)
      - drops missing data
    - [DataFrame.fillna()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.fillna.html#pandas.DataFrame.fillna)
      - argument fills missing values
  - [Operations](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#operations)
    - Operations in general exclude missing data.
    - DataFrame.mean
      - shows data on new axis
    - Operating with different dimensionality and needs alignment
      - `s = pd.Series([1, 3, 5, np.nan, 6, 8], index=dates).shift(2)`
- [Apply](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#apply)
    - [DataFrame.apply()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.apply.html#pandas.DataFrame.apply)
      - applies function
- [Histogramming and Discretization](https://pandas.pydata.org/pandas-docs/stable/user_guide/basics.html#basics-discretization)
- [String Methods](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#string-methods)
  - Series is equipped with a set of string processing methods in the str attribute
    - defaults to regex for pattern matching 
    - can use [Vectorized String Methods](https://pandas.pydata.org/pandas-docs/stable/user_guide/text.html#text-string-methods) alternatively
- [Merge](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#merge)
  - [ Merging section](https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html#merging)
  - [concat()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.concat.html#pandas.concat)
  - [merge()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.merge.html#pandas.merge)
- [Grouping](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#grouping)
  - Splitting the data into groups based on some criteria
  - Applying a function to each group independently
  - Combining the results into a data structure
  - [Grouping section](https://pandas.pydata.org/pandas-docs/stable/user_guide/groupby.html#groupby)
  - [sum()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.core.groupby.GroupBy.sum.html#pandas.core.groupby.GroupBy.sum)
- [Reshaping](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#reshaping)
  - [Hierarchical Indexing](https://pandas.pydata.org/pandas-docs/stable/user_guide/advanced.html#advanced-hierarchical)
  - [Reshaping](https://pandas.pydata.org/pandas-docs/stable/user_guide/reshaping.html#reshaping-stacking)
  -[stack()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.stack.html#pandas.DataFrame.stack) "compresses" a level in columns
  - [MultiIndex](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.MultiIndex.html#pandas.MultiIndex)
    - type of index aka primary key
  - [unstack()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.unstack.html#pandas.DataFrame.unstack)
- [Pivot Tables](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#pivot-tables)
  - [Pivot Tables](https://pandas.pydata.org/pandas-docs/stable/user_guide/reshaping.html#reshaping-pivot)
  - [pivot_table()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.pivot_table.html#pandas.pivot_table) pivots dataframe 
    - arguments specify values index and columns to pivot by
- [Time Series](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#time-series)
  - [Time Series section.](https://pandas.pydata.org/pandas-docs/stable/user_guide/timeseries.html#timeseries)
  - [Series.tz_localize()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.tz_localize.html#pandas.Series.tz_localize)
  - [Series.tz_convert()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.tz_convert.html#pandas.Series.tz_convert)
- [Categoricals](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#categoricals)
  - [API documentation](https://pandas.pydata.org/pandas-docs/stable/reference/arrays.html#api-arrays-categorical)
  - [Series.cat()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.cat.html#pandas.Series.cat) reorders and add missing categories returns new series
- [Plotting](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#plotting)
  - [Plotting Docs](https://pandas.pydata.org/pandas-docs/stable/user_guide/visualization.html#visualization)
  - plt.close closes figure window
  - [plot() ](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.plot.html#pandas.DataFrame.plot)
- [Importing and Exporting](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#importing-and-exporting-data)
  - can write to csv with [ DataFrame.to_csv()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_csv.html#pandas.DataFrame.to_csv)
  - [read_csv()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html#pandas.read_csv)
    - [Writing to a csv file](https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html#io-store-in-csv)
    - [Read csv file](https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html#io-read-csv-table)
- [HDF5](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#hdf5)
  - [HDFStores.](https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html#io-hdf5)
  - [DataFrame.to_hdf()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_hdf.html#pandas.DataFrame.to_hdf)
  - [read_hdf()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_hdf.html#pandas.read_hdf)
- [Excel](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#excel)
  - [write to excel with DataFrame.to_excel()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_excel.html#pandas.DataFrame.to_excel)
  - [read from excel with read_excel()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_excel.html#pandas.read_excel)
  - [Excel docs](https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html#io-excel)