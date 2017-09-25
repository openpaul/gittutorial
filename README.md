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
