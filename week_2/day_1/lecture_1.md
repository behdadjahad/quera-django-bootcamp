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


```python
def function(x)
```


we can have object property in python which can access without creating new object

```python
class Circle:

    data = 10
    radius = 0

    def __init__(self, r):
        self.radius = r


c = Circle(2)

print(c.radius)
print(Circle.data)
print(Circle.radius)


```

```python
class Account:
    rate = 0.2

    def __init__(self, balance):
        self.balance = balance

    def get_balance(self):
        return (self.balance * self.rate) + self.balance

```


we can validate data in object constructor

```python
class Circle:

    def __init__(self, r):
        if type(r) != type(int):
            raise ValueError('invalid radius.')
        if r < 0 : 
            raise ValueError('invalid radius.')
        self.r = r

    def getArea(self):
        return self.r ** 2 * 3.14

    def getPerimeter(self):
        return self.r * 2 * 3.14


```


as we see we can add custom property to the python objects that only available for that specific object
```python
class Circle:

    def __init__(self, r, isDebug):
        self.r = r

        if isDebug:
            self.verbose = 10 
            self.help = True
        else:
            self.log = False

c1 = Circle(1, True)
c1.x = 20
c1.y = 10


c2 = Circle(1, False)

print(dir(c1))
print(dir(c2))

```


we can use '`_`' and '`__`' for naming our properties and it will act like private property 

we can access the private property but it will not recommend by IDE or code editor  
```python
class Circle:

    def __init__(self, r):
        self.r = r
        self._isPrivate = True
        self.__radius = r


c1 = Circle(1)
print(c1.r)
print(c1._isPrivate)
print(c1._Circle__radius) # works fine
print(c1.__radius) # will throw an exception
```


we can use classmethod decorator for making them available at class level (no need for instantiating new object)


```python

class Test:
    testField = 0

    def testMethod(self, x, y):
        return x + y

x = Test()

print(x.testMethod(10, 20))

print(Test.testMethod(10, 20)) # will throw an exception

```


```python

class Test:
    testField = 1

    @classmethod
    def testMethod(self, x, y):
        return x + y

x = Test()
print(Test.testMethod(10, 20))
print(x.testMethod(10, 20))

```

staticmethod used for creating methods that dose not need object or class reference (this definition may not be accurate)

```python
class myMath:
    @staticmethod
    def pow(x, y):
        return x ** y

print(myMath.pow(10, 2))
```