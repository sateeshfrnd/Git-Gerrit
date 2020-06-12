# Merging
Combine the changes on different branches is called **Merging**.

Git can automatically merge the changes on different branches together. This branching and merging ability is what makes Git incredibly powerful! You can make small or extensive changes on branches, and then just use Git to combine those changes together.

**Note:**
  - *It's very important to know which branch you're on when you're about to merge branches together.*
  - *Making a merge makes a commit.*
  - *if you make a merge on the wrong branch, use below command to undo the merge*
    ```
    $ git reset --hard HEAD^
    (Make sure to include the ^ character! It's a known as a "Relative Commit Reference" and indicates "the parent commit".)
    ```
## The Merge Command
The git merge command is used to combine Git branches:
```
$ git merge <name-of-branch-to-merge-in>
```
When a merge happens, Git will:
  - look at the branches that it's going to merge
  - look back along the branch's history to find a single commit that both branches have in their commit history
  - combine the lines of code that were changed on the separate branches together
  - makes a commit to record the merge

Two main types of merges in Git:
  - Regular merge 
  - Fast-forward merge
    
 ### Fast-forward merge
 The branch being merged in must be ahead of the checked out branch. The checked out branch's pointer will just be moved forward to point to the same commit as the other branch.
 
 ### Regular merge :
 Combine two divergent branches, a merge commit is created as default.You can change the message if you want, but it's common practice to use the default merge commit message.
 
*When we merge, we're merging some other branch into the current (checked-out) branch. We're not merging two branches into a new branch. We're not merging the current branch into the other branch.*
 
## What If A Merge Fails?
Most of the time Git will be able to merge branches together without any problem. However, there are instances when a merge cannot be fully performed automatically. When a merge fails, it's called a merge conflict.

If a merge conflict does occur, Git will try to combine as much as it can, but then it will leave special markers (e.g. >>> and <<<) that tell you where you (yep, you the programmer!) needs to manually fix.

## What Causes A Merge Conflict
Git tracks lines in files. A merge conflict will happen when the exact same line(s) are changed in separate branches. Git isn't sure which line(s) you want to use from the branches that are being merged. So we need to edit the same line on two different branches...and then try to merge them.

## Merge Conflict Indicators Explanation
Following merge conflict indicators:
  - <<<<<<< HEAD everything below this line (until the next indicator) shows you what's on the current branch
  - ||||||| merged common ancestors everything below this line (until the next indicator) shows you what the original lines were
  - ======= is the end of the original lines, everything that follows (until the next indicator) is what's on the branch that's being merged in
  - '>>>>>>>' heading-update is the ending indicator of what's on the branch that's being merged in (in this case, the heading-update branch)
  
## Resolving A Merge Conflict
Git is using the merge conflict indicators to show you what lines caused the merge conflict on the two different branches as well as what the original line used to have. So to resolve a merge conflict, you need to:
  1. locate and remove all lines with merge conflict indicators
  2. choose which line(s) to keep

## Commit Merge Conflict
Once you've removed all lines with merge conflict indicators,just save the file, add it to the staging index, and commit it!

*Note:*
*Be careful that a file might have merge conflicts in multiple parts of the file, so make sure you check the entire file for merge conflict indicators - a quick search for <<< should help you locate all of them.*

 
 ## Resources
  - [Basic Merging from Git Book](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging#Basic-Merging)
  - [git-merge from Git Docs](https://git-scm.com/docs/git-merge)
  - [git merge from Atlassian blog](https://www.atlassian.com/git/tutorials/git-merge)
  - [Basic Merge Conflicts from the Git book](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging#Basic-Merge-Conflicts)
  - [How Conflicts Are Presented from the Git docs](https://git-scm.com/docs/git-merge#_how_conflicts_are_presented)
 
 
  
