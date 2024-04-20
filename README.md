
# GitHub Simplified to zom

This repository is made to simplify the understanding of GitHub and Git commands. It is a simple guide to help you get started with GitHub and Git commands.
(like if u where a zom)

## Table of Contents
- [GitHub Simplified to zom](#github-simplified-to-zom)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [GitHub](#github)
  - [ssh-keygen](#ssh-keygen)
  - [Git Commands](#git-commands)
    - [if there is no repository but there are files](#if-there-is-no-repository-but-there-are-files)
    - [if there is no repository and no files](#if-there-is-no-repository-and-no-files)
  - [Git simple life cycle](#git-simple-life-cycle)
  - [Git info commande](#git-info-commande)

## Introduction
GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

- Git is a version control system that lets you manage and keep track of your source code history.
- GitHub is a cloud-based hosting service that lets you manage Git repositories.
- ssh-keygen is a tool for creating new authentication key pairs for SSH.
- Git Commands are used to interact with git remote server.

## GitHub

- create a GitHub account
- create a new repository

## ssh-keygen

- generate a new ssh key
```bash
ssh-keygen -t rsa -b 4096 -C "email@placeholder.com"
```
- add the ssh key to the ssh-agent
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```
- add the ssh key to the GitHub account
there is a tutorial on GitHub to add the ssh key to the account [here](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
- copy the ssh key to the clipboard
```bash
sudo apt-get install xclip
xclip -sel clip < ~/.ssh/id_ed25519.pub
```

## Git Commands

### if there is no repository but there are files

- go to the directory where the files are
- create a new repository on gitHub
- copy the ssh url
- create a new repository
```bash
git init
```
- add the remote repository
```bash
git remote add origin <ssh-url>
```

### if there is no repository and no files

- create a new repository on gitHub
- copy the ssh url
- clone the repository
```bash
git clone <ssh-url>
```
- if you have cloned the repository, it is not necessary to add the remote repository

## Git simple life cycle

- add the files to the staging area
```bash
git add .
```
- commit the files to the local repository
```bash
git commit -m "commit message"
```

- push the files to the remote repository
```bash
git push origin master
```

- pull the files from the remote repository
```bash
git pull origin master
```

## Git info commande

- show the status of the files
```bash
git status
```
- show the commit history
```bash
git log
```
- show remote repository
```bash
git remote -v
```
- show the branch
```bash
git branch
```



[Back to Top](#table-of-contents)
