# Day 8: Basic Git & GitHub for DevOps Engineers

## Daily Log

**Date:** June 26, 2024

Today's focus was on understanding the fundamentals of Git and GitHub, essential tools for version control and collaborative software development. Exploring the concepts of version control, distributed version control systems, and the benefits of using Git over centralized version control systems provided valuable insights into modern software development practices.

## Key Concepts

### Git

Git is a distributed version control system that enables tracking changes to files and facilitates collaborative work among multiple individuals. It is widely utilized for software development and offers the ability to maintain a record of file changes, revert to previous versions, and merge changes made by different contributors into a unified file version.

### GitHub

GitHub is a web-based platform that hosts version control using Git. It provides distributed version control and source code management functionality, making it a popular choice for developers to share and collaborate on projects, including open-source initiatives.

### Version Control

Version control is a system that tracks changes to files over time, allowing users to recall specific versions later. It enables reverting files or the entire project to previous states, comparing changes over time, identifying contributors, and more.

### Types of Version Control Systems

There are two main types of version control systems:

- **Centralized Version Control Systems (CVCS)**: Utilize a central server to store all versions of a project's files.
- **Distributed Version Control Systems (DVCS)**: Allow developers to clone an entire repository, including the entire version history of the project, providing greater independence and flexibility.

### Advantages of Distributed Version Control

Using a distributed version control system offers several advantages over centralized systems, including better collaboration, improved speed, greater flexibility, and enhanced security.

## Tasks

### Getting Started with Git and GitHub

# Basics of Git

Git is a distributed version control system designed to handle everything from small to very large projects with speed and efficiency. Below are some basic Git commands and concepts to get you started.

## Installing Git

To install Git on your system, follow the instructions for your operating system:

- **Windows:** Download the installer from [git-scm.com](https://git-scm.com) and follow the instructions.
- **macOS:** Use Homebrew to install Git: `brew install git`.
- **Linux:** Use the package manager for your distribution, for example: `sudo apt-get install git` for Debian-based distributions.

## Basic Commands

- `git init`: Initializes a new Git repository in the current directory.
- `git clone`: Clones an existing repository into a new directory.
  - `git clone <repository-url>`
- `git status`: Displays the state of the working directory and the staging area.
  - `git status`
- `git add`: Adds changes from the working directory to the staging area.
  - `git add <file>`
  - To add all changes: `git add .`
- `git commit`: Records the changes in the repository.
  - `git commit -m "Commit message"`
- `git push`: Uploads local repository content to a remote repository.
  - `git push <remote> <branch>`
- `git pull`: Fetches and integrates changes from a remote repository to the local repository.
  - `git pull <remote> <branch>`
- `git branch`: Lists all the branches in the repository. Creates, deletes, or renames branches.
  - To create a new branch: `git branch <branch-name>`
  - To delete a branch: `git branch -d <branch-name>`
- `git checkout`: Switches branches or restores working tree files.
  - `git checkout <branch-name>`
  - To create and switch to a new branch: `git checkout -b <branch-name>`
- `git merge`: Merges changes from one branch into the current branch.
  - `git merge <branch-name>`

## Working with Remotes

- `git remote`: Manages the set of tracked repositories.
  - To add a new remote: `git remote add <name> <url>`
  - To remove a remote: `git remote remove <name>`
- `git fetch`: Downloads objects and refs from another repository.
  - `git fetch <remote>`

## Undoing Changes

- `git reset`: Resets the current HEAD to the specified state.
  - To unstage a file: `git reset HEAD <file>`
- `git revert`: Reverts some existing commits.
  - `git revert <commit>`

## Viewing History

- `git log`: Shows the commit history.
  - To view a summary of the commits: `git log --oneline`

### Exercises

1. **Create a New Repository on GitHub**: Establish a new repository on GitHub and clone it to your local machine.
2. **Make Changes and Commit**: Modify a file in the repository and commit the changes using Git.
3. **Push Changes to GitHub**: Push the committed changes back to the repository on GitHub.

By completing these exercises, you will gain practical experience in using Git and GitHub for version control and collaborative software development.

I have maintained the repo on github.

## Reflection

Understanding the core concepts of Git and GitHub has provided valuable insights into modern version control practices and collaborative software development. The ability to track changes, collaborate effectively, and maintain a comprehensive version history is essential for successful project management and software development.

## References

- [GitHub](https://github.com/): Official website for GitHub platform.
- [Git Downloads](https://git-scm.com/downloads): Official website for downloading Git.
- [Git and GitHub Master Class By Shubham Londhe](https://www.youtube.com/watch?v=AT1uxOLsCdk)

---

Happy Coding! 🚀

**Roshan Sahani**
