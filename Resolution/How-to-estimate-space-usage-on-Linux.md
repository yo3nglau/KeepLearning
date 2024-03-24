## Resolution: How to estimate space usage on Linux

### Application 1

Estimate the **total** space usage for the current (targeted) directory.

```python
du -sh (optional PATH_OF_TARGETS, ./ by default)
```

If you prefer a sorted list:

```python
du -sh * | sort -rh
```

### Application 2

Estimate space usage of **every directory recursively** in the current directory.

```python
du -h
```

### Application 3

Estimate space usage of **every file recursively** in the current directory.

```python
du -ah
```

<br>

## Reference

[(Linux) du](/Guide/Linux/Linux-du.md)
