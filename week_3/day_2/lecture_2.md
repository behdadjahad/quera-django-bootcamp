# lecture 2 (12:00 - 13:30)

## git 

+ centralized version control
+ distributed version control
+ git lfs (for large projects)
  
### git areas

+ Untracked
+ Unmodified
+ Modified
+ Stages


'`git add`' command added files from untracked to staged

'`git commit -m 'commit msg'`' command added files from staged area to unmodified

when we edit tracked files we added them from unmodified to modified area

``` console
$ git init
$ git touch quera.txt
$ git status 
$ git add filename.txt
$ git commit -m 'commit msg'
```
simple git commands


``` console
$ git log
```
will show all git commits


```
git checkout [commit-hash]
```
go back to that specific  commit 


```console 
$ git rm -cached quera.txt
```

this command will remove file from staging area

+ note : do not change or remove .git directory files

