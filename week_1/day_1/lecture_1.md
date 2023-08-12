# Lecture 1 (10:00 to 11:30)

# python review

## simple print function

```python
print('hello, world')
```
the result will be:

```console
$ python3 print.py
$ hello, world
$
```

note: the print function will add new line at the end by default
use end parameter to set your custom ending char

```python
print('hello world', end='-')
```

```console
$ python3 print.py
$ hello, world-
```

```python
print('hello world', end='-')
print('salam')
```

```console
$ hello, world-salam
$
```

for sake of speed I will just write python code.


as we see we can multiply strings (it will just repeat the string n times)
```python
a = 'salam'
a = a * 3
print(a)
```


but we can not use minus operand for strings
```python
a = 'salam'
a = a - 1 # problem
a = a = 'data' # problem
print(a)
```

## some python tool for checking compile error


1. pylint (https://pypi.org/project/pylint/)
2. pyright (https://github.com/microsoft/pyright)
3. pyflakes (https://pypi.org/project/pyflakes/)


## cython vs jython vs cpython vs ironPython vs pypy

+ https://linuxhint.com/cpython-jython-ironpython-pypy-cython/

+ https://github.com/python/cpython


## REPL (Read Evaluate Print Loop)

```console
$ python3
```

```
Python 3.8.10 (default, May 26 2023, 14:05:08)
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 2 + 2
4
>>>
```

### ipython

+ https://ipython.org/


``` console
$ ipython
```

```ipython
Python 3.8.10 (default, May 26 2023, 14:05:08)
Type 'copyright', 'credits' or 'license' for more information
IPython 8.12.2 -- An enhanced Interactive Python. Type '?' for help.

In [1]: print('salam')
salam

In [2]: 1 + 2 + 3
Out[2]: 6

In [3]:
```

## Float in python

+ https://link.springer.com/chapter/10.1007/978-3-319-50508-4_4

+ https://www.geeksforgeeks.org/floating-point-error-in-python/

```python
x = 0.1 + 0.2
print(x)
```

```console
$ 0.30000000000000004
```

note: python can handle really really big numbers (limited by memory volume)

## number formatting

underline will be ignored in numbers so we can use them for formatting  numbers:
``` python
x = 10_000_000_000
```

## divide in python

```python
result = 5 / 2
print(result) # prints 2.5
result = 5 // 2
print(result) # prints 2
```

## increment and decrement operation  

```python
x = 1
x += 1
print(x) # 2
x -= 1
print(x) # 1

```
+ note : we can use every math operation with this notation `var_name [operant]= value` and the result will be `var_name = var_name [operant] value`

## power operant in python

```python
x = 2 ** 4
print(x) # 16 
```
## complex number in python

```python
c = 1 + 2j # real part is 1 and imaginary part is 2
print(c.real)
print(c.imag)

```