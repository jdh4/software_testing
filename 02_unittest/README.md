# Unit Testing with unittest

Unit testing involves writing tests for standalone units of code such as a function. You could write your own testing framework maybe
using the `assert` statement but it is better to use a framework that already exists.

### Validation vs. Verification

Verification involves not executing the code whereas validation does.


## unittest from the Python Standard Library

A good starting point for unit testing is the the [`unittest`](https://docs.python.org/3/library/unittest.html) module of the Python Standard Library. If you have Python installed then you have
this module.

```
$ module load anaconda3
$ python
>>> import unittest
```

The idea is to write code in a separate file that 

Note: It is common to feel like you are making up tests that will obviously work and don't see the point in doing. In this case remind yourself that characters do getting entered into code accidentally ("sneezing" or a developer working on little sleep, someone changes the source code for debugging) so continue writing these tests with in mind. Imagination plays an important role here but don't get carried away. You can always add more tests later.

Terminology: White box testing is when you write tests for code that you can see.

# Example

Consider a simple implemenation of a function to compute the area of a circle:

```python
import math

def circle_area(radius):
  return math.pi * radius**2
```

Let's test this script against different input values for radius:

```python
import math

def circle_area(radius):
  return math.pi * radius**2

radius_values = [2, 0, -3, 2 + 5j, True, "cat"]
for radius in radius_values:
  area = circle_area(radius)
  print(f"Area of circle with radius={radius} is {area}")
```

Run the script above with these commands:

```
$ cd software_testing/02_unittest
$ python area.py
Area of circle with radius=2 is 12.566370614359172
Area of circle with radius=0 is 0.0
Area of circle with radius=-3 is 28.274333882308138
Area of circle with radius=(2+5j) is (-65.97344572538566+62.83185307179586j)
Area of circle with radius=True is 3.141592653589793
Traceback (most recent call last):
  File "area.py", line 8, in <module>
    area = circle_area(radius)
  File "area.py", line 4, in circle_area
    return math.pi * radius**2
TypeError: unsupported operand type(s) for ** or pow(): 'str' and 'int'
```
