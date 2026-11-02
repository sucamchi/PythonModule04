*This project has been created as part of the 42 curriculum by scamlett.*

# Python Module 04: Cyber Archives

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![42](https://img.shields.io/badge/42-Málaga-000000)

## Description

A module about working with files. The theme is recovering and preserving
old archives: open a file, read it, write a transformed copy, report errors
to the right stream, and finally do it all safely with context managers.

| Exercise | File | Topic |
|----------|------|-------|
| ex0 | `ft_ancient.text.py` | Opening and reading a file, closing it by hand, handling a missing file |
| ex1 | `ft_archive_creation.py` | Reading one file and writing a new, transformed copy |
| ex2 | `ft_stream_management.py` | Sending errors to `stderr` instead of `stdout` |
| ex3 | `ft_vault_security.py` | `with open(...)` so files close automatically |

## Instructions

Exercises 0 to 2 take the file to read as their only argument:

```bash
echo "hello archive" > sample.txt
python3 ex1/ft_archive_creation.py sample.txt
python3 ex2/ft_stream_management.py missing.txt 2> errors.log
python3 ex3/ft_vault_security.py
```

## What I learned

- Opening files in read (`"r"`) and write (`"w"`) mode, and why every opened
  file must be closed
- Catching `OSError` / `FileNotFoundError` so a bad path doesn't crash the
  program
- The difference between `stdout` and `stderr`, and printing to `stderr`
  with `print(..., file=sys.stderr)` so errors can be redirected separately
- Context managers: `with open(...) as f:` closes the file even if an error
  happens inside the block, which replaces the manual `try` / `finally`
