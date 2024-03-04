## Resolution: How to alter dict key in Python

### Pop and update

```python
dict={'a': 1, 'b': 2}
 
dict['c'] = dict.pop('a')
```

**Note:** The key in dict is forbidden to alter directly because of the hash mechanism.

