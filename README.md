# 📘 **Git Bash Practice**

This repository captures all Git and Git Bash commands practiced while building foundational skills in version control, branching strategies, merging workflows, stashing, resets, remote operations, and file handling.

This document now includes **all essential Git topics**, forming a complete learning reference.

---

# 📊 **Git Workflow Diagram (ASCII Visual)**

```
                          ┌───────────────────────────┐
                          │        Remote Repo        │
                          │         (GitHub)          │
                          └─────────────┬─────────────┘
                                        │
                                        │ git pull / git fetch
                                        ▼
 ┌──────────────────────────┐    ┌──────────────────────────┐
 │       Local Repo         │    │     Working Directory     │
 │     (Your computer)      │    │ (Your actual project)     │
 └─────────────┬────────────┘    └─────────────┬────────────┘
               │                                 │
               │ git checkout <branch>           │ Edit files
               ▼                                 ▼
        ┌──────────────┐                 ┌───────────────────┐
        │   Branches    │                 │ Modified Files     │
        │ main/dev/stg  │                 │ (Untracked/Changed)│
        └──────────────┘                 └───────────┬────────┘
                                                      │ git add
                                                      ▼
                                      ┌────────────────────────┐
                                      │      Staging Area      │
                                      │ (Files ready to commit)│
                                      └───────────┬────────────┘
                                                  │
                                                  │ git commit -m "msg"
                                                  ▼
                                      ┌────────────────────────┐
                                      │   Local Repository     │
                                      │  (Commits stored here) │
                                      └───────────┬────────────┘
                                                  │
                                                  │ git push origin <branch>
                                                  ▼
                           ┌─────────────────────────────┐
                           │         Remote Repo          │
                           │        (GitHub Server)       │
                           └──────────────────────────────┘
```

---

# 🔹 **1. Directory Navigation**

```bash
cd D:
cd Git\ Practice/
ls
pwd
```

---

# 🔹 **2. File Viewing & Editing**

```bash
cat file.txt
nl file.txt
notepad file.txt
cat >> file.txt        # Append text
```

---

# 🔹 **3. Branch Management**

```bash
git branch                 # List branches
git branch <name>          # Create a new branch
git checkout <branch>      # Switch branches
git branch -d <branch>     # Delete a branch
```

**Branches used:**
`main`, `development`, `staging`

---

# 🔹 **4. Staging & Committing**

```bash
git add .
git add *.txt
git add file.txt

git commit -m "Message"
```

---

# 🔹 **5. Diff & Commit Comparison**

```bash
git diff                        # Unstaged changes
git diff --staged               # Staged changes
git diff HEAD~1 HEAD            # Compare commits
git diff <commit1> <commit2>    
git diff main..development      # Compare branches
git show                        # Show commit details
```

---

# 🔹 **6. Merging Branches**

```bash
git merge <branch>
git merge <branch> -m "Message"
```

---

# 🔹 **7. Stash Operations**

```bash
git stash
git stash list
git stash pop
git stash apply
git stash drop
git stash pop stash@{0}
```

---

# 🔹 **8. Reset, Restore & Revert**

```bash
git reset                   # Unstage
git reset --staged
git reset --hard            # Remove all changes
git reset HEAD~             # Move HEAD back

git restore file.txt        # Restore file to last commit
git commit --amend          # Modify last commit message

git revert <commit>         # Undo commit safely
```

---

# 🔹 **9. Remote Repository Operations**

```bash
git clone <url>             # Clone a repository
git pull                    # Fetch + merge changes
git fetch                   # Fetch only
git push                    # Push commits
git push origin <branch>
git remote -v               # View remote URLs
git remote add origin <url>
```

---

# 🔹 **10. Logging & History**

```bash
git log
git log --oneline
git log --graph
git log --oneline --graph
history                     # Shell history
```

---

# 🔹 **11. Checking Out Old Commits**

```bash
git checkout <commit>
git checkout dcda870        # Example
```

---

# 🔹 **12. Using `.gitignore`**

```bash
touch .gitignore
echo "*.log" >> .gitignore
echo "node_modules/" >> .gitignore
```

---

# 🔹 **13. Tagging (Missing but Important)**

```bash
git tag v1.0
git tag -a v1.0 -m "Release version 1.0"
git push origin --tags
```

Used to mark release versions of your code.

---

# 🔹 **14. Cleaning Untracked Files**

```bash
git clean -f                # Remove untracked files
git clean -fd               # Remove untracked files + folders
```

---

# 🔹 **15. Git Configuration**

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```
