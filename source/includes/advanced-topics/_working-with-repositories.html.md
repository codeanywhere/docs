## Working with repositories
With Codeanywhere, you’ll be able to work directly with your repositories. You can work with your resository using standard git commands inside your SSH terminal. Right click on your Container and select SSH Terminal in order to open it up.

### Setting up a Repository
Create a new local repository:

~~~~
git init
~~~~

Create a new repository out of a directory:

~~~~
git init <directory> 
~~~~

Create a copy of an existing repository inside Container:

~~~~
git clone /path/repository_name.git 
~~~~

Create a copy of an existing repository inside Container into an directory:

~~~~
git clone /path/repository_name.git <directory>  
~~~~

Create a copy of an private repository inside Container:

~~~~
git clone username@host:/path/repository_name.git 
~~~~

### Saving changes
Stage all changes in a file for next commit:

~~~~
git add <filename> 
~~~~

Stage all changes in a folder for next commit:

~~~~
git add <foldername> 
~~~~

Add all files to staging:

~~~~
git add * 
~~~~

Commit changes to head:

~~~~
git commit -m "Commit message" 
~~~~

Commit all changes in the working directory:

~~~~
git commit -a 
~~~~

### Inspecting a Repository
List which files are staged, unstaged, and untracked:

~~~~
git status 
~~~~

Display the entire commit history using the default formatting:

~~~~
git log 
~~~~

### Connecting to a remote Repository
Add the server to be able to push to it:

~~~~
git remote add origin <server> 
~~~~

List all currently configured remote repositories:

~~~~
git remote -v 
~~~~

### Working with branches

Create a new branch and switch to it:

~~~~
git checkout -b <branchname>
~~~~

Switch from one branch to another:

~~~~
git checkout <branchname> 
~~~~

List all the branches in your repo, and also tell you what branch you're currently in:

~~~~
git branch 
~~~~

Delete the feature branch:

~~~~
git branch -d <branchname> 
~~~~

Push the branch to your remote repository, so others can use it:

~~~~
git push origin <branchname> 
~~~~

Push all branches to your remote repository:

~~~~
git push --all origin 
~~~~

Delete a branch on your remote repository:

~~~~
git push origin :<branchname> 
~~~~

For example, if you want to push to your master branch, just use:

~~~~
git push origin master 
~~~~

### Update to a remote repository

Merge changes on the remote server to your Container:

~~~~
git pull 
~~~~

Merge a different branch into your active branch:

~~~~
git merge <branchname> 
~~~~

View all the merge conflicts

~~~~
git diff 
~~~~
