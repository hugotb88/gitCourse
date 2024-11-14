# GIT Course UDEMY

Shortcuts to build or README files [HERE](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

## GIT Local workspace
- Working Repository
- Staging (Pre-Commit)
- Repository (Local / .git folder)

-  Remote Repository

## Commands
`git version` ->   Returns installed GIT Version

`git config user.name` ->   Configures the user of GitHub, only for that specific repository.

`git config user.email` ->   Configures the email of GitHub, only for that specific repository.

`git config --global user.name` ->   Configures the user of GitHub, for all the repositories.

`git config --global user.email` ->   Configures the email of GitHub,for all the repositories.

`git init` ->  creates .git folder in the current directory

`git config --global init.defaultBranch` -> Set the name of the default branch for all the repositories.


## Clone an existing repository
`git clone <repo_url>` ->  Clones remote repository into local.

## Review status of local repository
`git status` ->  Shows new, modified or delted files in the current workspace.

## Add new file
`git add <path_new_file>` ->  Adds new file to staging, before commit to local repository and push to remote repository.

## Update the index after an addition of a new file
`git add <path_new_file>` ->  Adds new file to staging, before commit to local repository and push to remote repository.

`git add -u` ->  Updates the index.

## Move new file to local repository (.git folder)
`git commit <path_new_file>` ->  Commits new file to local repository, before  push to remote repository.

## Push new file to remote repository (.git folder)
`git push origin <branch_remote_repository>` ->  Pushes new file to remote repository.

## Unstage a change already added
After `git add <file_path>`, `git reset HEAD <file_path>` ->  Returns to stage a commited change.

## Return a file to the remote repository version
`git checkout -- <file_path>` ->  Returns a file to the remote repository version.

## Fresh repository
- `git init <project_name>` ->  Creates a new GIT project (folder project and .git folder).
- Create new files in the project folder (like "vic.txt" file)
- `git status` -> to see the new files created.
- `git add vic.txt` -> Adds new file to staging area.
- `git commit` -> Moves new file to repository area, ready to be pushed to remote repository
  - You need to add a Commit message
- Create the remote repository in GitHub.com
- `git remote add origin <url_to_remote_repository>` -> Indicates to your local repo which one is the remote repo.
- `git push origin <destination_branch>` -> Pushes the commited changes into the remote repository.

## Existing repository
- Move to the root folder of your local project
- `git init ` -> Starts git repository and creates .git folder.
- `git add .` -> Adds all the files in the current folder to the staging area.
- `git commit` -> Moves new files to repository area, ready to be pushed to remote repository
  - You need to add a Commit message
- Create the remote repository in GitHub.com
- `git remote add origin <url_to_remote_repository>` -> Indicates to your local repo which one is the remote repo.
- `git push origin <destination_branch>` -> Pushes the commited changes into the remote repository.

- `git push origin <destination_branch>` -> Pushes the commited changes into the remote repository.


## Existing remote repository
- `git clone <url_remote_repository>` -> Makes a copy of the remote repository in your local.
- Create new files in the project folder (like "vic.txt" file)
- `git status` -> to see the new files created.
- `git add vic.txt` -> Adds new file to staging area.
- `git commit` -> Moves new file to repository area, ready to be pushed to remote repository
  - You need to add a Commit message
- `git push origin <destination_branch>` -> Pushes the commited changes into the remote repository.
