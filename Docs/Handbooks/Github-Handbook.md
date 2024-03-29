[⬅️ BACK TO INDEX](../../#my-open-studies)
# Git + Github Handbook #

## List branches: ##
git branch

## List all branches (remotes an locals) ##
git branch -a

## Create branch: ##
git branch -C "name"

## Delete branch: ##
git branch --delete "name"

## Rename current branch ##
git branch -M "new-name"

## Push new branch to Romote ##
git push -u 'remote-name' 'branch-name' 
- the -u is for upstream

## Add a remote ##
git remote add "remote-name" "https://remote.domain/repo.git"

## Create a new branch based on current ##
git checkout -b 'new-branch-name'


## Remove a remote ##
git remote remove "remote-name"
<br><br>
<hr><hr>

# Git Hub New Repo Step guides #

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

O commit é uma caixa de alteracoes com um selo(msg do commit)

Pasta local = working directory (WC)
Staging Area = Caixa de alteracoes aberta (SA)

git add <file-name-or-folder>
• Inclui mudancas feitas na WC a SA, porem mantem a caixa aberta

git rm --cached <file-name-or-folder>
• 'rm' removes
• '--cached' arquivos na caixa aberta
• '<>' seletor de arquivos
• 'git rm --cached .' unstages all changes

tree .git (lista a arvore de diretorios da pasta '.git')

O git guarda apenas objetos que representam as alteracoes e nao os arquivos inteiros

Se um commit novo é feito, ele aponta para os commits anteriores como referencia


git log
• mostra o historico de alteracoes na pasta .git

git checkout -b <nome do branch>
- Cria um novo braco de código que aponta para o último commit no braço anterior.

gitk --all  (commando)
GUI para inspecionar a pasta .git

git usa a estrutura de um grafo

cat .git/HEAD (comando)
mostra o branch em trabalho(?)

git log --decorate --oneline --graph --all


## How to merge dev branch on main branch

```
$ git checkout dev
# ...develop some code...

$ git add .
$ git commit –m "Some commit message"
$ git checkout main
Switched to branch 'main'
$ git merge dev
```
Quick answer: On main branch run ⬇️
```
git merge dev
```

## How to undo changes made in local environment
1) Clean the working tree
```
git reset --hard
git pull
```
2) If there are untracked local files you could use `git clean` to remove them.

- `git clean -f` to remove untracked files
- `git clean -df` to remove untracked files and directories
- `git clean -xdf` to remove untracked or ignored files or directories



## How to Delete a Git Branch Both Locally and Remotely
Delete branch locally
```bash
git branch -d localBranchName
```

Remove branch from remote
```bash
git push origin --delete remoteBranchName
```



[⬅️ BACK TO INDEX](../../#my-open-studies)

