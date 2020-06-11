# Branching

Git allows to create multiple lines of development. 
Eg: Develop different features of the project in parallel without getting confused as to which commits belongs to which feature.

## The git branch command
The git branch command is used to interact with Git's branches:

```
$ git branch
```

It can be used to:
  - list all branch names in the repository
  - create new branches
  - delete branches
  
If we type out just *git branch* it will list out the branches in a repository.

## Create A Branch
To create a branch, all you have to do is use *git branch* and provide it the name of the branch you want it to create. 
So if you want a branch called "sprint_1", you'd run this command:

```
$ git branch sprint_1
```
## Switch Branches
To switch between branches we need to use git **checkout** commmand.

```
$ git checkout <branch_name>
```
**Note:**
*When we switch branch, remove all the files and directories from the working directory that are referenced by the current branch. It will replace them with the files that are referenced by the commits with the branch that you switched.*

Create branch from particular SHA, by providing SHA to git branch command, like:
```
$ git branch <branch_name> SHA
```

## Delete A Branch

A branch is used to do development or make a fix to the project that won't affect the project (since the changes are made on a branch). Once changes are merged into the master branch, you probably won't need the branch anymore. If you want to delete the branch, you'd use the -d flag. 

```
$ git branch -d <branch_name>
```

**Note:**
  - *You can't delete a branch that you're currently on. So to delete the sidebar branch, you'd have to switch to either the master branch or create and switch to a new branch.* 
  
## References
  - [Git Branching - Basic Branching and Merging](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)
  - [Learn Git Branching](http://learngitbranching.js.org/)
  - [Git Branching Tutorial from the Atlassian Blog](https://www.atlassian.com/git/tutorials/using-branches)







