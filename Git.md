# Git - Knowledge Sharing

## Table of contents

[I. What is Git?](#what-is-git)

[II. Getting Started](#getting-started)
- [1. How to Install Git](#how-to-install-git)
- [2. Git Environment Setup](#git-environment-setup)
- [3. Git Tools](#git-tools)
- [4. Git Flow](#git-flow)

[III. Git Commands](#git-commands)
- [1. Git init](#git-init)
- [2. Git Clone](#git-clone)
- [3. Git Branch](#git-branch)
- [4. Git Checkout](#git-checkout)
- [5. Git Add](#git-add)
- [6. Git Commit](#git-commit)
- [7. Git Push](#git-push)
- [8. Git Pull](#git-pull)
- [9. Git Diff](#git-diff)
- [10. Git Stash](#git-stash)
- [11. Git Status](#git-status)
- [12. Git Log](#git-log)
- [13. Git Status](#git-status)
- [14. Git Log](#git-log)
- [15. Git Merge](#git-merge)
- [16. Git Rebase](#git-rebase)
- [17. Git Reset](#git-reset)
- [18. Git Revert](#git-revert)

<a name="what-is-git"></a> 
### What is Git?

Git is software for tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development.

![GIT](https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png)

Git was created by Linus Torvalds in 2005 for the development of the Linux kernel, with other kernel developers contributing to its initial development. Since 2005, Junio Hamano has been the core maintainer. Git is free and open-source software distributed under GNU General Public License Version 2.

<a name="getting-started"></a> 
### Getting Started

<a name="how-to-install-git"></a> 
#### How to Install Git

Install Git on Windows

```
https://git-scm.com/downloads
```

Install Git on Ubuntu

```
apt-get update
apt-get install git-core
```

Install Git on Mac

```
https://git-scm.com/downloads
```

Confirm Git the installation

```
git --version
```

<a name="git-environment-setup"></a> 
#### Git Environment Setup

Git supports a command called git config that lets you get and set configuration variables that control all facets of how Git looks and operates. It is used to set Git configuration values on a global or local project level.

Setting user.name and user.email are the necessary configuration options as your name and email will show up in your commit messages.

```
git config --global user.name "Tech Finally"
git config --global user.email "dev@techfinally.com"
```

You can check your configuration settings; you can use the git config --list command to list all the settings that Git can find at that point.

```
git config -list
```

<a name="git-tools"></a> 
#### Git Tools

To explore the robust functionality of Git, we need some tools. Git comes with some of its tools like Git Bash, Git GUI to provide the interface between machine and user. It supports inbuilt as well as third-party tools.

Git comes with built-in GUI tools like git bash, git-gui, and gitk for committing and browsing. It also supports several third-party tools for users looking for platform-specific experience.

- GitBash
- Git GUI
- Gitk
- SourceTree
- GitHub Desktop
- TortoiseGit
- SmartGit

<a name="git-flow"></a> 
#### Git Flow

Git flow is the set of guidelines that developers can follow when using Git. We cannot say these guidelines as rules. These are not the rules; it is a standard for an ideal project. So that a developer would easily understand the things.

It is referred to as Branching Model by the developers and works as a central repository for a project. Developers work and push their work to different branches of the main repository.

There are different types of branches in a project. According to the standard branching strategy and release management, there can be following types of branches:

- Master
- Develop
- Hotfixes
- Release branches
- Feature branches

Two of the branching model's branches are considered as main branches of the project (master, develop).

The master branch is the main branch of the project that contains all the history of final changes. Every developer must be used to the master branch. The master branch contains the source code of HEAD that always reflects a final version of the project.

It is parallel to the master branch. It is also considered the main branch of the project.  This branch contains the latest delivered development changes for the next release. 

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

<a name="git-commit"></a> 
#### Git Commit

Every time you commit your code changes, you’ll also include a message to briefly describe the changes you made. This helps other team members quickly understand what was added, changed, or removed.

```
git commit -m “<commit-message>”
```

Note: The git commit command saves the changes only in your local repository. It does not push to the remote origin and make your changes accessible for others to collaborate.

<a name="git-push"></a> 
#### Git Push

To make all your committed changes available to your teammates, you’ll have to push them to the remote origin.

```
git push <remote> <branch-name>
```

Note: It’s important to remember that git push command will upload only the changes you’ve committed.

<a name="git-pull"></a> 
#### Git Pull

The git pull command allows you to fetch all the changes that your teammates pushed and automatically merge them into your local repo.

```
git pull <remote>
```

<a name="git-diff"></a> 
#### Git Diff

Git Diff is my go-to command when I want to quickly see the difference between my current branch and another branch (usually the branch I’m merging into).

```
git diff
```

To compare a file from two branches

```
git diff branch1 branch2 ./filename.txt
```

<a name="git-stash"></a> 
#### Git Stash

Git Stash temporarily shelves your work, so you can switch to another branch, work on something else, and then come back to this at a later time.

It’s perfect if you need to work on something else and you’re midway through a code change, but aren’t ready to commit the code.

```
git stash save “<stash-message>”
```

This will stash your changes with the message you entered. This can be helpful when you want to come back and restore your stash, especially when you have several stashes.

However, this will only stash your tracked files that you added using git add. If you want to include the untracked files as well, run

```
git stash save -u
```

When you want to view all the stashed code, you can view them using this command. Once you stash your code, git will assign a stash id, so you can restore a specific stashed code later.

```
git stash list
```

This will automatically restore and apply the topmost stash in the stack.

```
git stash apply
```

To automatically also delete the stash from the stack, the git stash pop command is used. If you want to do it for a specific stash in the stack:

```
git stash pop
```

<a name="git-status"></a> 
#### Git Status

When you’re feeling a bit lost with what’s happened in your repo (yes, it can happen) the Git Status command can tell you all the information you’ll need to know.

```
git status
```

<a name="git-log"></a> 
#### Git Log

While git status gave you nearly all the information you’d have needed, it wouldn’t give you the information about the commit history for the repository. This is where the git log command comes into the picture.

```
git log
```

<a name="git-merge"></a> 
#### Git Merge

Once you’re done with development inside your feature branch and tested your code, you can merge your branch with the parent branch. This could be either a develop branch or a master branch depending on the git workflow you follow.

When running a git merge command, you first need to be on the specific branch that you want to merge with your feature branch.

```
git checkout develop
```

Before merging, you must make sure that you update your local develop branch. This is important because your teammates might’ve merged into the develop branch while you were working on your feature. We do this by running the pull command.

```
git pull
```

If there are no conflicts while pulling the updates, you can finally merge your feature branch into the develop branch.

```
git merge feature
```














