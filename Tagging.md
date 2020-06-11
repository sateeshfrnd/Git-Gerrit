# Git Tag Command

Allow to add tags to specific commits, its an extra label for a commit that can indicate useful information(like, its beta release)

The command we'll be using to interact with the repository's tags is the git tag command:

```
$ git tag -a v1.0

flag -a : tells Git to create an annotated flag. If you don't provide the flag (i.e. *git tag v1.0*) then it'll create what's called a lightweight tag
```

**Note:** *The tag does not move around as new commits.*

*Annotated tags are recommended because they include a lot of extra information such as:*
  - *the person who made the tag*
  - *the date the tag was made*
  - *a message for the tag*

*Because of this, you should always use annotated tags.*

## Verify Tag
 To know is the tag was actually added to the project, by running the command:
 
 ```
 $ git tag
 ```
 
 ## Deleting A Tag
 A Git tag can be deleted with the -d flag (for delete!) and the name of the tag:
 ```
 $ git tag -d v1.0
 ```
 
 ## Adding A Tag To A Past Commit
 Running git tag -a v1.0 will tag the most recent commit. But what if you wanted to tag a commit that occurred farther back in the repo's history?
 
 All you have to do is provide the SHA of the commit you want to tag!
```
 $ git tag -a v1.0 s0209k
 ```
 
 ## Resources
  - [Git Basics - Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
  - [Git Tag](https://git-scm.com/docs/git-tag) 
 
