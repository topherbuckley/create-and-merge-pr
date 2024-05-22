# Automating the following tasks for bugfix branches
- Creating a PR via the github cli
- Merging the PR via the github cli and checking for merge conflicts
- Deleting the local and remote bugfix branch after merging
- Pulling the latest changes from main branch into local repo

This assumes you are working on a bugfix branch and want to merge it into the main branch.
The bugfix branch can be named anything, and there is some basic checking for determining the main branch name.
See `create-and-merge-pr --help` for further options.

By default this assumes your fork is named `origin` and the upstream is named `upstream`. but you can specify the names of the remotes using the `--origin` and `--upstream` flags.
You can call this script even before pushing to your fork, or after, but it will not fix things for you if you accientally push to upstream directly. In that case it will just push an identical commit to your fork and create a PR from there.

# Usage
1. Clone the repo you want to work on (I assume this is refered to as upstream in your remotes)
2. Fork the repo on github (I assume this is refered to as origin in your remotes)
3. Create a new branch for your bugfix. Call it whatever you want, but this should be based on the main branch of the upstream repo to avoid merge conflicts.
4. Make your changes and commit them to your bugfix branch on your fork (i.e. `origin`)
5. Run the script. e.g. `create-and-merge-pr`
6. Follow the prompts to create a PR and merge it
7. If there are merge conflicts, resolve them and run the script again
