# Git Tutorial

Git is a source control managment solution for multiple people.

## Branches, commits and pushing stuff

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

Whats the status of the git repository?


### Staging, index, commits




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


## More links

Interactive and fun tutorial: https://try.github.io/

Good introduction in smart usage of branches: http://nvie.com/posts/a-successful-git-branching-model/




### Markdown helps
Gitlab has its own markdown format. More information can be found here: https://docs.gitlab.com/ee/user/markdown.html

