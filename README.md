# Explore Git

# Useful Git Commands

👉 [Basics of Terminal Commands](BasicsOfTerminal.md)\
👉 [Git In-Depth Notes](GitInDepth.md)

A handy list of commonly used Git commands with brief explanations.

---

## 1. `git status`
Displays the state of the working directory and the staging area.

---

## 2. `git pull`
Fetches from the remote repository and merges the changes with your local branch.

---

## 3. `git add .`
Stages **all** modified and new files for commit.

> 💡 Use to stage changes before committing.

---

## 4. `git restore --staged <file>`
Removes the specified file from the staging area.

---

## 5. `git restore <file>`
Discards local changes to the file and restores the last committed version.

---

## 6. `git commit -m "your commit message"`
Commits staged changes with a message.

---

## 7. `git reset --soft HEAD^`
Reverts the most recent commit and moves the changes back to the staging area.

> 💡 Use when you want to edit or fix your last commit before pushing.

---

## 8. `git push origin master`
Pushes the `master` branch to the remote repository.

---

## 9. `git log --oneline`
Shows commit history in a compact format – one commit per line.

---

## 10. `git log`
Displays the commit history with details like author, date, and message.

---

## 11. `git branch`
Lists all local branches.

> 💡 Use to check available branches.

---

## 12. `git branch <branchname>`
Creates a new local branch.

---

## 13. `git checkout <branchname>`
Switches to the specified branch.

---

## 14. `git checkout -b <branchname>`
Creates and checks out a new branch in one command.

---

## 15. `git branch -D <branchname>`
Deletes the specified local branch.

---

## 16. `git push origin <branchname>`
Pushes a local branch to the remote repository.

> 🔸 Requires the branch to exist locally first.

---

## 17. `git branch --set-upstream-to=origin/<branchname> <branchname>`
Links a local branch to track a remote branch.

---

## 18. `git merge <branchname>`
Merges the specified branch into your current branch.

---

## 19. `git remote -v`
Lists all remotes with their fetch and push URLs.

---

## 20. `git remote show origin`
Displays detailed information about the `origin` remote, including its tracked branches.

---

📘 _These notes are a part of my personal Git learning resources and are maintained on my GitHub for easy reference._

