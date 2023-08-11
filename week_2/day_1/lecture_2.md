# Lecture 2 (12:00 to 13:30)






## magic methods


we are implementing simple class for math operation for rational number :

```python
from math import gcd

class Rational:
    def _simplify(self):
        if self._denom < 0:
            self._denom = -self._denom
            self._num = -self._num
        g = gcd(self._num, self._denom)
        self._num //= g
        self._denom //= g
        
    def __init__(self, n, d = 1):
        if d == 0:
            raise ValueError('Invalid denom')
        self._num = n
        self._denom = d
        self._simplify()
        
    def getNum(self):
        return self._num
    
    def getDenom(self):
        return self._denom
    
    def setNum(self, n):
        self._num = n
        self._simplify()
        
    def setDenom(self, d):
        self._denom = d
        self._simplify()
        
    def __add__(self, right):
        if type(right) in [int]:
            right = Rational(right, 1)
        n = self._num * right._denom + self._denom * right._num
        d = self._denom * right._denom
        return Rational(n, d)

    def __eq__(self, right):
        return self._num == right._num and self._denom == right._denom
    
    def __radd__(self, left):
        return self + left
    
    def __str__(self):
        if self._denom == 1:
            return str(self._num)
        return f'{self._num}/{self._denom}'

    def __repr__(self):
        if self._denom == 1:
            return str(self._num)
        return f'{self._num}/{self._denom}'
```

+ '`__init__()`' :
  + data
+ '`__str__()`'
+ '`__eq__()`'
+ '`__radd__()`'
+ '`__add__()`'
+ '`__repr__()`'
+ '`__getattribute__()`'
+ '`__setattr__()`'

## inheritance