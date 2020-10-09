# Comp Thinking Quiz 1

## Q1: A Plus Abs B

Fill in the blanks in the following function for adding `a` to the absolute value of `b`, without calling `abs`. You may **not** modify any of the provided code other than the two blanks.

```python
from operator import add, sub

def a_plus_abs_b(a, b):
    """Return a+abs(b), but without calling abs.

    >>> a_plus_abs_b(2, 3)
    5
    >>> a_plus_abs_b(2, -3)
    5
    >>> # a check that you didn't change the return statement!
    >>> import inspect, re
    >>> re.findall(r'^\s*(return .*)', inspect.getsource(a_plus_abs_b), re.M)
    ['return f(a, b)']
    """
    if b < 0:
        ___ # fill in the blanks
    else:
        ___ # fill in the blanks
    return f(a, b)
```

To test your code, run this on your terminal:

```bash
python3 -i <filename>.py
```

Then type this in on the Python shell:

```python
import doctest
doctest.run_docstring_examples(a_plus_abs_b, globals())
```

## Q2: Hailstone

Douglas Hofstadter's Pulitzer-prize-winning book, *Gödel, Escher, Bach*, poses the following mathematical puzzle.

1. Pick a positive integer `n` as the start.
2. If `n` is even, divide it by 2.
3. If `n` is odd, multiply it by 3 and add 1.
4. Continue this process until `n` is 1.

The number `n` will travel up and down but eventually end at 1 (at least for all numbers that have ever been tried -- nobody has ever proved that the sequence will terminate). Analogously, a hailstone travels up and down in the atmosphere before eventually landing on earth.

This sequence of values of `n` is often called a Hailstone sequence. Write a function that takes a single argument with formal parameter name `n`, prints out the hailstone sequence starting at `n`, and returns the number of steps in the sequence:

```python
def hailstone(n):
    """Print the hailstone sequence starting at n and return its
    length.

    >>> a = hailstone(10)
    10
    5
    16
    8
    4
    2
    1
    >>> a
    7
    """
    pass
```

Hailstone sequences can get quite long! Try 27. What's the longest you can find?

To test your code, run this on your terminal:

```bash
python3 -i <filename>.py
```

Then type this in on the Python shell:

```python
import doctest
doctest.run_docstring_examples(hailstone, globals())
```

## Q3: Num eights

Write a recursive function `num_eights` that takes a positive integer `x` and returns the number of times the digit 8 appears in `x`. *Use recursion - the tests will fail if you use any assignment statements.*

```python
def num_eights(x):
    """Returns the number of times 8 appears as a digit of x.

    >>> num_eights(3)
    0
    >>> num_eights(8)
    1
    >>> num_eights(88888888)
    8
    >>> num_eights(2638)
    1
    >>> num_eights(86380)
    2
    >>> num_eights(12345)
    0
    >>> from construct_check import check
    >>> # ban all assignment statements
    >>> check(HW_SOURCE_FILE, 'num_eights',
    ...       ['Assign', 'AugAssign'])
    True
    """
    pass
```

To test your code, run this on your terminal:

```bash
python3 -i <filename>.py
```

Then type this in on the Python shell:

```python
import doctest
doctest.run_docstring_examples(num_eights, globals())
```