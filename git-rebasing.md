# Git rebasing

2025-04-03 12:37:41

Warning: Only rebase branches that are exclusively local.

1. git checkout staging
2. git pull (optional, to update staging)
3. git checkout feature
4. git rebase staging <--- This is the rebase command.
5. git checkout staging
6. git merge feature
