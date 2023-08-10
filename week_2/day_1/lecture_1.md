# Lecture 1 (10:00 to 11:30)

## OOP


`__init__` method is constructor in python.

`self` is equivalent of `this` in java or c++ programming which points to the object.

there are some methods by default in every python class which starts with '`__`' and we call it magic methods like `__init__` and `__str__`.

```python
class Circle:
    def __init__(self, r):
        self.radius = r


c = Circle(2)


print(c)
print(type(c))
print(dir(c))

```

python compares object by their reference

note: `is`  operation always compare the reference 
```python
c1 = Circle(5)
c2 = Circle(5)

print(c1 == c2)
print(c1 is c2)

c1 = c2

print(c1 == c2)
print(c1 is c2)
```