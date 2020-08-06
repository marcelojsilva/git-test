# Git Quick Guide
Command list for quick reference

*Leia isto em [Português](README.pt-br.md)*

## Table of contents
- [Initial Configuration](#initial-configuration)
- [Configuration List](#configuration-list)
- [Init a local repository](#init-a-local-repository)
- [Add changes](#add-changes)
- [Commit local changes](#commit-local-changes)
- [New remote repository](#new-remote-repository)
- [Add remote repository](#add-remote-repository)
- [Push to remote repository](#push-to-remote-repository)
- [Add and change to new branch](#add-and-change-to-new-branch)
- [Back to master](#back-to-master)
- [Create a second branch, do changes and merge to master](#Create-a-second-branch,-do-changes-and-merge-to-master)
- [View branchs](#view-branchs)
- [Repository status](#repository-status)
- [Commit history with statistics](#Commit-history-with-statistics)
- [List remote repositories](#list-remote-repositories)
- [Merge remote and local repositories](#merge-remote-and-local-repositories)

## Github

<!-- toc -->

### Initial Configuration
*(Only first time)*
```bash
git config --global user.name "UserName"
git config --global user.email "your_email@mail.com"
```

### Configuration List
```bash
git config --list
```

### Init a local repository
```bash
git init
```

### Add changes
```bash
git add *
```

### Commit local changes
```bash
git commit -m "Initial commit"
```

### New remote repository
curl -u '[your-git-userId]' https://api.github.com/user/repos -d '{"name":"[repository-name]"}'

### Add remote repository
```bash
git remote add origin https://github.com/[user-git]/[repository-name]
```

### Push to the remote repository
```bash
git push -u origin master
```

### Add and change to the new branch
```bash
git checkout -b development
```

### Back to master
```bash
git checkout master
```

### Create a second branch, do changes and merge to master
```bash
git checkout -b hotfix
#do changes
git checkout master
git merge hotfix
git branch -d hotfix
```
### View branchs
```bash
git branch -v
```

### Repository status
```bash
git status
```

### Commit history with statistics
```bash
git log --stat -2
```

### List remote repositories
```bash
git remote -v
```

### Merge remote and local repositories

*To resolve "fatal: refusing to merge unrelated histories"*

```bash
git pull origin master --allow-unrelated-histories -m "Merge text" 
```
