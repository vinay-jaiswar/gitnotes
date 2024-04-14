## Git & GitHub Notes

Resources:

1. https://unwiredlearning.notion.site/unwiredlearning/Git-GitHub-Resources-15b88c990e484f9880046db7acffce76

Installation:

> git --version

Configuration:

- Set your name and email address

  > git config --global user.name "Your Name"

  > git config --global user.email "your.email@example.com"

> git config --list

lists all the Git configuration settings

CMD Shortcuts:

1. `code .`
   opens the current directory in Visual Studio Code

Git Lifecycle:
![Git Lifecycle](https://milad-ezzat.vercel.app/static/images/git/git-4-phases.png)

Basic Git commands:

1. `git init`: Initializes a new Git repository.
2. `git add <file>`: Adds a file to the staging area.
3. `git add . or git add --all`: Adds all changes in the working directory to the staging area.
4. `git commit -m "Commit message"`: Commits staged changes with a descriptive message.
5. `git branch -M main`: Rename the branch to main and set it as the new default branch.
6. `git remote add origin repository_link`: Add the remote repository URL.
7. `git push -u origin main`: Push the main branch to the remote repository.
8. `git status`: Shows the current status of the repository.
9. `git log`: Displays the commit history.
10. `git branch`: To list all branches.
11. `git log --oneline`: command displays a simplified version of the commit history.

**HEAD -> main:** It points to the last commit in the current branch.

**Git diff**: used to show the changes between different states.

1. `git diff`: changes between the working directory and the staging area.
2. `git diff <commit1> <commit2>`: Difference between two commits.

**Git stash**: used to temporarily store changes that are not ready to be committed yet.

1. `git stash`: Stashes working directory changes.
2. `git stash pop`: To apply and remove the most recent stash.
3. `git stash pop <stash_number>`: Applies a specific stash and removes it from the stash list.
4. `git stash save "Work in progress`": Stash changes with a descriptive message.
5. `git stash list`: To list all stashed changes.
6. `git stash apply`: Applies the most recent stash without removing it from the stash list.
7. `git stash apply <stash_number>`: To apply a specific stash.
8. `git stash clear`: Deletes all stashed changes from the stash list.
9. `git stash drop`

**Git restore**:

1. `git restore <file>`: Discards changes and restores it to the state at the last commit.
2. `git restore --staged <file>`: Unstages changes, moving them from the staging area back to the working directory.

**Branches**:

1. `git branch <branch_name>`: Creates a new branch.
2. `git checkout <branch_name>`: switches your working directory to the specified branch.
3. `git merge <branch_name>`: merges the specified branch into the currently checked-out branch.
4. `git branch -d <branch_name>`: Deletes the specified branch.
   _Use -D to force delete a branch_
5. `git push origin --delete <branch_name>`: deletes the specified branch from the remote repository.
6. `git branch -r`: used to list all remote branches.
7. `git branch -v`: used to list all local branches with last commit message and commit hash.
8. `git branch --merged`: To list branches that have been merged into the current branch.
9. `git branch --no-merged`: To list branches that have not been merged into the current branch.

**Git pull**: used to fetch changes from a remote repository and merge them into the current branch.

- `git pull <remote_name> <branch_name>`

**Git Shortcuts**:

1. `git commit -a -m "Your commit message here"`: shortcut for staging all modified files and committing them.
2. `git checkout -b <branch_name>`: To create a new branch and switch to it

**Git rebase**:

- `git rebase <branch_name>`: used to integrate changes from one branch onto another branch.

  After resolving conflicts, use `git rebase --continue` to proceed with the rebase.

> _.gitignore_ file is used to specify intentionally untracked files

**Git squash**: used to combine multiple commits into a single commit.

- `git rebase -i HEAD~<number_of_commits>`

**Git revert**: used to undo changes by a specific commit or commits.

- `git revert <commit_hash>`

**Git reset**: used to reset the current branch to a specific state.

1. `git reset --soft <commit`>: Keeps changes in the staging area and working directory.
2. `git reset --mixed <commit>`: Resets the staging area to match the specific commit, while keeping changes in the working directory. (Default)
3. `git reset --hard <commit>`: discarding all changes.

> `git reset <commit> <file>`

**Git tag**: a way to mark specific points in your commit history as significant.

1. `git tag`: To list all tags in the repository.
2. `git tag <tag_name>`: To create a tag for the current commit.
3. `git push origin <tag_name>`: To push tags to a remote repository.
4. `git tag -d <tag_name>`: To delete a tag locally.
5. `git push --delete origin <tag_name>`: To delete a tag on the remote repository.

**Git clone**: used to create a copy of an existing Git repository.

- git clone https://github.com/example/repository.git

> `git remote rm origin`: removes the remote named "origin" from your local repository configuration.

> **upstream** refers to the original repository from which a fork was created.
