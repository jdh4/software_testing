# Non-Functional Testing

Everything up to this point has been functional testing where we have looked to see if the outputs agree with the expect outputs. Non-functional
testing looks at other aspects such as computational complexity, scalability, etc.

## Computation complexity

Consider the simple code below:

```
N = 1000
for i in range(N):
    x_sum += x[i]
```

What is the computational complexity in time and memory for this `for` loop? The answer is that the memory requirement grows linearly with N
and so does the execution time of the code. That is, if N is double the code requires twice as much memory and twice as much runtime.

What about this example?

```
x_min = 0.0
N = 1000
for i in range(N - 1):
    for j in range(i + 1, N):
        xij = abs(x[i] - x[j])
        if xij < x_min: x_min = xij
```

## Python sort

```python
from random import random
from time import perf_counter

times = []
for N in map(int, [10, 100, 1000, 10000, 100000, 1e6, 1e7, 1e8]):
  x = [random() for _ in range(N)]
  t0 = perf_counter()
  x.sort()
  times.append((N, perf_counter() - t0))
```
