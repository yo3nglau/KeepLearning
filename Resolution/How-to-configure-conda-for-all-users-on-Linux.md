## Resolution: How to configure conda for all users on Linux

Primarily, we define the directory where Anaconda is installed as `/ANACONDA/INSTALLATION/DIRECTORY`.

Add the path in `/etc/environment` and `/etc/profile` (or `/etc/profile.d/conda.sh`) so that every user on Linux can find `conda`:

```python
export PATH="/ANACONDA/INSTALLATION/DIRECTORY/bin:$PATH"
```

Create a group called `conda` (or other names that you prefer):

```python
groupadd conda
```

Change the group ownership of the installation directory of Anaconda to the created group `conda`:

```python
chgrp -R conda /ANACONDA/INSTALLATION/DIRECTORY
```

Inherit group permissions for subsequently created files in `/ANACONDA/INSTALLATION/DIRECTORY`:

```python
find /ANACONDA/INSTALLATION/DIRECTORY -type d -exec chmod g+s {} +
```

Grant permissions for the directory/file protection:

```python
chmod -R g=rX,o-rwx /ANACONDA/INSTALLATION/DIRECTORY
```

Allow users to download new packages:

```python
chmod -R g+w /ANACONDA/INSTALLATION/DIRECTORY/pkgs
```

(Consider before execution; see **Note** first) Avoid users to write in the shared directory:

```python
touch /ANACONDA/INSTALLATION/DIRECTORY/envs/.conda_envs_dir_test
chomod 600 /ANACONDA/INSTALLATION/DIRECTORYenvs/.conda_envs_dir_test
```

**Note:** If you intend to allow users to create virtual environments in the shared directory, you will not configure `.conda_envs_dir_test` and additionally execute commands instead:

```python
chmod -R g+w /ANACONDA/INSTALLATION/DIRECTORY
```

At the same time, you are also supposed to consider `cache` directories no matter which conditions:

```python
chgrp -R conda /MAIN/.cache
```

This setting will allow users to add or use cache files for `pip`, `torch`, etc.

Finally, configure the `.condarc` file exactly under the `/ANACONDA/INSTALLATION/DIRECTORY` (if it does not exist, `touch` one) with two alternatives:

- Allow users to create virtual environments in the shared directory

```python
envs_dirs:
  - /ANACONDA/INSTALLATION/DIRECTORY/envs
```

- Allow users to create virtual environments in their user directories

```python
envs_dirs:
  - ~/.conda/envs
```

