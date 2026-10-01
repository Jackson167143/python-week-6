# PLP Python Week 6 - Safe Functions

## Assignment Title

**PLP Python Week 6 - Safe Functions and Error Handling**

## Files in This Repository

* **`safe_tools.py`** - Contains three safe functions: `safe_divide()`, `safe_number()`, and `get_field()`. The functions use `try` and `except` to prevent the program from crashing when errors occur.
* **`unbreakable.py`** - Contains the unbreakable Python program required for the Week 6 assignment.
* **`README.md`** - Explains the assignment and describes the files in the repository.

## What I Learned

The `try` and `except` statements allow a Python program to handle errors safely instead of crashing.

An `if` check cannot catch `abc` on its own because `int("abc")` raises a `ValueError`. The `try` and `except` block catches the error and returns `"Not a number"`.

## Expected Output

```text
5.0
Cannot divide by zero
42
Not a number
82
Field not found
```

## Repository

This project was created for the **PLP Python Week 6** assignment.
