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

x = 123
str = f"number: {x}"
print(str) # number: 123
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

# generating list
lst = [x**2 for x in range(1, 5) if x > 2]
print(lst) # [9, 16]

# deleting
lst = [1,2,3]
del lst[1]
print(lst) # [1, 3]
```


### Tuples
```python
tpl = 1,2,3
print(tpl) # (1, 2, 3)

tpl = (1,2,3)
print(tpl) # (1, 2, 3)

tpl = (1,2,3)
tpl[2] = 0 # ERROR
```


### Sets
```python
st = {1, 2, 3}
print(st) # {1, 2, 3}

st = {1, 2, 3, 3}
print(st) # {1, 2, 3}
```


### Dicts
```python
dct = {'name': 'Denys', 'level': 'good'}
print(dct) # {'name': 'Denys', 'level': 'good'}


dct = dict([('name', 'Denys'), ('level', 'good')])
print(dct) # {'name': 'Denys', 'level': 'good'}


for k, v in dct.items():
  print(k, ':', v)

# name : Denys
# level : good
```


### Unpacking
```python
pck = [1,10]
a,b = pck
print(a)              # 1
print(b)              # 10
print(pck)            # [1, 10]
print(*pck)           # 1 10
print(pck[0], pck[1]) # 1 10
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


for i,v in enumerate(lst):
  print(n)
  
# 0 : 1
# 1 : 5
# 2 : 8


# prints 0,1,2,3,4: 
for i in range(5):
  print(i)
```


### Functions
```python
def sqr(x, p = 2):
  return x**p

print(sqr(8)) # 64
print(sqr(p=3, x=2)) # 8


# list of arguments
def test(*args, **keys):
  print(args)
  print(keys)

test('woa', a=1, b='!') # ('woa',)
                        # {'a': 1, 'b': '!'}


# lambda
l = lambda x: x ** 2
print(l(2)) # 4
```


### Files
```python
# reading file
with open('test.py') as f:
  data = f.read()
  print(data)

# writing file
with open('/tmp/test', 'w') as f:
  f.write('hi')
```


### Exceptions
```python
try:
  raise ValueError('hi')
except ValueError as v:
  print(v) # catch exception and print it's error message
```


### Classes
```python
class MyClass:
  name = 'Denys' # class variable

  def __init__(self, age): # constructor
    self.age = age # instance variable

  def get_age(self): # method
    return self.age # return instance variable

me = MyClass(37)
print(me.name, me.get_age())
```


### OOP
```python
# inheritance
class Iam(MyClass): # Iam inherits MyClasa
  name = 'Denys'
```

### Iterators
```python
def down_from(max):
  for index in range(max, 0, -1):
    yield index

for i in down_from(4):
  print(i)
  
# 4
# 3
# 2
# 1
```

### Multi-threading
```python
import threading, time

class AsyncHi(threading.Thread): # inherit class to allow multi-threading
    message = 'no'

    def run(self):
        time.sleep(2)
        self.message = 'hi'


test = AsyncHi()
test.start() # exec "run" in background
print(test.message)

time.sleep(3)

print(test.message);
```
