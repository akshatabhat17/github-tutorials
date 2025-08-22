# Git Commands Cheatsheet

A single reference file for essential Git commands.

---

```bash
# 🔹 Setup
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list

# 🔹 Create / Clone Repo
git init
git clone <repository_url>

# 🔹 Status / Stage / Commit
git status
git add <file>
git add .                      # stage all
git commit -m "Message"
git commit -am "Message"       # skip staging

# 🔹 Branching
git branch                     # list branches
git branch <branch>            # create branch
git checkout <branch>          # switch branch
git checkout -b <branch>       # create & switch
git switch <branch>            # switch (newer)
git switch -c <branch>         # create & switch
git merge <branch>             # merge branch

# 🔹 Remote
git remote add origin <url>
git remote -v
git push origin <branch>
git push --all
git pull origin <branch>
git fetch

# 🔹 Undo / Reset
git reset <file>               # unstage
git reset --soft HEAD~1        # undo commit keep staged
git reset --mixed HEAD~1       # undo commit unstaged
git reset --hard HEAD~1        # undo commit discard changes
git checkout -- <file>         # discard file changes
git revert <commit_id>         # revert commit

# 🔹 Stash
git stash
git stash list
git stash apply
git stash pop

# 🔹 Logs
git log
git log --oneline
git log --oneline --graph --all

# 🔹 Tags
git tag <tag_name>             # lightweight
git tag -a <tag> -m "Message"  # annotated
git push origin --tags

# 🔹 Diffs & Show
git diff                       # working vs staged
git diff --cached              # staged vs last commit
git show                       # details of commit
