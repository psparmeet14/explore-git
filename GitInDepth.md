# Git Basics

Comprehensive notes on Git fundamentals, setup, configuration, version control, undoing changes, and more — for quick reference and revision.

---

## 📦 Create a New Repository

**1. Create project folder**  
`mkdir gitProject`

**2. Open folder in VS Code**  
If you're in the parent directory:  
`code gitProject/`

If you're already inside the folder:  
`code .`

**3. Set up workspace**  
Place editor and terminal side-by-side for convenience.

**4. Create project files**  
```bash
cd gitProject  
touch index.html  
touch style.css
```

**5. Initialize a Git repository**  
`git init`

**6. Git folder not visible?**  
- Go to: Settings → top right `{}` icon  
- Add this in settings.json:
```json
"files.exclude": {
 "**/.git": false
}
```
- Restart VS Code if needed.

**7. Check Git status**  
`git status`

**8. Help with Git commands**  
`git init --help`

---

## ✅ Make First Commit

**1. Stage a file**  
`git add index.html`

**2. Commit staged changes**  
`git commit -m "Initial Commit"`

---

## ⚙️ Git Config (User Identity)

**Global config (applies to all repos):**  
```bash
git config --global user.name "John"  
git config --global user.email "workflow123test@gmail.com"
```
**Local config (for current repo only):**  
```bash
git config user.name "John"  
git config user.email "workflow123test@gmail.com"
```
---

## 🔄 Unstaging & Discarding Changes

**Unstage file from staging area:**  
```bash
git restore --staged index.html
```

**Discard changes in working directory:**  
```bash
git restore index.html
```

**Alternate unstage (safe to test):**  
```bash
git reset HEAD index.html
```
---

## 🕓 Viewing Commit History

**View full history:**  
`git log`

**Compact view (one-liners):**  
`git log --oneline`

**Visual history with branches:**  
`git log --graph --all --decorate`

---

## 📝 More About Commits

**Commit using editor (instead of `-m`):**  
`git commit`

**View global Git config file:**  
`code ~/.gitconfig`

---

## ♻️ Undoing Things

### What is HEAD?

- `HEAD` is a pointer. By default, HEAD points to the last commit.
- Check HEAD and previous commits using:  
  - `git show HEAD`  
  - `git show <commit-id>`  
  - `git show HEAD~1` (second last commit)

---

## 📂 Git Checkout (Undo, Inspect, Time Travel)

**Discard file changes (unstaged area):**  
```bash
git checkout script.js  
git checkout -- script.js  
git restore script.js
```

**Discard all changes:**  
```bash
git checkout *  
git checkout .
```

**View old project states (read-only mode):**  
```bash
git checkout master  
git checkout <commit-id> (detached HEAD)
```
---

## 🧼 Git Revert & Reset

### Git Revert (safe)
Reverts a commit by applying a new "undo" commit:  
`git revert <commit-id>`

### Git Reset (unsafe — deletes history)

**Mixed (default):**  
```bash
git reset --mixed <commit-id>  
# Removes commits and keeps changes unstaged.
```

**Soft:**  
```bash
git reset --soft <commit-id>  
# Removes commits and keeps changes staged.
```

To unstage after soft reset:  
`git reset .`

**Hard:**  
```bash
git reset --hard <commit-id>  
# Removes commits and deletes working directory changes.
```
---

## 🚫 Ignoring Files in Git

**Why?**  
To avoid tracking generated or unnecessary files (e.g., logs, compiled files, builds, binaries).

**Steps to ignore files/folders:**  
1. Create `.gitignore` file  
2. Add file/folder patterns to ignore

**Examples:**  
```vbnet
/text-1.txt  
/text-2.txt  
auto-gen-files/*  
auto-gen-files/*.txt
```

**Remove cached files from history:**  
```bash
git rm -r --cached .
```

**Unstage everything:**  
```bash
git reset .
```

**Discard all working changes:**  
```bash
git checkout .
```
---

✍️ These notes are structured for clarity and quick recall during daily Git workflows. Use them to save time, reduce mistakes, and manage your version history confidently.
