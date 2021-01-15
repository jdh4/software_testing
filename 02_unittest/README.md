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

The idea is to write code in a separate file that 

Note: It is common to feel like you are making up tests that will obviously work and don't see the point in doing. In this case remind yourself that characters do getting entered into code accidentally ("sneezing" or a developer working on little sleep, someone changes the source code for debugging) so continue writing these tests with in mind. Imagination plays an important role here but don't get carried away. You can always add more tests later.

Terminology: White box testing is when you write tests for code that you can see.


## Appendix

You can also put your testing inside the doc strings of code and have them run.
