# ProgrammerLifeHacks

## Speed up youtube videos

1. Go to the video.
2. Press [[CTRL]] + [[SHIFT]] + [[J]] or [[COMMAND]] + [[OPTION]] + [[J]] to open the JavaScript Console.
3. Copy and paste the following (let speed be 3x):
```
document.getElementsByTagName("video")[0].playbackRate = 3
```
x equals the speed you want; you can have it very specific, f.e. 1,15312 still works
4. Press ENTER.
5. Close the Console with [[CTRL]] + [[SHIFT]] + [[J]] or [[COMMAND]] + [[SHIFT]] + [[C]].

## Find a particular open port and kill it 

### Windows:

Let's say it is port 3306 (SQL)
```
netstat -ano | findstr :3306
```
Note the PID xxxx
```
taskkill /pid xxxx /F
```

### Linux:

Let's say it is port 3306 (SQL)
```
netstat -tulnp | grep ":3306"
```
Note the PID xxxx
```
sudo kill -9 xxxx
```

## Git commands

### New repo:
```
git init
git add .
git commit -m "my first git commit."
git remote -v
git push origin master
```

### Push to repo:

```
git stash
git status
git pull
git stash apply
git diff
git add README.md
git commit -m "Commit message"
git push origin master
```

### Reverting Changes in a File: 

This command reverts the changes in `<file>` to match the last committed state of that file.

```
git checkout -- <file>
```

### Reverting a Commit:

Replace `<commit>` with the hash of the commit you want to revert. Git will create a new commit that effectively undoes the changes introduced by `<commit>`, leaving the original commit history intact.

```
git revert <commit>
```

### Resetting to a Previous Commit:

If you want to reset your repository to a previous commit, discarding all commits after that point

```
git reset --hard <commit>
```

This command resets the current branch to match the last commit. It's like going back in time to the state of your last commit.
```
git reset --hard HEAD
```

### Undoing a Git Pull:

If you pulled changes from a remote branch and want to undo those changes:
```
git reset --hard ORIG_HEAD
```

`ORIG_HEAD` is a reference to where the branch was before the last pull or merge. It helps you undo a pull operation by resetting your branch to its previous state.

### Git's conflict resolution tool:**

Configure:
```
git config --global merge.tool meld
```

Use mergetool (configured):
```
git mergetool
```

Use mergetool (not configured)
```
git mergetool -t meld
```
or
```
meld .
```

**Notes:**
* `git stash`: Stash local changes if any
* `git status`: Check the status of your working directory
* `git pull`: Fetch and integrate changes from the remote repository
* `git stash apply`: Reapply stashed changes if stashed earlier
* `git diff`: Review the changes you're about to commit
* `git revert`: undo changes in a way that preserves the commit history
* `git log`: displays a detailed log of the commit history of a repository


## Download YouTube video
```
pip install yt-dlp  
```
Use:
```
yt-dlp --verbose https://www.youtube.com/watch?v=[videoId]
```

