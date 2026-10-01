# PLP Python Week 6 - Safe Functions

This repository contains my Week 6 Python assignment on safe functions and error handling.

## Files

* `safe_tools.py` - Contains three safe functions: `safe_divide`, `safe_number`, and `get_field`, with error handling using `try` and `except`.
* `unbreakable.py` - Contains the Week 6 unbreakable Python program.
* `README.md` - Provides information about the assignment and the files in the repository.

## Why can't the `if` check catch `abc` on its own?

An `if` check cannot catch `abc` when converting text with `int()` because `int("abc")` causes a `ValueError`. The `try` and `except` block catches this error and safely returns `"Not a number"` instead of allowing the program to crash.
