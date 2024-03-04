## Resolution: How to count files or directories on Linux

### Application 1

Count the files under the current directory.

```python
# Not recursively
ls -l | grep "^-" | wc -l
# Recursively
ls -lR | grep "^-" | wc -l
```

### Application 2

Count the subdirectories under the current directory.

```python
# Not recursively
ls -l | grep "^d" | wc -l
# Recursively
ls -lR | grep "^d" | wc -l
```

<br>

## Specification

