# Useful Git Commands
## Sync a fork of a repository to keep it up-to-date with the upstream repository
refer [this](https://2buntu.com/articles/1459/keeping-your-forked-repo-synced-with-the-upstream-source/) and [this](https://stackoverflow.com/questions/7244321/how-do-i-update-a-github-forked-repository)
```
git remote -v
git remote add upstream https://github.com/ORIGINAL_AUTHOR/ORIGINAL_REPOSITORY
git remote -v
git fetch upstream
git checkout master
git rebase upstream/master
git push origin master
```

## Stop tracking a file
If you have any files that are tracked by git and you want to ignore them, so that your secret keys don't show up on Github.
```
git update-index --assume-unchanged file_name
```

## Undo the most recent commit
```bash
git commit -m "Something terribly misguided"
git reset HEAD~
<< edit files as necessary >>
git add ...
git commit -c ORIG_HEAD
```

## Recovering unstaged changes
See [this](https://stackoverflow.com/a/1109433)
```bash
git fsck --cache --no-reflogs --lost-found --unreachable  HEAD
```

or

```bash
git show -p --format=raw $blob > $blob.txt
```

## Update the fork
```bash
git checkout master
git fetch upstream
git pull upstream master
```

## Fast forward a branch to master
```bash
git checkout <branch_name>
git merge origin/master
```

## remove all unstaged changes
```bash
git checkout .
```
