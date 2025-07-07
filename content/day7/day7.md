# panda
## installation of panda into jupyter
***panda is a library used for data analysis and data manipulation***

```python
pip install pandas
```
> type this and execute into jupyter notebook  and run using key `SHIFT` + `ENTER`
> restart kernel from kernel tab

## create a series
```python
my_series = pd.Series([1,34,65,78,91])
```

### to give the series better index 
```python 
my_series = pd.Series([1,34,65,78,91], index= ['a','b', 'c', 'd', 'e'])
```
### accesing elements via given index
```python 
print(my_series['a'])
print(my_series[:3])
print(my_series[2:4])
print(my_series.mean())
print(my_series.median())
```
## creating a data frame usind dictionary of series
```python 
d2 = {'one':45, 'two': 98}
print(d2)
```
### using given indexes

```python
d2 = {'one':pd.Series([1,34,65,78,91], index= ['a','b', 'c', 'd', 'e']), 'two': pd.Series([72,456,98,42,396], index= ['f','g', 'h', 'i', 'j'])}
type(d2)
```
### convert this into data frame
```python 
my_df = pd.DataFrame(d2)
print(my_df)
```
### with same given index
```python
d2 = {'one':pd.Series([1,34,65,78,91], index= ['a','b', 'c', 'd', 'e']), 'two': pd.Series([72,456,98,42,396], index= ['a','b', 'c', 'd', 'e'])}
my_df = pd.DataFrame(d2)
my_df
my_df.index
my_df.columns
```
### with no index
```python
d2 = {'one':pd.Series([1,34,65,78,91]), 'two': pd.Series([72,456,98,42,396])}
my_df = pd.DataFrame(d2)
my_df
my_df.index
my_df.columns
type(my_df)

```

## import csv file and check the head of the file
```python
my_csv = pd.read_csv("data.csv")
my_csv.head()
```
### to import the excel file into here
```python
pip install openpyxl
my_csv2 = pd.read_excel("data.xlsx")
my_csv2 # to check the excel sheet
my_csv2.columns # to check the cloumn header
my_csv2.values # to check the values of the table 
my_csv2.describe # to get deep details of the table
my_csv2["Pulse"] # to print the table
my_csv2[["Pulse"]] # to print the concatenate dataframe
my_csv2[["Pulse", "Date"]] # to print the multiple dataframe
my_csv.loc[0] # acces all the column where rows index is 0
my_csv.loc[[2]] # acces all the column where rows index is 2
my_csv.loc[[2,5]] # # acces all the column where rows are 2-5

```
> note: use double times[] is useful for better representation

