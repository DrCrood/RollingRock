# RollingRocks
Git Command Cookbook

## Checkout basic
  - git checkout code.cs  #use this to discard uncommitted code changes in code.cs

## Stash basic
- Case: made some changes on master branch but would like to apply the changes to a new branch instead.
  - git checkout master
  - make some changes
  - git stash
  - git branch newbranch
  - git checkout newbranch
  - git stash apply
  - continue to work on newbranch and then commit/push

## Branch basic
Always pull master branch and then create a new branch to make code updates.
- Case: create a new branch for code updates and then push the new branch to server for merge
  - git pull origin master
  - git checkout -b newbranch
  - make code changes
  - git add files-that-have-been-changed-and-need-to-be-pushed-to-server
  - git commit -m "commit comments"
  - git push -u origin newbranch
  - go to git server and make a pull requerst for newly updated changes

## Stage basic
  - git add code.cs  #stage a file for next commit
  - git reset HEAD code.cs  #unstage a file
  - git rm code.cs  #delete the file and stage the change

## Commit basic
  - git commit -m "comment"