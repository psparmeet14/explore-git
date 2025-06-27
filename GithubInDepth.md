# The Basics of GitHub

## 1. Pushing an Existing Repository to GitHub

To push an existing local repository to GitHub:

- `git remote add origin https://github.com/your-username/your-repo.git`
- `git push origin master`

If you face authentication issues, try updating the remote URL:

- `git remote set-url origin https://yourusername@github.com/user/repo.git`

---

## 2. Pulling from GitHub to Local Repository

Basic pull:

- `git pull origin master`

Shorter setup for future pulls:

- `git branch --set-upstream-to=origin/master master`
- `git pull`

---

# Working with Branches

## 1. Create a New Branch

- `git branch feature-1`

## 2. List All Branches & Check Current Branch

- `git branch`

## 3. Switch to Another Branch

- `git checkout feature-1`

## 4. Create and Switch to a New Branch Immediately

- `git checkout -b feature-2`

## 5. Delete a Branch Locally

- `git branch -D feature-1`

---

# Branching on GitHub

## 1. Push a Local Feature Branch to GitHub

- `git push origin feature-2`  
(You can now see it on GitHub)

## 2. Create Branches on GitHub

Use the GitHub UI → **Branch dropdown** → **Create new branch**.

## 3. Pull Branch from GitHub to Local

- `git pull origin feature-1`
- `git checkout --track origin/feature-1`  
(This sets up tracking between local and remote branch)

## 4. Delete a Branch on GitHub

- Navigate to **Branches** tab → Click **delete icon** next to the branch.

## 5. Delete the Same Branch Locally

- `git push origin --delete feature-2`
- `git branch -D feature-1`
- `git branch -D feature-2`

---

# Merging on GitHub

## Pull Request & Merge on GitHub

You can initiate a pull request via GitHub’s interface and then perform the merge once approved.

---

# Merge Conflicts on GitHub

Conflicts may occur when changes to the same lines of code are made in different branches.

---

# Merge Branches Locally

## To Add File to Staging & Commit in One Step

- `git commit -am "your commit message"`  
(*Only works for modified and deleted files, not new files*)

---

## Merging to Master Branch from Feature Branch

### 1. Fast Forward Merge

- `git checkout master`
- `git merge <feature-branch-name>`

### 2. 3-Way Merge

Occurs when the branches have diverged and Git must combine changes manually.

### 3. Merge Conflict Resolution

- Abort the merge if needed:  
  `git merge --abort`

- If conflict markers (`<<<<`, `====`, `>>>>`) appear:
  - Manually choose the correct code
  - Then:
    - `git add .`
    - `git commit`

---

# Git Rebase

Rebasing re-applies commits from your current branch onto the tip of another branch (usually `master`).

1. Start on your **feature branch**
2. Ensure there are new commits on `master`
3. Rebase your branch onto the latest `master`

- `git checkout feature`
- `git rebase master`

This rewrites your branch’s history as if it started from the latest commit on `master`.

---

📌 _These notes are for personal reference to help understand and work effectively with Git and GitHub._
