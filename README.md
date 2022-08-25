# git-sandbox
branching, rebasing, merging, prs practice

## experiments with interactive rebase

- git rebase -i HEAD~3
- tilda (~) specifies x number of commits behind head
- also can provide specific SHA
- cannot enter when you have unstaged changes
- newest commit appears on bottom
- after interactive rebase, in all situations i get message
```
 ! [rejected]        pr2 -> pr2 (non-fast-forward)
error: failed to push some refs to 'https://github.com/jerry81/git-sandbox.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
- git pull just makes me merge and lose all my commit rewrite stuff
```
git push origin +branch
```
- the above works and is similar to force push.
```
git push origin branch --force-with-lease
```
- the abovepreserves new commits added by others
- force push only recommended for local branch
- branch may have force push protection