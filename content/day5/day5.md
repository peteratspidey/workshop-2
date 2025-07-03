# python basics
## string data type
### declare a string
```python
my_string = "hello vivek"
```
### check the type of the string
### len function
```python
len("my_string")
```
### replacing the string
```python
string.replace("vivek", "peter")
```
### indexing and slicing
```python
print(my_string[0])
print(my_string[5])
print(my_string[0:3])
print(my_string[0:3:2])
print(my_string[-1:-4:-1])

```
### concatenate the strings
```python
print("hello","world", "how", "are" ," you")
print ("hello"+"vivek"+ "how" +"are"+ "you")
```

### accessing the value of the variable in the print statement
```python
value = 3.14
print(" the value is :",value)
print("the value is : %.1f"  %value)
print ("the value is : %.2f" %value)
print ("the value is : %.3f" %value)
```

## list

### create a list
```python
my_list =[ 225,335,445]
print(my_list)
print(my_list[0:2])

```
### create a empty list
```python
my_new = [] # create a empty list
```
### add values to the list
```python
my_new.append(667)
my_new.append(668)
my_new.append(669)
print(my_new)
```
### for loop in my list
```python
for i in my_new:
    print(i)
for i in range(5):
    print(i)
```
### to run a loop and put the output in a list
```python
ls= [x for x in range(5)]
print(ls)
ls =2 [x for x in my_new]
print(ls2)
```


