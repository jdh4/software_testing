# Unit Testing

Unit testing involves writing tests for standalone units of code such as a function. You could write your own testing framework maybe
using the `assert` statement but it is better to use a framework that already exists.


# Self-written Test

```
def f(a, b):
  return a + b
```

```
assert f(1, 2) == 3
```

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


## doctest

There is a fundamentally different approach to testing using the [`doctest`](https://docs.python.org/3/library/doctest.html) module. This involves writing tests inside the docstrings and then executing these tests. The advantage of this approach is it combines writing documentaion with testing. Both of these tend to get neglected. For researchers who are trying to write some tests and some documentation this may be the best approach for you.
