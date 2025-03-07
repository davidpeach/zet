# Fix the author details of all commits after a given commit hash

Tuesday, 12 November 2024. 15:56:35GMT

Id made some changes to a codebase locally where the global git config email was of a different email address.

I needed to fix the author details of all commits after the last correctly-authored commit.

Firstly need to fix the author config for the local repository.

```bash
git config --local user.email "you@your-email"
git config --local user.name "Your Name"
```

Now use `git log --oneline` to show your commits in reverse chronological order. Find the commit hash that is the last correcly-authored one.

Here is my actual output I was working with:

```bash
19665e9 (HEAD -> main, origin/main, origin/HEAD) Fix resolve.conf when setting up systemd networking on Arch Linux - created
ee587a3 Limiting host cpu usage from docker compose - updated
ef8f2c2 This is my zettelkasten
b1a29f7 run build after typo amend
```

The bottom one `b1a29f7` is correctly authored. The three recent ones above it are all authored by the machine default.

The following command will fix the author details for all commits _after_ the given commit hash.
Just make sure to swap out the hash in the example below for your own.

```
git rebase -i b1a29f7 -x "git commit --amend --reset-author -CHEAD"
```

You can then confirm the changes and force push back to the repo.

🔥DANGER 🔥: Beware force pushing to a repo that is accessed by others. In my case it was my own zettelkasten repo. So only me commiting to it.

