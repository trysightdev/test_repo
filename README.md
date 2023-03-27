# test_repo
## Create tag and push to remote
```
git tag 3.84
git push --tags
```
## Create branch and change upstream (Only do once)
```
git clone https://github.com/trysightdev/test_repo
cd test_repo
git branch test_branch
git checkout test_branch
git push -u origin test_branch
```
## Merge branch (already checked out)
```
git checkout origin
git merge test_branch
git push
```
## Revert one file
```
git checkout filename.txt
```
## Reset everything back to local head
```
git reset --hard HEAD
```

