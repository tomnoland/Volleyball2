# Git Procedures

## Common Branches:

* **development:**  This is the branch we use as the basis of all development
* **more to come:** There will be another 3-5 common branches


## Branches for tickets

### Feature
For adding a new feature or functionality
  
`feature/[your initials]_[zoho number]_[what is it]`

### Fix
For repairing something broken: 

`feature/[your initials]_[zoho number]_[what is it]`

## Working on a Ticket Process

### Leave a terminal window or tab open that is set to the 
app root ( /siteboxfolder/app ).  **Always perform git operations from here.**


1: switch to development and synchronize it with the origin repo.
```
    git checkout development
    git pull origin development
```

2: create a branch for your ticket: 
( but, you say, what if i do not have a zoho ticket? Well.. if the work is authorized, 
please make one and assign it to yourself )
``` 
    git checkout -b [feature or fix]/[initials]_[zoho number]_[some feature name]
```

3: Do some amazing stuff in your branch.

* While you are coding, commit early and often.
  * This provides you with several backups in case you 
    break something while coding
    * After you got something to work
    * Before you are about to do a big thing.
  * ALWAYS push your commits to the remote
    * This is a backup copy of your work in case something 
      happens to your system
    * This also provide a way for someone else on the team to 
      help you.
      
4: Make a commit: 
This makes a 'snapshot' of your 
```
  git add -A .
  git commit -m 'a memo to identify what you did, you know a note to yourself and others'
```

5: Push a commit: 
This copies your changes to the gitlab repository
``` 
  git push origin HEAD
```


## Backmerge when you are finished with a ticket 
**Backmerge** and test.  This means you get the latest copy of the development
branch and merge it into your own branch.

1: make sure you committed your changes and pushed
```
    git add -A .
    git commit -m 'note to self'
    git push origin HEAD
```
  
2: switch to the development branch and pull the latest from the repo
``` 
  git checkout development
  git pull origin development
```

3: switch back to your branch 
```  
  git checkout your_very_nice_branch
```

4: merge development into your branch
``` 
  git merge development
```

5: If git tells you there were conflicts, then fix them in each file

6: Test everything and make adjustments if needed.

7: commit your changes and push
```
    git add -A .
    git commit -m 'note to self'
    git push origin HEAD
```

8: goto the git lab page for the repo and create a merge request.



