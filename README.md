# Django Demo

Pure Python example now.

Just run `python hellowrold.py`


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

## References

https://dfpp.readthedocs.io/en/latest/chapter_01.html