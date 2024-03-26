## Resolution: How to set cache location of the pip and torch

We commonly set the cache location of pip and torch because they occupy a bulk of storage in the system directory (especially when you use cloud resources).

The simple and effective way is configuring the `.bashrc` file of users (probably more efficient if set in `/etc/profile`):

```python
export PIP_CACHE_DIR=/IDEAL/LOCATION/.cache/pip
export TORCH_HOME=/IDEAL/LOCATION/.cache/torch
```

