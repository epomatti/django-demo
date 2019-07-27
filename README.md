# Django Demo

Getting started:

`python hellowrold.py`

## Git Flow

### Develop Branch

Create develop branch

```shell
git checkout -b develop
git push origin develop
git branch -a
```

### Feature Branch

Create branch from develop, stage and commit:

```shell
git checkout -b purepython develop
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

### Release Branch

Change, stage, commit, merge to master, tag, and push:
```shell
git checkout -b release-1.2
git commit -a -m "some change"
git checkout master
git merge --no-ff release-1.2
git tag -a 1.2 -m "new release 1.2"
git push --tags origin master
```

Merge to develop and delete release:

```shell
git checkout develop
git merge --no-ff release-1.2
git branch -d release-1.2
```

### Hotfix Branch

Create hotfix branch, bump version and fix the problem

```shell
git checkout -b hotfix-1.2.1 master
./bump-version.sh 1.2.1
git commit -a -m "Bumped version number to 1.2.1"
git commit -m "Fixed severe production problem"
```

Merge to master, tag and push (with tags)

```shell
git checkout master
git merge --no-ff hotfix-1.2.1
git tag -a 1.2.1
git push --tags origin master
```

Merge to develop and delete branch

```shell
git checkout develop
git merge --no-ff hotfix-1.2.1
git push --tags origin develop

git branch -d hotfix-1.2.1
```

## References

https://dfpp.readthedocs.io/en/latest/chapter_01.html

https://githowto.com/

https://danielkummer.github.io/git-flow-cheatsheet/
