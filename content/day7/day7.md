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

## to give the series better index 
```python 
my_series = pd.Series([1,34,65,78,91], index= ['a','b', 'c', 'd', 'e'])
```
## accesing elements via given index
```python 
my_series
