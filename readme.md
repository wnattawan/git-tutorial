This is where I write what I have learned about Git.

Introduction to Git
===================

Git is a distributed version control, created by Linus Travalds.

So many names: Git, Git on Windows, Git on Mac OSX, Git on Linux, GitHub, Bitbucket, etc. What are they?

Git - A verson control system, created by Linus Torvalds
GitHub - A web-based Git repository hosting service
Bitbucket - A web-based hosting service for projects that use either the Mercurial or Git

Then, there are bunch of Git clients. 

To use Git for collaborate with other developers. You need to know concepts of remote and local repositories. 
A remote repo can be for example hosted on Github or Bitbucket. This is known as "origin". You can also create your own central repository. In this case it is call a bare repository. Unlike normal repositories, a bare repository doesn't have a working copy. 

You use a remote repository to share and synchronize work between developers. 

A developer needs to donwload the latest version from the remote repo and share his/her work by uploading to the remote repo using git pull and push respectively. 

Git pull is equivalent to git fetch + git merge

For a succesful collaboration with Git, you need a syncing model to follow. For example, you should only commit functional code to the remote repository. Pull from the remote repo often to ensure that you develop on the latest code. Develop new feature on a new branch. Agree on how a release is built, how to find code ready for production so on and so forth.

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

Working with Git remotely
-------------------------
```
// Clone a git repository
$ git clone https://github.com/wnattawan/git-tutorial.git

// View a remote repository
$ git remote

// Show remote url 
$ git remote -v

// View commit
$ git show HEAD

// View all branches locally
$ git branch

// View all branches remotely
$ git branch -r
```

Advanced Git
============
N/A
