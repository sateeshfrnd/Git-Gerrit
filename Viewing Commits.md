# View Commits
Shows the detailed information about the existing commits of a repository.

By default, this command displays the **SHA,author,date,message** of every commit in the repository.

Git uses the command line pager, Less, to page through all of the information. The important keys for Less are:

 - to scroll down by a line, use j or ↓
 - to scroll up by a line, use k or ↑
 - to scroll down by a page, use the spacebar or the Page Down button
 - to scroll up by a page, use b or the Page Up button
 - to quit, use q
 
 ## git log --oneline
 The *git log* command has a flag *--oneline* that shows:
 - lists one commit per line
 - shows the first 7 characters of the commit's SHA
 - shows the commit's message
 ```
 $ git log --oneline
 ```

 ## git log --stat
 The git log command has a flag *--stat* ("stat" is short for "statistics") that shows:
  - displays the file(s) that have been modified
  - displays the number of lines that have been added/removed
  - displays a summary line with the total number of modified files and lines that have been added/removed
 
  ```
 $ git log --stat
 ```
 
 ## git log -p
 The git log command has a flag that can be used to display the actual changes made to a file. The flag is --patch which can be shortened to just -p:
   
 ```
 $ git log -p
 ```
 Coomand shows:
   - the file that have been modified.
   - the hash of the first version of the file and the hash of the second version of the file
   - the old version and current version of the file
   - the location of the lines that have been added/removed
   - the actual changes that have been made in the commit
   
 **git log -p -w** will show the patch information, but will not highlight lines where only *whitespace* changes have occurred.
 
 ## --graph and --all flags
 The --graph flag adds the bullets and lines to the leftmost part of the output. This shows the actual branching that's happening. The --all flag is what displays all of the branches in the repository.
  
 Running this command will show all branches and commits in the repository:
 ```
  $ git log --oneline --decorate --graph --all
 ```

## Filter By Author
We can display all of the commits by an author is to use the regular git log command but include the --author flag to filter the commits to the provided author.
```
$ git log --author="Tejaswini"
```

## Filter commits with patteren maching in commit
We can filter down to just the commits that reference the word "bug". We can do that with either of the following commands:
```
$ git log --grep="bug fix"
$ git log --grep "bug fix"
```
 
## Group By Commit Author
Using the **git shortlog**, we can get how many commits each contributor has added to the repository.
```
 $ git shortlog
```
Displays an alphabetical list of names and the commit messages that go along with them.
 
If we just want to see just the number of commits that each developer has made, we can add a couple of flags: -s to show just the number of commits (rather than each commit's message) and -n to sort them numerically (rather than alphabetically by author name).

```
$ git shortlog -s -n
```

 
 
 
