# Knowledge Sharing

## Table of contents

[I. What is Git?](#what-is-git)

[II. Getting Started](#getting-started)
- [1. How to Install Git](#how-to-install-git)
- [2. Git Environment Setup](#git-environment-setup)
- [3. Git Tools](#git-tools)
- [4. Git flow](#git-flow)

[III. Git Commands](#git-commands)
- [1. Git init](#git-init)
- [2. Git Clone](#git-clone)
- [3. Git Branch](#git-branch)
- [4. Git Checkout](#git-checkout)
- [5. Git Add](#git-add)

![GIT](https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png)

<a name="what-is-git"></a> 
### What is Git?

Git is software for tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development.

Git was created by Linus Torvalds in 2005 for the development of the Linux kernel, with other kernel developers contributing to its initial development. Since 2005, Junio Hamano has been the core maintainer. Git is free and open-source software distributed under GNU General Public License Version 2.

<a name="git-commands"></a> 
### Git Commands

<a name="git-init"></a> 
#### Git Init

```
git init
```

This will transform the current directory into a Git repository.

<a name="git-clone"></a> 
#### Git Clone

```
git clone <https://url-of-the-repository>
```

The git clone command is used to download the source code from a remote repository (like GitHub, Bitbucket, or GitLab). When you clone a repo, the code is automatically downloaded to your local machine.

<a name="git-branch"></a> 
#### Git Branch

Command to view all branches

```
git branch
```

Git command to delete a branch

```
git branch -d <branch-name>
```

<a name="git-checkout"></a> 
#### Git Checkout

```
git checkout -b <branch-name>
```

<a name="git-add"></a> 
#### Git Add

Every time you create a new file, delete it, or make a change, you’ll have to tell Git to track it and add it to the staging area. Otherwise, the files you made changes to wouldn’t be added when you try to push your changes.

```
git add <file-name>
```

This command will add only a single file to your next commit. If you want to add all the files to which changes were made, you can use:

```
git add -A
```







