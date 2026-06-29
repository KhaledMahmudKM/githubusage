# Concise Book on Github Usage


<img src="cover_image.jpeg" alt="Cover Image" width="500" >

---

## 1. Introduction to Git and GitHub

### What is Git?

Git is a **distributed version control system** that helps you track changes in files over time. It allows you to:

* Keep a history of changes
* Revert to previous versions
* Work on different features simultaneously
* Collaborate with others without overwriting work

Git works locally on your machine and does not require an internet connection for most operations.

### What is GitHub?

GitHub is a **cloud-based hosting platform** for Git repositories. It adds collaboration features such as:

* Remote repositories
* Pull requests
* Issue tracking
* Code reviews
* Access control

In simple terms:

* **Git** = tool
* **GitHub** = service that hosts Git repositories

### Git vs GitHub

| Git             | GitHub                 |
| --------------- | ---------------------- |
| Runs locally    | Runs online            |
| Version control | Collaboration platform |
| CLI-focused     | Web + API + CLI        |

### Why Use Git from the Command Line?

* Full control over Git features
* Faster workflows
* Works on any system
* Essential for servers and DevOps

---

## 2. Installing and Configuring Git

### Installing Git

**Linux (Debian/Ubuntu):**

```bash
sudo apt update
sudo apt install git
```

**macOS (Homebrew):**

```bash
brew install git
```

**Windows:**
Download Git from the official website and install it with default options.

### Verifying Installation

```bash
git --version
```

### Initial Configuration

Git requires your identity for commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

### Setting Default Branch Name

```bash
git config --global init.defaultBranch main
```

### Viewing Configuration

```bash
git config --list
```

---

## 3. Creating and Cloning Repositories

### Initializing a New Repository

```bash
git init
```

This creates a hidden `.git` directory that stores all version control data.

### Creating a Repository on GitHub

* Log in to GitHub
* Click **New Repository**
* Do not initialize with README (for CLI-first workflow)

### Cloning an Existing Repository

```bash
git clone https://github.com/username/repository.git
```

### HTTPS vs SSH

* **HTTPS**: Easy, requires PAT
* **SSH**: More secure, no repeated authentication

---

## 4. Git File States and Workflow

### File States

* **Untracked** – new files
* **Modified** – changed files
* **Staged** – ready to commit
* **Committed** – saved in history

### Checking Repository Status

```bash
git status
```

### Typical Workflow

1. Edit files
2. Stage changes
3. Commit
4. Push to GitHub

---

## 5. Tracking Files – `git add`

### Adding Files

```bash
git add file.txt
```

### Adding All Files

```bash
git add .
```

### Interactive Add

```bash
git add -p
```

### Unstaging Files

```bash
git restore --staged file.txt
```

---

## 6. Saving Changes – `git commit`

### What is a Commit?

A commit is a **snapshot** of staged changes with a message describing what changed.

### Creating a Commit

```bash
git commit -m "Add initial project files"
```

### Writing Good Commit Messages

* Use present tense
* Be concise
* Describe *what* and *why*

### Viewing Commit History

```bash
git log
git log --oneline
```

### Amending a Commit

```bash
git commit --amend
```

---

## 7. Working with Remote Repositories

### Viewing Remotes

```bash
git remote -v
```

### Adding a Remote

```bash
git remote add origin https://github.com/username/repo.git
```

### Understanding origin

`origin` is the default name for the main remote repository.

---

## 8. Uploading Code – `git push`

### Pushing Changes

```bash
git push
```

### First Push with Upstream

```bash
git push -u origin main
```

### Force Push (Use with Caution)

```bash
git push --force
```

---

## 9. Downloading Updates – `git pull` and `git fetch`

### git pull

Fetches and merges changes.

```bash
git pull
```

### git fetch

Fetches changes without merging.

```bash
git fetch
```

---

## 10. Branching Basics

### Viewing Branches

```bash
git branch
```

### Creating a Branch

```bash
git branch feature-x
```

### Switching Branches

```bash
git switch feature-x
```

---

## 11. Merging Branches

### Merging a Branch

```bash
git merge feature-x
```

### Handling Conflicts

* Edit conflicting files
* Add resolved files
* Commit merge

---

## 12. Undoing Changes and Recovery

### Discard Local Changes

```bash
git restore file.txt
```

### Reset Commits

```bash
git reset --soft HEAD~1
git reset --hard HEAD~1
```

### Reverting a Commit

```bash
git revert <commit-hash>
```

### Using reflog

```bash
git reflog
```

---

## 13. Ignoring Files

### .gitignore Example

```
*.log
node_modules/
.env
```

### Ignoring Tracked Files

```bash
git rm --cached file.txt
```

---

## 14. Tagging and Releases

### Creating Tags

```bash
git tag v1.0.0
git push origin v1.0.0
```

---

## 15. GitHub Authentication

### SSH Key Generation

```bash
ssh-keygen -t ed25519
```

### Adding SSH Key to Agent

```bash
ssh-add ~/.ssh/id_ed25519
```

---

## 16. Collaboration Workflows

### Forking Workflow

* Fork repository
* Clone fork
* Add upstream
* Sync changes

```bash
git remote add upstream https://github.com/original/repo.git
```

---

## 17. Inspecting and Comparing Changes

### Viewing Differences

```bash
git diff
git diff --staged
```

---

## 18. Best Practices and Common Mistakes

* Commit often
* Pull before push
* Use branches
* Avoid force-push on shared branches

---

## 19. Git Command Cheat Sheet

* `git status`
* `git add .`
* `git commit -m`
* `git push`
* `git pull`
* `git branch`
* `git merge`

---






