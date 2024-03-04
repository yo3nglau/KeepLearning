## Resolution: How to estimate space usage on Linux

### Application 1

Estimate the **total** space usage for the current (targeted) directory.

#### Resolution 1

```python
du -sh
```

#### Resolution 2

```python
du PATH_OF_TARGETS -h
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

[du command](/Guide/Linux-du.md)
