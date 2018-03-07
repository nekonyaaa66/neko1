Common terms
============
master = trunk
remote/origin = server repo
checkout = switch


To initialize a git repo
========================
git init


To clone a repo
===============
git clone <repo url>


Status check [make this a habit before any actions]
===================================================
git status ( shows your current branch, working status, file changes, new files )


Branching / Checkouts
=====================
git branch ( shows you branches in your current local machine )
git branch -a ( shows you all branches, both local and remote)
git checkout <branch name> ( switch branch )
git checkout -b <branchname> (creates a new local branch, switches working copy to new branch)
git branch -D <branchname> (deletes local branch)
git push origin --delete <branchname> (deletes remote branch)
git log --graph --decorate ( fancy branch display )


Committing
==========
git add . ( adds all modified files. prep for pushing )
git add <filename> ( adds a specific file. prep for pushing )
git diff --staged ( show file changes )
git commit -m <message> ( commits file changes up to local repo with a commit message )
git push origin <remote branch> (commits current branch to specified remote branch)


Merge / Updates
===============
git merge <branchname> ( merges specified branch to current branch )
git fetch --all (fetches all branch changes )
git pull origin <branchname> ( update changes from specified branch )


Logs / file change checks
=========================
git log ( shows author, datetime, commit message, commit hash )
git log --oneline ( simplified log, showing shorten hash with commit message )
git shortlog ( groups file changes by user, commit messages )
git log -p -1 ( show file changes & line changes )
git blame <filename> ( shows line changes by date and user )
git show ( show simplified latest commit )
git diff-tree --no-commit-id --name-only -r <commit id> ( list file changes )
git log --stat --author="Jakeisgay" --oneline


Reverts
=======
git revert <commit hash> ( reverts all changes from that commit )
git reset --hard <commit hash> ( revert all changes, rebase HEAD)
git reset soft HEAD ( revert last commit. Edit your changes and recommit )
git reset ( reverts all adds )
git reset <filename> ( revert specific file adds )
git checkout . (reverts all local modifications )
git pull --rebase origin <branch> ( rebase local branch after revert on origin )


Stashing
========
git stash ( creates a temporary copy of all your modified changes, making your current state clean)
git stash show ( show all stash changes )
git stash pop ( pop stash changes to current branch )
git stash branch <branchname> ( pop stash changes to a new branch )
git stash drop

