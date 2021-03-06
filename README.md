To access the `hashes` mentioned below you can run `git log` on whatever branch and then copy it

# Reverting Commits

Better for using on the master branch, maintains commit history
```
git revert {commit hash}
```
---

Better for using on other branches, doesn't maintain commit history

The `Soft` param returns the files to the staging area 

The `Hard` param returns to the commit and ignores all the changed files
```
git reset --soft {commit hash}
git reset --hard {commit hash}
```

PS: It may be necessary to use the `--force` param for pushing to master branch when having different commit histories



# Changing Previous added Commit

`Amend` is recommended for separate branches or changes that have not yet been pushed to the remote 

```
git commit --amend 
```
# Cherry Picking Commits

Used for picking specific commits from another branch

```
git cherry-pick {commit hash}
```

# Committing specific hunks of a file - Interactive Staging

```
git add -p 
git add --patch <fileName>
```
Legend

`y` Stage this hunk for the next commit;

`n` Do not stage this hunk for the next commit;

`q` Quit; do not stage this hunk or any of the remaining hunks;

`a` Stage this hunk and all later hunks in the file;

`d` Do not stage this hunk or any of the later hunks in the file;

`g` Select a hunk to go to;

`/` Search for a hunk matching the given regex;

`j` Leave this hunk undecided, see next undecided hunk;

`J` Leave this hunk undecided, see next hunk;

`k` Leave this hunk undecided, see previous undecided hunk;

`K` Leave this hunk undecided, see previous hunk;

`s` Split the current hunk into smaller hunks;

`e` Manually edit the current hunk;

`?` Help



## Credits:

[Git na Vida Real](https://www.udemy.com/course/git-e-github-na-vida-real/)

[Interactive Staging - Legend Section](https://stackoverflow.com/questions/1085162/commit-only-part-of-a-file-in-git)