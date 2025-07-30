# 🧠 How Git Works — From Beginner to Advanced

Git is a **distributed version control system** that helps track changes in code and collaborate with others efficiently.

---

## 📦 Initialize & Clone

| Command                | Description               |
| ---------------------- | ------------------------- |
| `git init`             | Initialize a new git repo |
| `git clone <repo-url>` | Clone a repo from remote  |

---

## 🔍 Status & Config

| Command                                            | Description                          |
| -------------------------------------------------- | ------------------------------------ |
| `git status`                                       | Show current state (staged/unstaged) |
| `git config --global user.name "Your Name"`        | Set global username                  |
| `git config --global user.email "you@example.com"` | Set global email                     |
| `git config --list`                                | View all current git configs         |

---

## ➕ Add & Commit

| Command                   | Description                          |
| ------------------------- | ------------------------------------ |
| `git add .`               | Stage all changes                    |
| `git add <file>`          | Stage a specific file                |
| `git commit -m "message"` | Commit staged changes                |
| `git commit -am "msg"`    | Add & commit tracked files in one go |

---

## 📤 Push & Pull

| Command                | Description                      |
| ---------------------- | -------------------------------- |
| `git push origin main` | Push commits to main branch      |
| `git pull origin main` | Pull latest changes from remote  |
| `git fetch`            | Download changes but don't merge |

---

## 🌿 Branching

| Command                  | Description                     |
| ------------------------ | ------------------------------- |
| `git branch`             | List branches                   |
| `git branch <name>`      | Create a new branch             |
| `git checkout <name>`    | Switch to branch                |
| `git checkout -b <name>` | Create and switch to new branch |
| `git merge <branch>`     | Merge a branch into current     |
| `git branch -d <name>`   | Delete a branch                 |

---

## 🔄 Undo & Reset

| Command               | Description                          |
| --------------------- | ------------------------------------ |
| `git restore <file>`  | Undo changes in working dir          |
| `git reset <file>`    | Unstage a file                       |
| `git reset --hard`    | Discard all uncommitted changes      |
| `git revert <commit>` | Revert a specific commit             |
| `git log`             | Show commit history                  |
| `git reflog`          | Show all HEAD history (even deleted) |

---

## 🔁 Rebase & Cherry-Pick

| Command                    | Description                               |
| -------------------------- | ----------------------------------------- |
| `git rebase main`          | Replay current branch over `main`         |
| `git cherry-pick <commit>` | Apply a specific commit on current branch |
| `git stash`                | Save uncommitted work temporarily         |
| `git stash pop`            | Restore stashed work                      |

---

## 🧠 Tagging

| Command                        | Description                |
| ------------------------------ | -------------------------- |
| `git tag`                      | List tags                  |
| `git tag v1.0`                 | Create lightweight tag     |
| `git tag -a v1.0 -m "release"` | Annotated tag with message |
| `git push origin --tags`       | Push tags to remote        |

---

## 🧪 Collaborator Commands

| Command                       | Description               |
| ----------------------------- | ------------------------- |
| `git remote -v`               | View connected remotes    |
| `git remote add origin <url>` | Add remote origin         |
| `git fetch origin`            | Fetch changes from remote |
| `git merge origin/main`       | Merge remote changes      |

---

## 🧯 Common Fixes

| Problem                                  | Command                                     |
| ---------------------------------------- | ------------------------------------------- |
| Merge conflict                           | Manually fix file then `git add .` & commit |
| Rejected push                            | `git pull origin main --rebase`             |
| Reset last commit (keep changes)         | `git reset --soft HEAD~1`                   |
| Remove file from repo (but keep locally) | `git rm --cached file.txt`                  |

---

## 🚀 GitHub Integration Tips

- Create `.gitignore` to exclude files from git
- Protect branches using GitHub settings
- Use Pull Requests for code review
- Use GitHub Actions for CI/CD

---

## ✅ Summary Git Workflow

```bash
git init
git add .
git commit -m "initial"
git branch -M main
git remote add origin <repo-url>
git push -u origin main
```
