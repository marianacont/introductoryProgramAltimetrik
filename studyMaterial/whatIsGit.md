#Documentation
##What is GIT and GitHub?

Git is a version management system that allows you to manipulate the different versions of the development of a product. The goal is to have control of all the changes made and to be able to roll back if necessary.
Git works with local and remote repositories, so it allows you to work in groups. The best known remote repository is GitHub.

###Most common commands
- Getting & Creating Projects
  + git init:  Initialize a local Git repository
  + git clone ssh://git@github.com/[username]/[repository-name].git: 	Create a local copy of a remote repository
- Basic Snapshotting
  + git status: Check status
  + git add [file-name.txt]: Add a file to the staging area
  + git add -A: Add all new and changed files to the staging area
  + git commit -m "[commit message]": Commit changes
  + git rm -r [file-name.txt]: Remove a file (or folder)
- Branching & Merging
  + git branch: List branches
  + git branch [branch name]: Create a new branch
  + git branch -d [branch name]: Delete branch
  + git merge [branch name]: Merge a branch into the active branch
  + git stash: Stash changes in a dirty working directory
- Sharing & Updating Projects
  + git push origin [branch name]: Push a branch to your remote repository
  + git push -u origin [branch name]: Push changes to remote repository (and remember the branch)
  + git pull: Update local repository to the newest commit
  + git pull origin [branch name]: Pull changes from remote repository
  + git remote add origin ssh://git@github.com/[username]/[repository-name].git: Add a remote repository
- Inspection & Comparison
  + git log: View changes
  + git diff [source branch] [target branch]: Preview changes before merging

##Git Branches
 Each branch of a project saves different versions of it. Git branches are effectively a pointer to a snapshot of your changes. When you want to add a new feature or fix a bug—no matter how big or how small—you spawn a new branch to encapsulate your changes.

By developing the features in branches, it’s not only possible to work on each one in parallel, but it also keeps the main branch free from questionable code.

###Git tags
Tags are references that point to specific points in Git history. A tag is like a branch that doesn’t change. Unlike branches, tags, after being created, have no further history of commits. 
To create a tag use the command: git tag [tagname]
A common pattern is to use version numbers like git tag v1.4. Git supports two different types of tags, annotated and lightweight tags. A best practice is to consider  Lightweight tags as private and Annotated tags (with extra data such as: the tagger name, email, and date) as public.

###Git commit
The git commit command captures a snapshot of the project's currently staged changes. Committed snapshots can be thought of as “safe” versions of a project.
The commit is done locally, and the changes will be updated in the remote repository whenever the developer wishes. It makes it easier to split up a feature into atomic commits, keep related commits grouped together, and clean up local history before publishing it to the central repository

###Git Stash
Git stash temporarily shelves (or stashes) changes you've made to your working copy so you can work on something else, and then come back and re-apply them later on. Stashing is handy if you need to quickly switch context and work on something else, but you're mid-way through a code change and aren't quite ready to commit.
You can reapply previously stashed changes with git stash pop. Popping your stash removes the changes from your stash and reapplies them to your working copy.

###Links
Git and Github tutorial: https://youtube.com/playlist?list=PLQxX2eiEaqby-qh4raiKfYyb4T7WyHsfW
GitHub commands: https://github.com/joshnh/Git-Commands 
Atlassian Git Tutorial: https://www.atlassian.com/git/tutorials 
