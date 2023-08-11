# Lecture 1 (10:00 to 11:30)

## testing

```python
import unittest

def divideTowNumbers(a, b):
    if b == 0:
        raise ZeroDivisionError('division by zero!')
    return a / b


class TestDivideTowNumbers(unittest.TestCase):
    def test_divideSuccess(self):
        res = divideTowNumbers(10, 2)
        self.assertEqual(res, 5)

    def test_divideByZero(self):
        with self.assertRaises(ZeroDivisionError):
            divideTowNumbers(10, 0)
        



if __name__ == '__main__':
    unittest.main()


```