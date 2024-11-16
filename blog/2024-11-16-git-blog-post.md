---
slug: Git
title: Git
authors: Mouad
tags: [Git]
---

# Git Commands Summary

Git is an essential tool for version control, allowing you to manage your project’s codebase efficiently. Below are some basic and essential Git commands to help you get started.

## 1. Initialize a Git Repository

- **If the project was cloned from a platform like GitHub:**
  - Use the command `git clone <repository-url>` to clone the repository.

- **For a local project:**
  - Run `git init` to initialize a new Git repository in your project folder.
  - Run:
    
    git remote add origin https://github.com/MouadBourquouquou/test-repo.git
    git branch -M main
    git push -u origin main
    

## 2. Configure Git User Details

- **To view your current configuration:**
  git config --list
To set your user name:



git config --global user.name "Your Name"
To set your user email:



git config --global user.email "youremail@example.com"
To remove the current user name configuration:



git config --global --unset-all user.name
3. View Repository Status
Use git status to see the status of your working directory and staged files.
4. View Changes Between Local and Last Commit
Use git diff to see the differences between your working directory and the last commit.
5. Stage Changes for Commit
To stage a specific file:



git add filename
To stage all files:



git add .  # or git add -A
6. Create a Commit
Use git commit -m "your commit message" to commit staged changes with a message.
7. Rename the Current Branch
Use git branch -M branchName to rename the current branch (e.g., from master to main).
8. Push Changes to the Remote Repository
Use git push -u origin main to push your local changes to the remote repository on the main branch.
9. Pull Changes from the Remote Repository
Use git pull origin main to fetch and merge changes from the main branch of the remote repository into your local repository.
10. Handling Line Endings Warning
If you get a warning like:
lua

warning: in the working copy of 'blog/authors.yml', LF will be replaced by CRLF the next time Git touches it,
you can configure Git to automatically handle line endings with the following command:


git config --global core.autocrlf true
Objectif des Branches dans Git
Les branches permettent de travailler sur différentes fonctionnalités ou parties d’un projet de manière indépendante, tout en préservant la branche principale (généralement main ou master). Chaque collaborateur peut créer sa propre branche, y apporter des modifications, puis fusionner (merger) sa branche avec la branche principale après validation.

Commandes Liées aux Branches
Créer une nouvelle branche :



git branch <nom_de_branche>
Lister les branches locales :



git branch
Changer de branche :



git switch <nom_de_branche>
Créer une nouvelle branche et y basculer directement :



git switch -c <nom_de_branche>
Key Notes:
git add stages changes, and git commit saves those changes in your local repository.
git push uploads your local changes to the remote repository, and git pull downloads changes from the remote repository to your local machine.
git status helps you track changes and see which files are staged, modified, or untracked.
csharp

