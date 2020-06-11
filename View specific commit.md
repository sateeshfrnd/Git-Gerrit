# git show

The git show command will show only one commit, the most recent commit. If a SHA is provided as a final argument then shows that particular commit.

```
$ git show

$ git show sat29ish
```

git show displays:
  - the commit
  - the author
  - the date
  - the commit message
  - the patch information
  
However, git show can be combined with most of the other flags we've looked at:
  - Flag --stat - to show the how many files were changed and the number of lines that were added/removed
  - Flag -p or --patch - this the default, but if --stat is used, the patch won't display, so pass -p to add it again
  - Flag -w - to ignore changes to whitespace
