# Comp Thinking Quiz 1

## Q1: Num eights
Write a function num_eights that takes a positive integer x and returns the number of times the digit 8 appears in x.

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

## Q2: Ping-pong

The ping-pong sequence counts up starting from 1 and is always either counting up or counting down. At element `k`, the direction switches if `k` is a multiple of 8 or contains the digit 8. The first 30 elements of the ping-pong sequence are listed below, with direction swaps marked using brackets at the 8th, 16th, 18th, 24th, and 28th elements:

|Index|1|2|3|4|5|6|7|[8]|9|10|11|12|13|14|15|[16]|17|[18]|19|20|21|22|23|
|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|
|PingPong Value|1|2|3|4|5|6|7|[8]|7|6|5|4|3|2|1|[0]|1|[2]|1|0|-1|-2|-3|

|Index (cont.)|[24]|25|26|27|[28]|29|30|
|:---|:---|:---|:---|:---|:---|:---|:---|
|PingPong Value|[-4]|-3|-2|-1|[0]|-1|-2|

Implement a function `pingpong` that returns the nth element of the ping-pong sequence without using any assignment statements.

You may use the function `num_eights`, which you defined in the previous question.

```python
def pingpong(n):
    """Return the nth element of the ping-pong sequence.

    >>> pingpong(8)
    8
    >>> pingpong(10)
    6
    >>> pingpong(15)
    1
    >>> pingpong(21)
    -1
    >>> pingpong(22)
    -2
    >>> pingpong(30)
    -2
    >>> pingpong(68)
    0
    >>> pingpong(69)
    -1
    >>> pingpong(80)
    0
    >>> pingpong(81)
    1
    >>> pingpong(82)
    0
    >>> pingpong(100)
    -6
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
doctest.run_docstring_examples(pingpong, globals())
```

## Q3: Missing Digits

Write the recursive function `missing_digits` that takes a number `n` that is sorted in increasing order (for example, `12289` is valid but `15362` and `98764` are not). It returns the number of missing digits in `n`. A missing digit is a number between the first and last digit of `n` of a that is not in `n`. *Use recursion - the tests will fail if you use while or for loops.*

```python
def missing_digits(n):
    """Given a number a that is in sorted, increasing order,
    return the number of missing digits in n. A missing digit is
    a number between the first and last digit of a that is not in n.
    >>> missing_digits(1248) # 3, 5, 6, 7
    4
    >>> missing_digits(1122) # No missing numbers
    0
    >>> missing_digits(123456) # No missing numbers
    0
    >>> missing_digits(3558) # 4, 6, 7
    3
    >>> missing_digits(35578) # 4, 6
    2
    >>> missing_digits(12456) # 3
    1
    >>> missing_digits(16789) # 2, 3, 4, 5
    4
    >>> missing_digits(19) # 2, 3, 4, 5, 6, 7, 8
    7
    >>> missing_digits(4) # No missing numbers between 4 and 4
    0
    >>> from construct_check import check
    >>> # ban while or for loops
    >>> check(HW_SOURCE_FILE, 'missing_digits', ['While', 'For'])
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
doctest.run_docstring_examples(missing_digits, globals())
```