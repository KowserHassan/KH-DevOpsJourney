# Essential Git Commands

## Initialise a new Git Repository

| Command       | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| `git init`    | Initialises a new git repository in the current directory by creating a `.git` folder in the project. |

## Git Add

| Command                 | Description                                               |
|-------------------------|-----------------------------------------------------------|
| `git add filename`    | Adds a specific file to the staging area.                 |
| `git add -A`             | Stages new, modified, or deleted files.                   |
| `git add .`              | Stages new and modified files.                            |
| `git add -u`             | Stages modified and deleted files.                        |

## Git Commit

| Command                          | Description                                                                 |
|----------------------------------|-----------------------------------------------------------------------------|
| `git commit -m "your text"`      | Commits staged changes with a message describing the changes.               |

## Git Status

| Command         | Description                                                   |
|-----------------|---------------------------------------------------------------|
| `git status`    | Lists files in green (staged but not committed) or red (not staged). |

## Working with Branches

| Command                           | Description                                                               |
|-----------------------------------|---------------------------------------------------------------------------|
| `git branch branch_name`          | Creates a new branch.                                                     |
| `git checkout branch_name`        | Switches to a specific branch.                                             |
| `git checkout -b branch_name`     | Creates a new branch and switches to it automatically.                     |
| `git branch`                      | Lists all branches and shows the current branch.                           |

## Git Log

| Command             | Description                                                   |
|---------------------|---------------------------------------------------------------|
| `git log`           | Lists the version history for the current branch.              |
| `git log --oneline` | Shows a concise version of the commit history (one line per commit) |

## Push & Pull

| Command       | Description                                                              |
|---------------|--------------------------------------------------------------------------|
| `git push`    | Sends committed changes to a remote repository.                          |
| `git pull`    | Pulls changes from a remote server to your local computer.                |

## Tips & Tricks

| Command                                   | Description                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| `git reset --hard`                        | Throws away all uncommitted changes.                                              |
| `git reset file_name`                     | Removes a file from git without removing it from the local computer.              |
| `echo filename >> .gitignore`             | Adds a file to `.gitignore` to avoid accidentally committing it again.            |
| `git commit --amend -m "New message"`     | Edits a commit message.                                                           |
