# Django Demo

Getting started:

`python hellowrold.py`

## Git Flow

Create develop branch: 

```shell
git checkout -b develop
git push origin develop
git branch -a
```

Perform code changes, stage and commit:

```shell
git add .
git status
git commit -m "first commit"
```

Merge:

```shell
git checkout develop
git merge --no-ff purepython
git push origin develop
git branch -d purepython
```

Change, stage, commit, merge to master, tag, and push:
```shell
git checkout -b release-1.2
git commit -a -m "some change"
git checkout master
git merge --no-ff release-1.2
git tag -a 1.2 -m "new release 1.2"
git push origin master
```

Merge to develop and delete release:

```shell
git checkout develop
git merge --no-ff release-1.2
git branch -d release-1.2
```

## References

https://dfpp.readthedocs.io/en/latest/chapter_01.html

https://githowto.com/

https://danielkummer.github.io/git-flow-cheatsheet/
