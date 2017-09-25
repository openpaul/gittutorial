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

