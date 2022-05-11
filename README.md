# Python Notes
Python programming language short notes for students like me

### Basics

```python
# Ints
var = 123
print(var)


# Floats
var = 123.12
print(var)


# Strings
var = 'first_line\nsecond_line'
print(var)


# Multiline strings
var = """
many lines
...
last line
"""
print(var)


# Concatenation
print('hi' + ' ' + 'all')
```


### Strings
 ```python
 str = 'hi all'

# length
print(len(str)) # 6

# character
print(str[1]) # i

# substring
print(str[0:4]) # hi a
print(str[-3:]) # all
print(str[:2]) # hi
```


### Lists
```python
lst = [1, 3, 6, 8]

# length
print(len(lst)) # 4

# indexes
print(lst) # [1, 3, 6, 8]
print(lst[1]) # 3
print(lst[1:3]) # [3, 6]

# conncatenate
print(lst + [9, 10]) # [1, 3, 6, 8, 9, 10]

# adding values
lst.append(11)
print(lst) # [1, 3, 6, 8, 11]
```



# If
```python
if x > 1:
  print('ok')
elif x == 0:
  print('zero')
else:
  print('notok')
```


# For
```python
lst = [1,5,8]

for n in lst:
  print(n)

# 1
# 5
# 8
```
