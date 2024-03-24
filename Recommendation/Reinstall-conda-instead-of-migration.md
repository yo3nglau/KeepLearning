## Recommendation:  Reinstall conda instead of migration

It is hard to migrate conda from one location to another painlessly. Practically, if you insist on migration, the problems of execution paths hinder you most. You have to modify variables almost everywhere to deal with the issue of `bad interpreter: No such file or directory`, like:

```python
vim ~/miniconda3/bin/pip
vim ~/miniconda3/bin/pip3
vim ~/miniconda3/bin/conda
...
```

To make matters worse, if you have multiple virtual environments, they **all** have to be manually modified, as above!

At the same time, you will probably encounter the issue in terms of `clear` command:

```python
terminals database is inaccessible
```

Though practitioners seemingly [resolve](https://askubuntu.com/questions/988694/clear-command-terminals-database-is-inaccessible) this [issue](https://github.com/ContinuumIO/anaconda-issues/issues/331):

```python
# alternative 1
export TERMINFO=/usr/share/terminfo
# alternative 2
sudo mv $CONDA_PREFIX/bin/clear $CONDA_PREFIX/bin/clear_old
```

Related issues still tend to exist when you switch between system and conda environments.

Overall, it is not recommended to migrate the conda location even if you have a wealth of time. The appropriate way to achieve your attempt is **reinstallation**.

### Reinstallation

Before that, a correct uninstallation is highly recommended:

```python
conda install anaconda-clean
anaconda-clean --yes
```

However, if your conda has broken down, in which case you intend to migrate it before:

```python
Error: Unable to move .anaconda
```

`anaconda-clean` probably does not work as usual. In this unfortunate situation, you must manually delete all conda-related directories and files recursively and any latent configurations about conda.

Installing conda is as simple as:

```python
wget -c https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

Remember to choose the compatible version from the [official website](https://docs.anaconda.com/free/miniconda/). 

Then grant permissions and execute:

```python
chmod 777 Miniconda3-latest-Linux-x86_64.sh
sh Miniconda3-latest-Linux-x86_64.sh
```

Specify the ideal location when installing:

```python
Miniconda3 will now be installed into this location:
    ...
    - Or specify a different location below
```

After installation, you might need to configure it for global use on Linux and set mirrors on mainland China.

