## Resolution: How to configure conda channels

You can show current conda channels with:

```python
conda config --show channels
```

You can quickly add/remove particular channels with:

```python
conda config --add channels MIRROR_URL
conda config --remove channels MIRROR_URL
```

However, it is neither efficient nor versatile; the recommended resolution is configuring the `.condarc` file, as illustrated below.

### For regular/personal users

Configure the `.condarc` file exactly under the user directory, e.g., `/home/ABC`; if it does not exist, first input with the CLI:

```python
conda config --set show_channel_urls yes
```

Then, modify the content with the expected mirrors (you can refer to the section of `Recommended mirrors` below).

### For root/administer users

Configure the `.condarc` file exactly under the installation directory; if it does not exist, `touch .condarc` manually.

Then, modify the content with the expected mirrors (you can refer to the section of `Recommended mirrors` below). By doing so, you can allow all users on the machine to benefit from this configuration.

## Recommended mirrors

```python
channels:
  - defaults
show_channel_urls: true
default_channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
custom_channels:
  conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch-lts: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  deepmodeling: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/
```



## Reference

[Tsinghua mirrors of Anaconda](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)
