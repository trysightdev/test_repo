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

## Overwrite `develop` Branch with `main`

```bash
# Step 1: Switch to the develop branch
git checkout develop

# Step 2: Pull the latest changes from the main branch
git pull origin main

# Step 3: Reset the develop branch to match the main branch
git reset --hard origin/main

# Step 4: Force push the changes to the remote repository
git push origin develop --force

echo "Develop branch has been overwritten with the content of the main branch."
```
# 1. Create a backup branch with the current state
git checkout -b backup-main

# 2. Switch back to master
git checkout master

# 3. Revert all commits after 2b7ef015 but don't commit yet
git revert --no-commit 2b7ef015..HEAD

# 4. Commit the revert as a single commit
git commit -m "Revert codebase to state of commit 2b7ef015 while preserving history"

# 5. Push changes to origin
git push origin master
