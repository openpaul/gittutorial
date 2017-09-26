# Git Tutorial

![gitphdcomic](http://swcarpentry.github.io/git-novice/fig/phd101212s.png)

Git is a open source fast distributed version control system.
-----------------------------------

## Repository, branches, commits and pushing stuff around

```
mkdir repro
cd repro
git init
```
or
```
git clone https://url.de/repro
cd repro
```
-----------------------------------


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

The git workflow starts with files in the working directory. As
soon they are changed or created they can be added to the *staging* area. 
They are added via `git add FILE`.

A *commit* is a snapshot of all *staged* files bundled together to form a useful 
unit of change. It is created via `git commit -m "message"` after 
files are added to staging. `git commit -a -m "message"` will add all changes 
to the commit, this is usefull but migth not be what you want.

The *HEAD* (caps!) is the position we are in the git graph.

*head* (lowercase) refers to any one of the named heads in the repository (*branches*).

See here for more and better information: https://www.sbf5.com/~cduan/technical/git/


![image](https://git-scm.com/book/en/v2/images/areas.png)


-----------------------------------

## Changing files
[basic workflow](basicWorkflow.md)


-----------------------------------


# Links

Maybe the best explanation of git: https://www.sbf5.com/~cduan/technical/git/

Interactive and fun tutorial: https://try.github.io/

Good introduction in smart usage of branches: http://nvie.com/posts/a-successful-git-branching-model/


### Markdown helps to make documentation pretty
Gitlab has its own markdown format. More information can be found here: https://docs.gitlab.com/ee/user/markdown.html


































