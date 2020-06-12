# Resetting Commits
Reset or erase the commits from the repository.

## The git reset Command
The git reset command is used to reset (erase) commits:
```
$ git reset <reference-to-commit>
```
It can be used to:
  - move the HEAD and current branch pointer to the referenced commit
  - erase commits
  - move committed changes to the staging index
  - unstage committed changes
  
## Git Reset's Flags
The way that Git determines if it erases, stages previously committed changes, or unstages previously committed changes is by the flag that's used. The flags are:

  - *--mixed :* unstages committed changes
  - *--soft :* moves committed changes to the staging index
  - *--hard :* erase commits
  
 ## Relative Commit References
 There are special characters called "Ancestry References" that we can use to tell Git about these relative references. Those characters are:
  - '^' : indicates the parent commit
  - '~' : indicates the first parent commit
  
 **Note:**
  - Before restting, create a 'backup' branch on the most-recent commit so that I can get back to the commits.
 
 ## Resources 
  - [git-reset from Git docs](https://git-scm.com/docs/git-reset)
  - [Reset Demystified from Git Blog](https://git-scm.com/book/en/v2/Git-Tools-Reset-Demystified)
  - [Ancestry References from Git Book](https://git-scm.com/book/en/v2/Git-Tools-Revision-Selection#Ancestry-References)
