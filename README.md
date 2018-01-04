# GIT CHEAT SHEET

* [Create repositories](#createRepo)
* [Configure tool](#confTool)
* [Make changes](#makeChange)
* [Synchronise changes](#syncChanges)
* [Group changes](#groupChanges)
* [Save fragments](#saveFrag)
* [Review history](#revHistory)



## CREATE REPOSITORIES <a id=createRepo></a>

*Start a new repository or obtain one from an existing URL*
- **git init [project-name]** Creates a new local repository with the specified name
- **git clone [url]** Downloads a project and its entire version history


## CONFIGURE TOOLING <a id=confTool></a>

*Conigure user information for all local repositories*
- **git config --global user.name "[name]"** Sets the name you want attached to your commit transactions
- **git config --global user.email "[email address]"** Sets the email you want attached to your commit transactions
- **git config --global color.ui auto** Enables helpful colorization of command line output


## MAKE CHANGES <a id=makeChange></a>

*Review edits and craft a commit transaction*
- **git status** Lists all new or modifed files to be committed
- **git add [file]** Snapshots the file in preparation for versioning
- **git reset [file]** Unstages the file, but preserve its contents
- **git diff** Shows file diferences not yet staged
- **git diff --staged** Shows file diferences between staging and the last file version
- **git commit -m "[descriptive message]"** Records file snapshots permanently in version history


## SYNCHRONIZE CHANGES <a id=syncChanges></a>

*Register a repository bookmark and exchange version history*
- **git fetch [bookmark]** Downloads all history from the repository bookmark
- **git merge [bookmark]/[branch]** Combines bookmark’s branch into current local branch
- **git push [alias] [branch]** Uploads all local branch commits to GitHub
- **git pull** Downloads bookmark history and incorporates changes


## GROUP CHANGES <a id=groupChanges></a>

*Name a series of commits and combine completed efforts*
- **git branch** Lists all local branches in the current repository
- **git branch [branch-name]** Creates a new branch
- **git checkout [branch-name]** Switches to the specified branch and updates the working directory
- **git merge [branch]** Combines the specified branch’s history into the current branch
- **git rebase [branch]** Combines the specified branch’s history after all the changes in the current branch
- **git branch -d [branch-name]** Deletes the specified branch
- **git tag [tag-name]** Create tag of merge


## SAVE FRAGMENTS <a id=saveFrag></a>

*Shelve and restore incomplete changes*
- **git stash** Temporarily stores all modified tracked files
- **git stash list** Lists all stashed changesets
- **git stash pop** Restores the most recently stashed files
- **git stash drop** Discards the most recently stashed changeset


## REVIEW HISTORY <a id=revHistory></a>

*Browse and inspect the evolution of project files*
- **git log** Lists version history for the current branch
- **git log --follow [file]** Lists version history for a file, including renames
- **git diff [first-branch]...[second-branch]** Shows content diferences between two branches
- **git show [commit]** Outputs metadata and content changes of the specifed commit