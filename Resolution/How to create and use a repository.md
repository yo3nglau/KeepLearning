## Resolution

### Crate a new repository

#### Step 1

Click the `Repositories` button on the main page (typically like https://github.com/yo3nglau).

Click the `New` button to create a new repository.

#### Step 2

Input `Repository name` and `Description` (optional).

Choose whether publicly available or not.

Initialize the repository with a `README` file (recommended).

Choose a license for the repository (recommended).

Click the `Create repository` button to complete.

### Update contents for the created repository

#### Step 1

Click the `<> Code` button on the repository page (typically like https://github.com/yo3nglau/KeepLearning).

Copy the web URL, open `Git Bash` at the local position of `Git` repositories (typically like `D:/Git/Repository/`), and clone the repository with:

```python
# Change the web URL of yours
git clone https://github.com/yo3nglau/KeepLearning.git
```

#### Step 2

Edit contents locally (typically like `cd KeepLearning`).

Upload updated contents online with [git init](https://git-scm.com/docs/git-init), [git add](https://git-scm.com/docs/git-add), [git commit](https://git-scm.com/docs/git-commit), and [git push](https://git-scm.com/docs/git-push):

```python
# Create an empty Git repository or reinitialize an existing one (one-off)
git init
# Add file contents to the index
git add -A
# Record changes to the repository
git commit -m "necessary specification of this update"
# Update remote refs along with associated objects
git push
```

