# Lecture 2 (12:00 to 13:30)


## stderr vs stdout vs stdin

+ note: stdout will use for common output data but stderr will use for error outputs
+ when we write the result of our program to a file only stdout will writes to the file
+ when we get input from user it will use stdin

```python
import sys

print("this is stderr", file=sys.stderr)

```

+ note : we can print prompt in `input()` function and the default type of input function is str.
```python 
inp = input('please enter your name:')

print(inp)
print(type(inp))
print(type(1))
```

## multi line string 'literal string'

```python

string = """hi this string
can be multi line 
and what ever we write it will print it, "literally"."""

print(string)
```

## multi line command

```python 
print(
    type(1
    )
    ,
    "hi"
    ,
    type(
        'ok'
    )
)

```

+ note : we can use '`\`' to inform python that we want to break our line in irregular places.

```python

print \
("this is \
only for sake of learning and no one acutely use it like \
this.")
```



+ note : we use indentation to specify block of code in python (4 spaces fo every block)
+ and we can use `pass` keyword for creating empty block
```python
a = 1

if a == 1:
    print('in if block')
print('out of if block')


if True:
    pass

```

## python scripts

+ we use '`#!/usr/bin/env python3`' to address the python that we want to run this script with
+  '`#!/usr/bin/python3`' can be use too
```python
#!/usr/bin/env python3

a = input()
print(a)
if (a == 2) and (a == 3):
    if a == 2:
        print("ok")
    print("ok")
    if a == 3:
        pass
print('end')
```

## convert str to int

+ note : python can parse str to int if the str contains only digits or it will cause an error

```python
a = int(input())
print(a)
if (a == 2) and (a == 3):
    if a == 2:
        print("ok")
    print("ok")
    if a == 3:
        pass
print('end')
```


## conditions in python

as we know `if` keyword is used for condition

```python
x = 10
y = 20

if x == y:
    print('x equal y')

if x <= y:
    print('x less than or equal y')

if x >= y:
    print('x grater than or equal y')

if x < y:
    print('x less than y')

if x > y:
    print('x grater than y')

if x != y:
    print('x not equal y')


is_user_valid = True
is_user_authenticated = True

if is_user_valid and is_user_authenticated:
    print('show them the content')

token_expires = True
session_open = True

if token_expires or not session_open:
    print('do not show them the content')

day = input('please enter the day of the week:')

if day == 'shanbe':
    pass
elif day == 'yekshanbe':
    pass
elif day == 'doshanbe':
    pass
else:
    pass


```

## bitwise operation
we don't really need them
```python
x = 1 | 2
y = 2 & 1
```

## loop in python


### for loop
```python
a = int(input())


# counts from 0 to a-1
for i in range(a):
    print(i)


# counts from 1 to a-1
for i in range(1, a):
    print(i)


# counts from 1 to a-1 and increment 2 (step)
for i in range(1, a, 2):
    print(i)


print(list(range(-5, 11, 3)))

```

### while loop

```python
while True:
    print(1)


i = 0
while i < 100:
    print(i)
    i += 1
```

### for-else and while-else

```python
for i in range(10):
    if i == 5:
        break
else:
    print('in for else (if for dose not break)')


while i < 10:
    if i == 5:
        break
else:
    print('in while else(if while dose not break)')
```

## string in python


+ python has lots of built in methods for working with strings 

```python

a = '    salam ChetorI   '
print(a.upper())
print(a.lower())
print(a.capitalize())
print(a.startswith('sa'))
print(a.endswith('i'))
print(a.isalnum())
print(a.isalpha())
new_a = a.replace('a', 'A')
print(new_a)
print(a.strip())
print(a.replace('a', ''))
print(a.swapcase())
print(a)

print('salam' in a)
print('z' in a)

print('salam\nkhubi?')
print(r'salam\nkhubi?')
```


## pep8

python standard guid lines
+ https://peps.python.org/pep-0008/


for example its better to not write 2 excretions in one line

and every indent should be 4 spaces

```python
a = input() ; b input()
```

there is a tool for this kind of work that called '`black`'

+ https://pypi.org/project/black/