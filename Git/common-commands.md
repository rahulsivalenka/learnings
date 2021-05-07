# Git Commands Used

## Initialization
One time op to initialize a git repo in the folder. This will create a `.git` folder to keep track of the commits and changes made.

```bash
git init
```

## To save ur work

Add files to staging area i.e., stage the files u wanna commit.

`--all` is used to add all changed files (or changes).

```bash
git add --all
```

Save work by committing the staged files

```bash
git commit -m '<Commit Message>'
```

## Rename master to main

```bash
git branch -m <new-name-of-the-current-branch>
## Ex.
## git branch -m main
```

## Linking a remote repo

> Before this we should create a remote repo in some server such as GitHub

```bash
git remote add <name-of-remote> <remote/repo/url>

# Ex.
# git remote add origin https://github.com/rahulsivalenka/ui-meetup-react-working-patterns.git
```

## Fetch the remote repo refs (commits)

```bash
git fetch --all
```

## Set current local branch to track remote branch

```bash
git branch --set-upstream-to=<name-of-remote>/<branch-to-track>

# Ex.
# git branch --set-upstream-to=origin/main
```

## To check status of the git working tree

```bash
git status
```

## Pull the changes from remote

> Before pulling with rebase we have to make our local repo working tree clean i.e., we should not have any uncommitted changes.
>
> To make the working tree clean, commit all the changes.

```bash
git pull --rebase
```

---
## Alternative to linking a remote repo

First, create remote repo in GitHub.

Then clone the repo

```bash
git clone <remote/repo/url>

# Ex.
# git clone https://github.com/rahulsivalenka/ui-meetup-react-working-patterns.git
#
# This command will create a folder ui-meetup-react-working-patterns and download the content
# of the remote repo into it.
```
---

## Push the local commits
This is just one time in case local branch (ex. `main`) is not tracking remote branch (ex. `main`)

```bash
git push -u <name-of-remote> <remote-branch>

# Ex.
# git push -u origin main
```

We can use this once the tracking is done

```bash
git push
```
