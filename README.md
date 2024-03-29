# git-cheat-sheet

### undo file modification
```bash
git reset --hard           # resets all modifactions!
git restore path/to/file   # a single file

```
### undo commit (not pushed)
```bash
git reset HEAD~     # modifications will be kept.
```

### undo last pushed commit
```bash
git log --oneline
git reset --hard HEAD^     # Use --hard if you don't care about keeping the changes you made
git push -f
```

### modify unpushed commit message
```bash
git commit --amend -m "New commit message"
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
This takes the modifications into the new branch (and main will have no modifications anymore).

### staging
```bash
git stage filename
git pull
```
`git restore --staged <file>`

### new access rule
```
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for
```

From [github doc](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).
Once for the whole account:
```bash
xclip -selection clipboard < ~/.ssh/id_ed25519.pub
```
In each repo:
```bash
git remote set-url origin git@github.com:mzechmeister/<reponame>
git push
```
Make sure ssh and not https is used.
(Create a token (https://github.com/settings/tokens) and provide the token as "password".)

See also
* https://docs.gitlab.com/ee/topics/git/numerous_undo_possibilities_in_git
