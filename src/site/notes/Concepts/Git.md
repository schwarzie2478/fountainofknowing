---
{"dg-publish":true,"permalink":"/concepts/git/","tags":["concept/SRE"]}
---

Type of [[Concepts/Source Control\|Source Control]]

Versioning in Git:  [[Concepts/GitVersion\|GitVersion]]
## Usage
### Typical commands:
```shell
git init
git clone repo-url
git checkout -b feature/myfeature
git checkout master
git merge feature/myfeature
git add .
git commit -m"message"
git push -u origin HEAD
git pull
```

### git aliases
```shell
[alias]
	co = checkout
	com = checkout master
	cof = "!git checkout -B feature/$1 && echo Created feature branch "
	cob = "!git checkout -B bugfix/$1 && echo Created bugfix branch "c
	pushh = push origin head
	list = branch -l
	undo = reset --soft HEAD~1
	diff-words = diff --color-words='[^[:space:]]|([[:alnum:]]|UTF_8_GUARD)+'
	lol = log --graph --decorate --pretty=oneline --abbrev-commit
    lola = log --graph --decorate --pretty=oneline --abbrev-commit --all
```
