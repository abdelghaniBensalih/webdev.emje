---
slug: git-Commands-Part-1
title: git Commands Part 1
authors: Mouad
tags: [git, github]
---
![git logo](git-commands-part1.png)

# git Commands Part 1

git is an essential tool for version control, allowing you to manage your project’s codebase efficiently. Below are some basic and essential git commands to help you get started.

<!-- truncate -->

## Initialize a Git Repository

- **If the project was cloned from a platform like GitHub:**
    - Use the command `git clone <repository-url>` to clone the repository.

- **For a local project:**
    - Run `git init` to initialize a new Git repository in your project folder.
    - Run:
        ```sh
        git remote add origin <https://github.com/MouadBourquouquou/test-repo.git>
        git branch -M main
        git push -u origin main
        ```

## Configure Git User Details

- **To view your current configuration:**
    ```sh
    git config --list
    ```

- **To set your user name:**
    ```sh
    git config --global user.name "Your Name"
    ```

- **To set your user email:**
    ```sh
    git config --global user.email "youremail@example.com"
    ```

- **To remove the current user name configuration:**
    ```sh
    git config --global --unset-all user.name
    ```

## View Repository Status

Use `git status` to see the status of your working directory and staged files.

## View Changes Between Local and Last Commit

Use `git diff` to see the differences between your working directory and the last commit.

## Stage Changes for Commit

- **To stage a specific file:**
    ```sh
    git add filename
    ```

- **To stage all files:**
    ```sh
    git add .  # or git add -A
    ```

## Create a Commit

Use `git commit -m "your commit message"` to commit staged changes with a message.

## Rename the Current Branch

Use `git branch -M branchName` to rename the current branch (e.g., from master to main).

## Push Changes to the Remote Repository

Use `git push -u origin main` to push your local changes to the remote repository on the main branch.

## Pull Changes from the Remote Repository

Use `git pull origin main` to fetch and merge changes from the main branch of the remote repository into your local repository.

## Handling Line Endings Warning

If you get a warning like:

```
warning: in the working copy of 'blog/authors.yml', LF will be replaced by CRLF the next time Git touches it,
```

you can configure Git to automatically handle line endings with the following command:

```sh
git config --global core.autocrlf true
```

## Objectif des Branches dans Git

Branches allow you to work on different features or parts of a project independently while preserving the main branch (usually main or master). Each collaborator can create their own branch, make changes, and then merge their branch into the main branch after validation.

## Commandes Liées aux Branches

- **Créer une nouvelle branche :**
    ```sh
    git branch <nom_de_branche>
    ```

- **Lister les branches locales :**
    ```sh
    git branch
    ```

- **Changer de branche :**
    ```sh
    git switch <nom_de_branche>
    ```

- **Créer une nouvelle branche et y basculer directement :**
    ```sh
    git switch -c <nom_de_branche>
    ```
# Difference Between Git Staging Commands

The commands `git add .`, `git add --all`, and `git add *` are used to stage changes in Git, but they have some subtle differences. Let's break down what each one does:

## 1. `git add .`
- **What it does**: Stages all changes (new files, modified files, deleted files) in the **current directory** and its subdirectories.
- **How it works**: 
  - Adds all tracked and untracked files (except ignored ones) within the current directory and its subdirectories.
  - **Does not stage deleted files** that were removed using non-Git commands (like `rm`).
- **Use case**: Useful when you want to stage everything within your current directory but don't want to include deletions.

## 2. `git add --all` (or `git add -A`)
- **What it does**: Stages all changes (new, modified, and deleted files) in the **entire repository**, regardless of the current directory.
- **How it works**: 
  - Equivalent to running `git add .` followed by `git add -u`.
  - Stages all tracked and untracked files, **including deleted files** that were removed manually.
- **Use case**: Ideal when you want to stage absolutely everything in your repository, including file deletions.

## 3. `git add *`
- **What it does**: Stages changes to all files in the current directory that match the shell's glob pattern (`*`).
- **How it works**: 
  - Relies on your shell to expand the `*` wildcard, so it only adds files in the current directory (not subdirectories).
  - Stages changes only for files, not directories, and skips hidden files (those starting with a dot, like `.gitignore`).
- **Use case**: Useful if you want to quickly add all non-hidden files in the current directory, but not subdirectories.

## Summary of Differences

| Command           | New Files | Modified Files | Deleted Files | Hidden Files | Recursively Adds Subdirectories |
|-------------------|:---------:|:--------------:|:-------------:|:------------:|:------------------------------:|
| `git add .`       | ✅        | ✅             | ❌            | ✅           | ✅                             |
| `git add --all`   | ✅        | ✅             | ✅            | ✅           | ✅                             |
| `git add *`       | ✅        | ✅             | ❌            | ❌           | ❌                             |

## When to Use Each Command
- **`git add .`**: Use when you want to stage all changes in the current directory and subdirectories, excluding deletions.
- **`git add --all`**: Use when you want to stage all changes in the entire repository, including deletions.
- **`git add *`**: Use when you only want to stage non-hidden files in the current directory (not recursively).


## Key Notes

- `git add` stages changes, and `git commit` saves those changes in your local repository.
- `git push` uploads your local changes to the remote repository, and `git pull` downloads changes from the remote repository to your local machine.
- `git status` helps you track changes and see which files are staged, modified, or untracked.
