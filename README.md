# GIT CHEAT SHEET

MAKE CHANGES Review edits and craft a commit transaction
$ git status Lists all new or modi?ed ?les to be committed
$ git add [file] Snapshots the ?le in preparation for versioning
$ git reset [file] Unstages the ?le, but preserve its contents
$ git diff Shows ?le di?erences not yet staged
$ git diff --staged Shows ?le di?erences between staging and the last ?le version
$ git commit -m "[descriptive message]" Records ?le snapshots permanently in version history

CONFIGURE TOOLING Con?gure user information for all local repositories
$ git config --global user.name "[name]" Sets the name you want attached to your commit transactions
$ git config --global user.email "[email address]" Sets the email you want attached to your commit transactions
$ git config --global color.ui auto Enables helpful colorization of command line output

CREATE REPOSITORIES Start a new repository or obtain one from an existing URL
$ git init [project-name] Creates a new local repository with the speci?ed name
$ git clone [url] Downloads a project and its entire version history

GROUP CHANGES Name a series of commits and combine completed e?orts
$ git branch Lists all local branches in the current repository
$ git branch [branch-name] Creates a new branch
$ git checkout [branch-name] Switches to the speci?ed branch and updates the working directory
$ git merge [branch] Combines the speci?ed branch’s history into the current branch
$ git branch -d [branch-name] Deletes the speci?ed branch

SAVE FRAGMENTS Shelve and restore incomplete changes
$ git stash Temporarily stores all modi?ed tracked ?les
$ git stash list Lists all stashed changesets
$ git stash pop Restores the most recently stashed ?les
$ git stash drop Discards the most recently stashed changeset

REVIEW HISTORY Browse and inspect the evolution of project ?les
$ git log Lists version history for the current branch
$ git log --follow [file] Lists version history for a ?le, including renames
$ git diff [first-branch]...[second-branch] Shows content di?erences between two branches
$ git show [commit] Outputs metadata and content changes of the speci?ed commit

SYNCHRONIZE CHANGES Register a repository bookmark and exchange version history
$ git fetch [bookmark] Downloads all history from the repository bookmark
$ git merge [bookmark]/[branch] Combines bookmark’s branch into current local branch
$ git push [alias] [branch] Uploads all local branch commits to GitHub
$ git pull Downloads bookmark history and incorporates changes
