# Automating the following tasks for bugfix branches
- Creating a PR via the github cli
- Merging the PR via the github cli and checking for merge conflicts
- Deleting the local and remote branch after merging
- Pulling the latest changes from each branch into local repo

This assumes you are working on a bugfix branch and want to merge it into the main branch.
The bugfix branch can be named anything, and there is some basic checking for determining the main branch name.
See `create-and-merge-pr --help` for further options.
