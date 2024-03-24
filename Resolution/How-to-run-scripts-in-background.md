## Resolution: How-to-run-scripts-in-background

### nohup

```python
nohup ./myprogram > foo.out 2> foo.err < /dev/null &
```

redirect `standard error` to `standard output`:

```python
nohup ./myprogram > foo.out 2>&1 < /dev/null &
```

Use specific GPUs:

```python
CUDA_VISIBLE_DEVICES=0,1,2,3 nohup ./myprogram > foo.out 2> foo.err < /dev/null &
```



### tmux



## Reference

[Application of nohup](https://www.jianshu.com/p/31e2f61f605e)

[Redirection in Computing](https://www.jianshu.com/p/d39130d8e08d)
