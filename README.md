# squash-all-commits
A script to squash all commits and replace master - useful if you want a clean start or to remove your personal email from github, for example find a commit and put .patch in the url to see the user's email.  

### Clone and run the script from the command line

Either:
```
git clone git@github.com:ryanwhocodes/squash-all-commits.git <CHOSEN_PATH>
```
Then:
```
cd GIT_REPO_FOLDER
<CHOSEN_PATH>/squash-all-commits/squash-all-commits.sh
```

### Copy and paste the script into your terminal

```
git checkout --orphan new-master
git add .
git commit -m "Clean commits"
git branch -m master old-master
git branch -m new-master master
git push --force --set-upstream origin master
git branch -D old-master
git push
```

### To change author info without squashing commits
- [Github changing author info](https://help.github.com/articles/changing-author-info/)
