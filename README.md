# Git Cheatsheet

Git is an immensely powerful version control tool that revolutionized the way developers manage their projects. Whether you're working on a small personal project or collaborating on a large-scale business application, Git offers an efficient and reliable solution for tracking changes made to files and folders.

To make working with Git even more convenient, here is an updated Git cheatsheet that has been carefully restructured and features better section titles. This cheatsheet serves as a handy reference for the most commonly used Git commands, allowing you to quickly access the information you need:

## Table of Contents

1. [Configuration](#configuration)
2. [Repository Initialization](#repository-initialization)
3. [Basic Operations](#basic-operations)
4. [Branching and Merging](#branching-and-merging)
5. [Remote Repositories](#remote-repositories)
6. [History and Undoing Changes](#history-and-undoing-changes)
7. [Collaboration](#collaboration)

## Configuration

Git configuration commands help you set up your identity and customize Git's behavior.

- `git config --global user.name [name]`: Set the name to be associated with your commits.
- `git config --global user.email [email]`: Set the email address to be associated with your commits.
- `git config --global user.username [username]`: Set the username to be associated with your commits.
- `git config --global color.ui auto`: Enable colored output in Git for improved readability.
- `git config --global core.editor [editor]`: Set the default text editor for commit messages.
- `git config --global core.autocrlf [true|false|input]`: Configure line ending conversions.
- `git config --global core.ignorecase [true|false]`: Set whether Git should be case-sensitive or case-insensitive.
- `git config --global alias.[alias-name] [command]`: Create a custom alias for a Git command.
- `git config --global core.pager [pager]`: Set the pager for displaying output in the command-line interface.
- `git config --global merge.tool [tool]`: Set the default merge tool to resolve conflicts.
- `git config --global diff.tool [tool]`: Set the default tool for viewing diffs.
- `git config --global push.default [matching|simple|current|upstream|nothing]`: Set the default behavior for pushing branches.
- `git config --global pull.rebase [true|false]`: Set whether `git pull` should perform a rebase by default.
- `git config --global branch.autosetuprebase [always|local|remote|none]`: Set automatic rebase behavior for new branches.

## Repository Initialization

Here are the Git commands related to repository initialization:

- `git init`: Create a new Git repository in the current directory. This command initializes an empty repository with the necessary Git files and folders.

- `git clone [repository]`: Clone an existing repository from a remote source to your local machine. This command creates a local copy of the remote repository, including all its branches, commit history, and files.

- `git remote add [remote] [url]`: Add a remote repository. This command associates a remote repository with your local repository, allowing you to fetch and push changes to and from the remote.

- `git remote -v`: List all remote repositories. This command displays the names and URLs of the remote repositories associated with your local repository.

These commands are used to establish and configure your Git repository, whether by initializing a new repository or cloning an existing one.

## Basic Operations

Perform fundamental Git operations to track changes and manage files.

- `git add [file]`: Add a specific file to the staging area.
- `git add .`: Add all changes in the current directory to the staging area.
- `git commit -m "[message]"`: Commit the staged changes with a descriptive message.
- `git status`: View the status of your working directory and staging area.
- `git diff`: Display the differences between the current state and the last commit.

## Branching and Merging

Branching and merging are essential concepts in Git that allow for parallel development and merging of changes. Here are the commands related to branching and merging:

- `git branch`: List all local branches in the repository. This command shows all the branches in your repository and highlights the currently checked out branch.

- `git branch [branch-name]`: Create a new branch based on the current branch. This command creates a new branch with the specified name, starting from the commit the current branch is pointing to.

- `git checkout [branch-name]`: Switch to a different branch. This command allows you to switch to the specified branch, making it the active branch in your working directory.

- `git merge [branch]`: Merge a branch into the current branch. This command incorporates changes from the specified branch into the current branch, creating a new merge commit if necessary.

- `git branch -d [branch-name]`: Delete a branch. This command deletes the specified branch from the repository. Note that the branch being deleted must not have unmerged changes.

- `git merge --abort`: Abort a merge in progress. This command aborts the current merge operation and restores the repository to the state before the merge began.

- `git stash`: Stash changes in a dirty working directory. This command saves the modifications in the working directory to a new stash, allowing you to switch branches without committing or losing changes.

- `git stash apply`: Apply the most recent stash to the current branch. This command applies the changes stored in the most recent stash to the working directory without removing the stash itself.

Branching enables you to work on different features or bug fixes simultaneously, keeping the changes isolated. Merging combines the changes from different branches, integrating them into a single branch. These commands provide the flexibility to manage and organize your development process effectively.

## Remote Repositories

Working with remote repositories is crucial for collaborating with others and sharing your code. Here are the Git commands related to remote repositories:

- `git remote add [remote] [url]`: Add a remote repository. This command associates a remote repository with your local repository, providing a name for the remote (e.g., "origin") and the URL of the remote repository.

- `git remote -v`: List all remote repositories. This command displays the names and URLs of all the remote repositories associated with your local repository.

- `git push [remote] [branch]`: Push local commits to a remote repository. This command sends your local commits to the specified remote repository and branch, updating the remote branch with your changes.

- `git pull [remote] [branch]`: Fetch and merge changes from a remote repository. This command retrieves the latest changes from the remote repository and automatically merges them into your current branch.

- `git fetch [remote]`: Download objects and references from a remote repository. This command fetches the latest changes from the remote repository without merging them into your branch, allowing you to review and merge them manually.

- `git clone [repository]`: Clone an existing repository from a remote source to your local machine. This command creates a local copy of the remote repository, including all its branches, commit history, and files.

- `git remote rm [remote]`: Remove a remote repository. This command removes the association between your local repository and the specified remote repository.

These commands enable you to interact with remote repositories, push your changes, fetch updates from others, and clone repositories for collaboration or personal use. Remote repositories are essential for team-based development and contributing to open-source projects.

## History and Undoing Changes

Git provides powerful features for managing commit history and undoing changes. Here are the Git commands related to history and undoing changes:

- `git log`: Display the commit history. This command shows a list of commits in reverse chronological order, including commit hashes, authors, dates, and commit messages.

- `git log --oneline`: Display a condensed commit history. This command provides a simplified view of the commit history, showing only the commit hashes and commit messages in a single line each.

- `git log --graph`: Display a commit history graph. This command visualizes the commit history as a graph, illustrating the relationships between different branches and commits.

- `git log [file]`: Display the commit history for a specific file. This command shows the commit history that affected the specified file, including changes, authors, and dates.

- `git reset [commit]`: Undo commits, moving the branch pointer to a previous commit. This command allows you to reset the current branch to a previous commit, discarding any commits after the specified commit. Be cautious when using this command as it can permanently discard commits.

- `git revert [commit]`: Create a new commit that undoes the changes made in a specific commit. This command creates a new commit that undoes the changes introduced by the specified commit, effectively reverting those changes without removing any commit from history.

- `git cherry-pick [commit]`: Apply the changes from a specific commit to the current branch. This command allows you to select and apply the changes from a specific commit onto the current branch, without merging the entire branch.

- `git reflog`: Display a log of all reference changes. This command shows a detailed log of all reference changes in your repository, including branch checkouts, commits, merges, and resets.

These commands enable you to explore and manage the commit history, undo changes at different levels, and selectively apply changes from specific commits. It's essential to use these commands with caution to avoid unintended data loss or conflicts.

## Collaboration

Advanced commands for collaborating with other developers.

- `git merge [remote]/[branch]`: Merge a remote branch into the current branch.
- `git branch -d [branch-name]`: Delete a branch.
- `git stash`: Stash changes in a dirty working directory. This command saves the modifications in the working directory to a new stash, allowing you to switch branches without committing or losing changes.

Refer to the official **[Git](https://git-scm.com/doc)** documentation and additional resources for more in-depth explanations and advanced usage of these commands.

With this comprehensive guide, you now have the knowledge to leverage Git effectively for version control, collaboration, and efficient project management. Happy coding!

[GitHub Cheat Sheet PDF 📕](https://training.github.com/downloads/github-git-cheat-sheet.pdf)
[Visual Git Cheat Sheet 🥽](https://ndpsoftware.com/git-cheatsheet.html#loc=index;)
[More Advanced Stuff 🔥](https://cs.fyi/guide/git-cheatsheet)
