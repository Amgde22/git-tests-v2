# changing commits

# amend
git commit --amend :replaces last commit with what you are commiting now

[if someone else is working on this don't amend they might be basing their work on the commit you are deleting (previous)]


# rebase
git rebase -i --root
  to start from root

git rebase -i head~n
  n: number of commits to go back

* commits are lines
change line order => chnage commit order
delete line => delete commit

* change line message => change commit message but replace pick with edit
- this will take you to the commit in that point in time
- git commit --amend to edit confirm
    if you edit anything do a git add
- git rebase --continue to get on with the rebase

# reset
git reset HEAD^
git reset HEAD~n

go to the previous commit
head > points to prev commit
staging aria > reseted
filed > untouched

git reset HEAD^ --soft
head > points to prev commit
staging aria > not reset
filed > untouched

git reset HEAD^ --hard
head > points to prev commit
staging aria > not reset
filed > [touched]
exactly like they were in the point you reset to



