# GIT Course UDEMY

Shortcuts to build or README files [HERE](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

## UI Tools for merging or solve conflicts 
- GitHub Desktop
- P4Merge 
- Visual Studio Code with git plugin


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

## Delete a file
`git rm <file_path>` ->  Moves the file to staging space.

## "Undelete" or unstage a file from staging
`git reset HEAD <file_path>` ->  Moves out the file from staging space, but it doesnt restores the file in the working directory.

`git checkout -- <file_path>` ->  Moves the file to the working directory again.

## Unstage a change already added
After `git add <file_path>`, `git reset HEAD <file_path>` ->  Returns to stage a commited change.

## Return a file to the remote repository version
`git checkout -- <file_path>` ->  Returns a file to the remote repository version.

## Fetch changes without merging them
`git fetch origin` ->  Retrieves commits, files, and references from the remote repository to local repository.

## Merge
`git merge <branch_from_where_we_want_to_merge_changes>` ->  Combines the current branch with the specified one.

## Rebase
`git rebase <base>` ->  It will put at the top the commits of the current branch over the commits of the base branch.

## Differences
`git diff <branch_one> <branch_two>` ->  Shows differences between two branches.

A Fast-Forward merge means that the changes coming from the branch were merged without any issue and will be the last changes in the current branch.
.orig files are the ones created when we have merge conflicts and a temporary file is created with both changes.

## History commands
`git log` ->  Displays commits history by commit.

`git log --abbrev-commit` ->  Displays commits history by commit and showing only the first 6-7 characters of the commit id.

`git log --oneline` ->  Displays commits history by commit in one line.

`git log --graph` ->  Displays commits history in an ASCII that represents the branching.

`git log --decorate` ->  Displays commits history by commit adding tags to describe info.

`git log --since="3 days ago"` ->  Displays commits history for the last 3 days.

`git log -- <file_path>` ->  Displays commits history for the specified file.

`git log --follow -- <file_path>` ->  Displays commits history for the specified file reviewing file name changes.

`git log --oneline --graph --decorate` ->  Example of combination.

`git show <commit_id>` ->  Displays information of the specified commit.

## Branching Commands
`git branch -a` -> Show a list of branches in in the remote and our local repository.

`git branch <new_branch>` -> Creates a new branch based on the current one.

`git checkout <branch>` -> Switch to the specified branch.

`git checkout -b <new_branch>` -> Creates and switches to a new branch based on the current one.

`git branch -m <old_branch_name> <new_branch_name>` -> To rename a branch.

`git branch -d <branch_name>` -> To delete a branch (locally).

`git branch -D <branch_name>` -> To delete a branch (Remote repository).

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

# Git Aliases
Customization of git commands.
They are stored in the `~/.gitconfig` file, inside of the .git folder of the project or the git/etc/ folder in the GIT installation folder

- ` git config --global alias.<alias_name> "<git_command_plus_options>"`

Example:
Instead of typing`git log --all --graph --decorate --oneline` you can create an alias that executes that git command with a shorter instruction like `git hist`
- `git config --global alias.hist "log --all --graph --decorate --oneline"` -> Creates git hist alias


# Unwanted files (.gitignore)
File where we specify the files that we dont want that git tracks, usually is in the root folder of the project or we can create it manually. 
It can be done in three different ways:
- Specific file -> File.txt
- File pattern -> *.ext
- Folder -> my-folder/

One expression per line.
                              

# Rebasing

Examples
- feature branch with changes
- master branch with changes
  - Changes in both branches are in different files. 
- go to feature branch and run `git rebase master`, to get the latest changes from master, but put on the top the changes made by the feature branch.
- checkout master branch and `git merge <feature_branch>`, it will be a fast-forward merge since the changes were rebased, master changes first and then feature branch changes.
- go and commit and push changes in master.


## Abort a Rebase

Example
- feature branch with changes
- master branch with changes
  - Changes are in the same files
- go to feature branch and run `git rebase master`, to get the latest changes from master, an error is showed, there is a conflict.
- `git rebase --abort` will get us out of the rebase process letting the files are they were before the attempt to rebase.


## Fixing Rebase conflicts and continue

Example
- feature branch with changes
- master branch with changes
  - Changes are in the same files
- go to feature branch and run `git rebase master`, to get the latest changes from master, an error is showed, there is a conflict.
- Fix conflicts in files
- `git add <files_fixed_after_resolvd_conflict>` to add the new versions of the fixed files.
- `git rebase --continue` to continue with the rest of the rebase.

## Pull with Rebase

Example
- remote master with changes
- local master with changes
- `git pull --rebase origin master` -> Indicates we want remote master changes, but they will be rebased and we will our changes on top of the remote changes.


# Stashing
Stashing is about to save your work in progress in your current branch if you are not ready to commit it, while you change to another branch or need to do another stuff and your previous changes are not ready to be commited.

- `git checkout -b <feature_branch>` to create a feature branch based on master.
- Changes made in feature branch
- `git status` will show you your files changed.

Then you need to do some other urgent changes in another branch and your changes are not ready to be commited.

- `git stash` -> Will save your work in progress.
- `git status` will show you your working directory clean, since your work is already stashed.
- You make the changes in the proper files and commits them
- To recover your previous stashed changes you need to `git stash apply`
- `git status` will show you your working directory with the changes you were doing before stash.
- Commit changes
- `git stash list` to show the stashed changes, you can `git stash drop` to remove that from stashed work.
  - if you use `git stash pop` it will perform  `git stash apply` and then `git stash drop` 


Another Example (untracked files)

- New file created, this is an untracked file since GIT doesnt know it.
- if you do a `git stash` and then `git status` the file still appears because GIT is not tracking it.
- You can add the new file and then stash it.
  - Or you can do `git stash -u` to stash untracked files.

## Managing multiple stashed files

- branch with changes in one file
- `git stash save "changes in file 1"`
- do another change in another file
- `git stash save "changes in file 2"`
- do another change in another file
- `git stash save "changes in file 3"`
- `git stash list` to see the list of changes stashed.
- `git stash show stash@{1}` -> to show that specific element form the stashed list.
- `git stash apply stash@{1}` -> Applies that stashed change
- `git stash forp stash@{1}` -> removes that specific stashed change form the list.
  - `git stash clear` -> Cleans and empty all the stashed list.

## Staging into a branch
-
- Branch with a modified file already added with `git add <file>`
- Changes not ready to be commited.
- a New file not tracked yet.
- `git stash -u` to stash untracked files.
- `git stash branch <new_branch_name>` -> creates a new branch and moves all the changes to a new branch and switch to that branch
  - It will contain the modified and added file
  - The changes not commited yet.
  - The untracked files.

# Tagging
GIT tags are only labels for our branches to be able to differentiate them, GIT has some "default" tags like:
- `git log --oneline --decorate --all`
  - HEAD -> Its just a pointer
  - origin/HEAD and origin/master  branches in the remote repository
  - master is our local repository master branch.

Example

- `git tag myTag` -> will create "myTag" label
- `git log --oneline --decorate --all` will display the new tag also
- `git tags --list` -> will shows the tag list.
- `git show <tag_name>` -> will show the details of a tag.
- `git tag --delete <tag_name>` -> Deletes an specific tag.

## Annotated Tags
It has a little extra of information than a lightweight tag.

- `git tag -a <tag_name>` -> Option to say that it will be an annotated tag.

## Comparing tags
- `git diff <tag_name1> <tag_name2>`

## Tagging an specific commit 
- `git tag -a <tag_name> <commit_id>`

## Updating tags
- `git tag -a <tag_name> -f <commit_id>`

## Tags with GitHub
- `git push origin <tag_name>` --> Will send to GitHub the specified tags to "Releases" section.
- `git push origin master --tags` --> will send to Github all the tags in master branch.
- `git push origin :<tag_name>` -> Removes from the remote repository that tag, it keeps in the local repository.


