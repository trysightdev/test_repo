# test_repo
## Create tag and push to remote
```
git tag 3.84
git push origin --tags
```
## Delete local tag and delete remote tag
```
git tag -d 3.84
git push origin --delete 3.84
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
## Delete branch locally and remotely
```
git branch -d test_branch
git push -d origin test_branch
```

## Revert one file
```
git checkout filename.txt
```
## Reset everything back to local head
```
git reset --hard HEAD
```

## Reset remote branch and local branch to previous commit
```
git push -f origin commit_id:branch_name
git reset --hard commit_id
```
```
git push -f origin 3c056fe9f71dd406c0b56bb54caa2b08c81c5a0c:develop
git reset --hard 3c056fe9f71dd406c0b56bb54caa2b08c81c5a0c
```

