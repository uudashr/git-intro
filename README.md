# Short intro to Git

## Git setup (first time only)

First time only

```shell
# set global config
git config --global user.name "Nuruddin Ashr"
git config --global user.email "uudashr@gmail.com"

# list global config
git config -l --global
```



or for specific project

```shell
# set local config
git config --local user.name "Nuruddin Ashr"
git config --local user.email "nuruddin@kurio.co.id"

# list local config
git config -l --local
```

## Create repository

### Github first

```shell
# TODO go to github.com and create repository
git clone https://github.com/uudashr/git-intro.git
cd git-intro
```



### Local first

```shell
# TODO create README.md with some content

git init
git add README.md
git commit -m "Added README.md"
git remote add origin https://github.com/uudashr/git-intro.git
git push -u origin master
```



## Ignoring files (.gitignore)

If we want something to ignore by the git

**file:** *.gitignore*

```
.DS_store
temp
TODO.txt
```

## Make some changes

```shell
# TODO make some change to README.md
git status
git add README.md

# check again the status
git status
git commit -m "Made some changes to the README.md"
git push
```

or add new file

```shell
# TODO create new file story.txt

git status
git add story.txt

# check again the status
git status
git commit -m "Add our first story"
git push
```



## Branching

### Listing branch

```shell
git branch
```



### Create branch

```shell
git branch <branch-name>
```



or create branch and checkout (switch)

```shell
git checkout -b <branch-name>
```



### Switching between branch

```shell
git checkout <branch-name>
```



### Merging branch

```shell
git checkout master
git merge <branch-name>
```



### Deleting (local) branch

```shell
git branch -d <branch-name>
```



### Pushing (local) branch to remote repo

```shell
git push -u origin <branch-name>
```



### Deleting remote branch

```shell
git push origin --delete <branch-name>
```

or

```shell
git branch -dr origin/<branch-name>
```



## Tagging

```shell
git tag <tag-name>
```



push to remote

```shell
git push origin <tag-name>
```

or

```shell
git push --tags
```
