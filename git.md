# git

**Sync a fork of a repository to keep it up-to-date with the upstream repository.**:
```
git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
git fetch upstream
git checkout master
git merge upstream/master
```

**Selective add:**
```
git add -p
```

**Update selectively previous commit:**
```
git rebase -i HEAD~3
```

**Check logs:**
```
git log
git reflog
```

**Add/remove remote repos:**
```
git remote add NAME git://
git remote remove NAME https://
```
