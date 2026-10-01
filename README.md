# PLP Python Week 6 - Safe Functions

## Step-by-Step Solution Guide

### Step 1 - `safe_divide()`

Create `safe_tools.py` and start with `safe_divide()`. The risky line goes inside the `try`, and the rescue message goes inside the `except`.

```python
def safe_divide(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "Cannot divide by zero"
```

Test it with:

```python
print(safe_divide(10, 2))
print(safe_divide(10, 0))
```

Expected output:

```text
5.0
Cannot divide by zero
```

### Step 2 - `safe_number()`

`safe_number()` uses the same `try` and `except` structure. Converting invalid text such as `"abc"` with `int()` raises a `ValueError`.

```python
def safe_number(text):
    try:
        return int(text)
    except ValueError:
        return "Not a number"
```

### Step 3 - `get_field()`

`get_field()` safely looks up a value in a dictionary. If the requested key does not exist, Python raises a `KeyError`.

```python
def get_field(learner, key):
    try:
        return learner[key]
    except KeyError:
        return "Field not found"
```

## Complete `safe_tools.py`

```python
def safe_divide(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "Cannot divide by zero"


def safe_number(text):
    try:
        return int(text)
    except ValueError:
        return "Not a number"


def get_field(learner, key):
    try:
        return learner[key]
    except KeyError:
        return "Field not found"


print(safe_divide(10, 2))
print(safe_divide(10, 0))
print(safe_number("42"))
print(safe_number("abc"))

learner = {"name": "Amina", "score": 82}
print(get_field(learner, "score"))
print(get_field(learner, "email"))
```

## Expected Output

```text
5.0
Cannot divide by zero
42
Not a number
82
Field not found
```

## Why can't an `if` check catch `abc` on its own?

An `if` statement can check conditions, but `int("abc")` raises a `ValueError` while Python is trying to perform the conversion. The `try` and `except` block catches this error and prevents the program from crashing.

## Files

* `safe_tools.py` - Contains the three safe functions and their tests.
* `unbreakable.py` - Contains the required unbreakable Python program.
* `README.md` - Contains the assignment information and solution explanation.

## GitHub Repository

Repository name:

`plp-python-week6`
