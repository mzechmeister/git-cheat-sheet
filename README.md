# git-cheat-sheet

### undo file modification
```bash
git reset --hard        # resets all modifactions!

```
### undo commit (not pushed)
```bash
git reset HEAD~
```

### undo last pushed commit
```bash
git log --oneline
git reset --hard HEAD^     # Use --hard if you don't care about keeping the changes you made
git push -f
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

### branch when already modified
```bash
git checkout -b testing
```

### staging
```bash
git stage filename
git pull
```


### new access rule
From [github doc](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).
Once for the whole account:
```bash
xclip -selection clipboard < ~/.ssh/id_ed25519.pub
```
In each repo:
```
git remote set-url origin git@github.com:mzechmeister/<reponame>
git push
```

See also
* https://docs.gitlab.com/ee/topics/git/numerous_undo_possibilities_in_git
