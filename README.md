# GitHub useful commands

## 1. Adding new files.
```
git status
git add .
git commit -m 'added'
git push
```

## 2. Deleting a folder.
```
git status
git rm -r folder-name
git commit -m 'removed'
git push
```

## 3.1 Tagging submission.
```
git tag -a submission -m 'submission for hw'
git push --tags
```

### 3.2. Overwriting a tag.
```
git tag -a -f submission -m 'submission for hw' 
git push -f --tags
```
### 3.3 Deleting a tag
```
git tag -d tag-name
```

## 4.1 Dealing with branches
```
git branch
git checkout -b Abhinav7076      // create new branch
git checkout Abhinav7076      // change branch
mkdir workflows
touch ciworkflow.yaml           //create new file
```

### 4.2. Pushing in new branch
```
git checkout -b branch2  // creates a branch then add and commit
git push --set-upstream origin branch2
git checkout branch2
```

### 4.3. Create a new branch from a tag.
```
git checkout -b branch-name tag-name
```
### 4.4 Delete branch from remote 
```
git push origin --delete branch-name 
git branch -d branch-name // and then delete from remote 
```

## 5. if someone has changed the code then use pull command to copy and paste it in ur local repo
```
git pull
```

- if https(https://github.com/Abhinav7076/OS-Lab-Assignments.git) not working, try this by repacing https to git - git://github.com/Abhinav7076/OS-Lab-Assignments.git

## 6. Merging files.
```
git checkout master
git merge cs316pa4
git push
```

## 7. Uploading a folder.
```
git init 
git remote add origin https://github.com/Abhinav7076/Face_Recognition_Attendence.git
git remote -v
git add .
git commit -m 'kjasf'
git push --set-upstream origin master
```

## 8. Switch to commit id
```
git checkout commit-id
```

## 9. Stash
```
git stash : stashes means keeps it safely
git stash list : shows all stash entries
git stash show -p stash@{0} : show the changes of stack stash{0} = name of stash
git stash apply STASH-NAME applies the changes and leaves a copy in the stash
git stash pop STASH-NAME applies the changes and removes the files from the stash
git stash drop STASH-NAME : deletes the stash 
git stash clear : deletes all stash
```

## 11. Gitignore.
- simply write relative folder path or file name
- e.g. npm_mods/node_modules

## 12. create github personal token for working.
- Go To : Settings > Developer Tools > Personal Access Token > Generate New token

### 13.1 If you want to delete the file from the Git repository and the filesystem, use:
```
git rm file1.txt
git commit -m "remove file1.txt"
```
### 13.2 But if you want to remove the file only from the Git repository and not remove it from the filesystem, use:
```
git rm --cached file1.txt
git commit -m "remove file1.txt"
And to push changes to remote repo

git push origin branch_name
```

## 14. Cloning a particular commit
```
git checkout shakey (find from git log)
coming back to head
git reset --hard
```

## 15. See all the files in git repo (counterpart of LS) 
git ls-files

## 16. Remove last commit 
### Keep changes in your working directory(local) 
git reset --soft HEAD~1 
### Remove and discard changes
git reset --hard HEAD~1
### If commit has been pushed to remote repository 
git push origin -f

# Errors

## 1. git pull not working
```
git fetch --all 
git reset --hard origin/master
git pull
```

## 2. Please commit your changes or stash them before you switch branches. Aborting.
```
git reset --hard
git pull
```

## 3. Error : Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
- Solution : ```git push -f origin master```

## 4. you need to resolve your current index first
Solution : ```commit kardo fir checkout karo```

