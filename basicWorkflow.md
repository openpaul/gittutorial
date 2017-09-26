# A basic workflow
## Adding files

```
git checkout -b dev                             # create branch 'dev'
[.. work on some files...]                      # do normal work
add newfile newfile2 newfile3                   # add the new and changed files
# now we have many changes in staging
```

## Make a new commit
```
commit -m "I made many new files which do X"    # create a new commit
# now we have a local commit
```
## Send this to the server
```
git push
# now the changes are online and
```


![image](http://web.archive.org/web/20090210020404id_/http://whygitisbetterthanx.com/images/index1.png)

# Working together
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

























