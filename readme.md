This is where I write what I have learned about Git.

Introduction to Git
===================

Git is a distributed version control, created by Linus Travalds.

So many names: Git, Git on Windows, Git on Mac OSX, Git on Linux, GitHub, Bitbucket, etc. What are they?

Git - A verson control system, created by Linus Torvalds
GitHub - A web-based Git repository hosting service
Bitbucket - A web-based hosting service for projects that use either the Mercurial or Git

Then, there are bunch of Git clients. 

Basic Git
=========

Configuring Git
---------------

There are three levels of configuration: system, user and project
```
// system level
// file location (-nix): /etc/gitconfig
// file location (Windows): <git_installed>/etc/gitconfig
$ git config --system

// user level
// file location (-nix): ~/.gitconfig
// file location (Windows): Users/<name>/.gitconfig
$ git config --global

// repository level 
// file location (-nix): <repo>/.git/config
// file location (Windows): <repo>/.git/config
$ git config
```

####Common config
user.name=wnattawan
user.email=wnattawan@abc.com
help.autocorrect=1
color.ui=auto
remote.origin.url=https://github.com/wnattawan/git-tutorial.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
branch.master.remote=origin
branch.master.merge=refs/heads/master

Working with Git locally
------------------------
```
// Initialize Git
$ git init

// Create a readme.txt
$ touch readme.txt

// Stage readme.txt
$ git add readme.txt

// Modify readme.txt
// Update a staged readme.txt
$ git add -u readme.txt

// Commit readme.txt to local repo
$ git commit -m "Initial commit"

// Show file status in a working copy
$ git status

// Show commit logs
$ git log [--oneline] [--graph]
$ git shortlog

// Unstage files
$ git reset readme.txt	

// Restore working copy files
$ git checkout -- readme.txt

// Show changes between commits
$ git diff HEAD~1..HEAD
$ git diff nnnnnn..mmmmmm
$ git diff --staged
```

Advanced Git
============
N/A
