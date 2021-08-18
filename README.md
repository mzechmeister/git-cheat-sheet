# git-cheat-sheet

### undo file modification
```bash
git reset --hard        # resets all modifactions!
```

### branching

```bash
git branch testing      # create a branch   
git checkout testing    # switch the branch
# do stuff
git commit
git pull
git checkout master
git merge testing       # with master 
```



From some github doc (regarding new access rule):
```bash
xclip -selection clipboard < ~/.ssh/id_ed25519.pub

git remote set-url origin git@github.com:mzechmeister/serval
git push
```

See also
* https://docs.gitlab.com/ee/topics/git/numerous_undo_possibilities_in_git
