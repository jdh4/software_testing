# Software Testing for Computational Researchers

This workshop is designed for anyone doing computational research that writes software toward a software tool or for data analysis. It is not designed

Don't try to become a professional software tester but if you are writing code toward software projects or writing data analysis code then you should spend some time writing tests for the software you write.


# Reasons to write tests

## It is easy to make mistakes

C/C++ allow for assignment in an if statement:

```c++
if (a = b) {
  // do work
}
```

Changes made between Python 2 and 3

```python
a = 1
b = 2
a / b  # equals 0 in Python 2
a / b  # equals 0.5 in Python 3
```

## Inspire confidence

By writing a test suite you will have confidence that at least all the test will run. Running the test suite is usually the first thing to do when a bug is found.

## Promotes writing proper code

If you can't write tests for your code then the structure and design choices of the code are probably poor. An example is a lengthy routine that writes to STDOUT and returns nothing.

## A test suite makes debugging easier

If you have a battery of tests for a certain piece of code then when a bug arises you can run the test suite to rule out potential problems.
