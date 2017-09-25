# Git Tutorial

![gitphdcomic](http://swcarpentry.github.io/git-novice/fig/phd101212s.png)

Git is a source control managment solution for multiple people.

## Repository, branches, commits and pushing stuff around

```
git clone https://tbi-gitlab.dkfz.de/saary/gittutorial     # gitlab, github, ...
cd gittutorial                                             # ...
git status                                                 # see whats going on
git log                                                    # see the history
```

Whats the status of the git repository?


### Definitions

A git repository contains, among other things, the following:

- A set of commit objects.
- A set of references to commit objects, called heads.

TYhe git workflow starts with files in the working directory. As
soon they are changed or created can be added to the *staging* are. 
They need to be added via `git add FILE` but not are
part of a commit yet.

A *commit* is a snapshot of all *staged* files bundled together to form a useful 
unit of change. It is created via `git commit -a -m "message"` after 
files are added to staging.

The *HEAD* (caps!) is the position we are in the git graph.

*head* (lowercase) refers to any one of the named heads in the repository (*branches*).

See here for more and better information: https://www.sbf5.com/~cduan/technical/git/


![image](https://git-scm.com/book/en/v2/images/areas.png)


## Changing files


```
git checkout -b dev                             # create branch 'dev'
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
git branch                                      # see all branches
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







# Links

Maybe the best explanation of git: https://www.sbf5.com/~cduan/technical/git/

Interactive and fun tutorial: https://try.github.io/

Good introduction in smart usage of branches: http://nvie.com/posts/a-successful-git-branching-model/


### Markdown helps to make documentation pretty
Gitlab has its own markdown format. More information can be found here: https://docs.gitlab.com/ee/user/markdown.html


































