# Git Tutorial

![gitphdcomic](http://swcarpentry.github.io/git-novice/fig/phd101212s.png)

Git is a source control managment solution for multiple people.

## Branches, commits and pushing stuff

```
git clone https://tbi-gitlab.dkfz.de/saary/gittutoria
cd gittutorial
git status
```

Whats the status of the git repository?


### Staging, index, commits

Files in the *staging* stage are changed and added via `git add FILE` but not 
part of a commit yet.

A *commit* is the *staged* files bundled together to form a useful unit of 
change. It is created via `git commit -m "message"` after files are added to 
staging.

The *HEAD* is the position we are in the git graph.

![image](https://git-scm.com/book/en/v2/images/areas.png)


## Changing files


```
git checkout dev                                # go into the right branch
[.. work on some files...]                      # do normal work
add newfile newfile2 newfile3                   # add the new and changed files
# now we have many changes in staging
commit -m "I made many new files which do X"    # create a new commit
# now we have a local commit
git push
# now the changes are online and
```


![image](http://web.archive.org/web/20090210020404id_/http://whygitisbetterthanx.com/images/index1.png)

### Working together
```
git checkout dev                                # go into the right branch
[.. work on some files...]                      # do normal work
add newfile newfile2 newfile3                   # add the new and changed files
# now we have many changes in staging
commit -m "I made many new files which do X"    # create a new commit
# now we have a local commit
git pull                                        # fetch from upstream just in case
# now we have the same information that was online
git push
# now the changes are online and
```



## Using branches
```
git checkout dev                                # Go to dev
git checkout -b NewFancyFeature                 # Make new branch
[... work ...]                                  # Do some work
git add -u                                      # Add all changed files to staging
git commit -m "Completed new fancy feature."    # Make Commit
git checkout dev                                # Go to dev
git merge NewFancyFeature                       # Merge
git checkout master                             # go to master
git merge dev                                   # Merge dev into master for new release
```

![branching model](http://nvie.com/img/main-branches@2x.png)







## More links

Interactive and fun tutorial: https://try.github.io/

Good introduction in smart usage of branches: http://nvie.com/posts/a-successful-git-branching-model/


### Markdown helps
Gitlab has its own markdown format. More information can be found here: https://docs.gitlab.com/ee/user/markdown.html



































# Manual git, doing everything the manual way
```
mkdir gittutorial 
cd gittutorial
git init
touch README.md
git add README.md
git commit -m "initialized repro with README"
git checkout -b dev
git push --set-upstream origin dev
git status
```

### Fetching it from the internetz

Usually we would create a repro on GitHub or Gitlab and then start working in it:

```
git clone https://tbi-gitlab.dkfz.de/saary/gittutorial
cd gittutorial
git status
```

### Adding upstream

```
...
git remote add origin git@tbi-gitlab.dkfz.de:saary/gittutorial.git
git fetch
git push -u origin --all
git push -u origin --tags
```
or 
```
git remote add origin git@tbi-gitlab.dkfz.de:saary/gittutorial.git
git fetch
git branch --set-upstream-to=origin/dev dev
```


