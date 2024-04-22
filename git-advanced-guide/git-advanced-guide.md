# Git advanced techniques

This document references from Youtube: [13 Advanced (but useful) Git Techniques and Shortcuts](https://www.youtube.com/watch?v=ecK3EnyGD8o)


## 1. Combine add and commit
```bash
git commit -am "message"
```

This commit only works with modified files, not untracked files.

## 2. Command alias
```bash
git config --global alias.alias_name "command"
Ex:
git config --global alias.ac "commit -am"
git ac "message"
```

--global flag sets config on user account, without it doing on repository

## 3. Change the last commit message
Change the last commit message:
```bash
git commit --amend -m "message"
```
Commit with no message:
```bash
git commit --amend --no-edit
```

## 4. Revert
```bash
git revert <hash_id>
```
To get hash_id of a commit, using extensions (like Git Graph) or list all head in branch:
```bash
git log --oneline
```
--oneline flag helps more visual

## 5. Github Web editor

Press "." on the repository to open web editor, but we cannot run terminal.
Can use terminal by Github Codespace.

## 6. Git stash

The git stash command in Git is used to temporarily store changes that you have not committed yet, allowing you to work on something else without committing your changes.
```bash
git stash
git stash <name>
git stash apply <hash_id/number/name>
git stash list
git stash drop <hash_id/number/name>
git stash pop
```