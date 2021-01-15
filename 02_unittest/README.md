# Unit Testing

Unit testing involves writing tests for standalone units of code such as a function. You could write your own testing framework maybe
using the `assert` statement but it is better to use something that already exists.


# Self-written Test

```
def f(a, b):
  return a + b
```

```
assert f(1, 2) == 3
```

## unittest from the Python Standard Library

A good starting point for  unit testing is the the `unittest` module of the Python Standard Library. If you have Python installed then you have
this module.

```
$ python
>>> import unittest
```

