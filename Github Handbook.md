# Git + Github Handbook #

## List branches: ##
git branch

## List all branches (remotes an locals) ##
git branch -a

## Create branch: ##
git branch -C "name"

## Delete branch: ##
git branch --delete "name"

## Push new branch to Romote ##
git push -u 'remote-name' 'branch-name' 
- the -u is for upstream

## Add a remote ##
git remote add "remote-name" "https://remote.domain/repo.git"

## Remove a remote ##
git remote remove "remote-name"

## Git Hub Step guides ##

`after creating a new Github Repo ->`

### Creating a new local repo via CLI and connecting it to Github ###

```
$    echo "# Project Name" >> README.md
$    git init
$    git add README.md
$    git commit -m "first commit"
$    git branch -M main
$    git remote add origin https://github.com/username/repo-name.git
$    git push -u origin main
```

### Taking a existing local repo via CLI and connecting it to Github ###

```
$    git remote add origin https://github.com/username/repo-name.git
$    git branch -M main
$    git push -u origin main
```



