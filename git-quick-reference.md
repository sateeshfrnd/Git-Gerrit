### Quick Reference
- Initialize or reinitialize a repository.
  - **git init**

- Copy existing repos from somewhere else to you local computer.
  - **git clone**

- Check the status of the repo
  - **git status**

- Add files from the working directory to the staging index
  - **git add <file>** : Add a file.
  - **git add -A** : Add new files, update modified files and remove deleted files.
  - **git add -u** : Update modified files and remove deleted files.

- Alter the most recent commit
  - **git commit --amend**

- Shows the details about the existing commits of a repository.
  - **git log**

- Shows the details about the given commit
  - **git show**
  
- Takes files from the staging index and save them in the repository.
  -**git commit -m "commit msg"**    : commit staged changes
  -**git commit -a -m "commit msg"** : stage and commit changes but ignores newly created files.

- Shows the difference between two versions of a file.
  - **git diff**

- Unstage all the files (allows to delete commits)
  - **git reset**
  
- Unstage a files
  - **git reset <filename>**
  
 - Discard last commit and checkout the commit done before
  - **git reset --hard HEAD~1**
 
 - Discard last 3 commit and revert back to the 4th last commit
  - **git reset --hard HEAD~3**
  
 - Delete file from the staging area and working directory
  - **git rm <fileName>**
 
 - Rename file
  -**git mv <file1> <file2>**
  
- Move the file
  -**git mv <file1> <dir>**

- Add tags to specific commits, its an extra label for a commit that can indicate useful information(like, its beta release)
  -**git tag <tag-name> <commit-id>** : Add a tag to a commit.
  
- Display all the tags
  -**git tag**

- Create a new Branch 
  -**git branch <branch-name>**

- Create a new Branch based on a commit
  -**git branch <branch-name> <sha-id>**

- Create a new Branch from a remote branch 
  -**git branch --track <branch-name> orign/<base-branch>**
  
- Delete a branch
  -**git -d <branch-name>

- Switch between different branches and tags.
  - **git checkout <branch-name/tag-name>**

- Add a remote named origin to a remote repository
  - **git remote add orign <rep-url>
  
- Verify the remotes
  - **git remote -v**
  
- Push the changes to a remote master branch, where origin is name of the remote you added
  - **git push orign master**
  
- Fetch from a remote repository 
  - **git fetch origin master**
  
- Merge a branch with current branch with another branch
  - **git merge <branch-name>**

- Fetch and merge from remote repository.
  - **git pull orign master**
  
- Revere the comit (provided SHA)
  - **git revert <sha-id>**
  
- Remove from the staging index
  - **git rm --cached**
  - It will not destroy any of your work; it just removes it from the Staging Index.
  - Eg: If you accidentally ran git add and gave it the wrong file, to discard changes by running below command:
  - **git rm --cached <file>...** 
  
- Save all the local changes
  - **git stash**
  
- Drop all the saved changes
  - **git stash pop**

- Apply all the previously saved changes
  - **git stash apply**
