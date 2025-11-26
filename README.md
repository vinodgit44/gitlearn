

# 📘 Git & GitHub Beginner Guide

*Learn Git step-by-step with icons, images, and easy commands.*

<div align="center">
  <img src="https://raw.githubusercontent.com/github/explore/main/topics/git/git.png" width="120" />
  <img src="https://raw.githubusercontent.com/github/explore/main/topics/github/github.png" width="120" />
</div>

---

## 🏷️ Badges

<p align="center">
  <img src="https://img.shields.io/badge/Git-Beginner%20Guide-orange?logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub-Mastery-black?logo=github" />
  <img src="https://img.shields.io/badge/License-MIT-green" />
</p>

---

# 📁 Table of Contents

1. [Install Git](#-1-install-git)
2. [Configure Git](#-2-configure-git-username--email)
3. [Generate SSH Key](#-3-generate-ssh-key-connect-pc-to-github)
4. [Add SSH Key to GitHub](#-4-add-ssh-key-to-github)
5. [Create GitHub Repo](#-5-create-a-github-repository)
6. [Initialize Local Repo](#-6-create-local-project-folder)
7. [Connect to GitHub](#-7-connect-local-repo-to-github-repo)
8. [Commit & Push](#-8-add-files--commit)
9. [Branching](#-10-create-a-new-branch)
10. [Pull, Merge, Delete](#-11-pull-latest-changes-from-github)
11. [Useful Commands](#-15-useful-git-commands)
12. [gitignore](#-16-example-gitignore-file)
13. [Push existing project](#-17-push-an-existing-project-folder-to-github)

---

# 🧰 **1. Install Git**

<div align="center">
  <img src="https://raw.githubusercontent.com/github/explore/main/topics/git/git.png" width="80" />
</div>

### Windows

Download Git:
👉 [https://git-scm.com/download/win](https://git-scm.com/download/win)

### Linux

```bash
sudo apt update
sudo apt install git -y
```

### Mac

```bash
brew install git
```



# 👤 **2. Configure Git (Username & Email)**

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Check configuration:

```bash
git config --list
```



# 🔐 **3. Generate SSH Key (Connect PC to GitHub)**

Generate key:

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

Start SSH agent:

```bash
eval "$(ssh-agent -s)"
```

Add private key:

```bash
ssh-add ~/.ssh/id_ed25519
```

Show public key:

```bash
cat ~/.ssh/id_ed25519.pub
```



# 🏦 **4. Add SSH Key to GitHub**

<div align="center">
  <img src="https://raw.githubusercontent.com/monkeyhippie/images/master/github-ssh-keys.png" width="600" />
</div>

1. Go to **GitHub → Settings → SSH and GPG Keys**
2. Click **New SSH Key**
3. Paste your public key
4. Save

Test SSH connection:

```bash
ssh -T git@github.com
```



# 📂 **5. Create a GitHub Repository**

<div align="center">
  <img src="https://raw.githubusercontent.com/monkeyhippie/images/master/github-new-repo.png" width="600" />
</div>

Steps:

1. Click **New Repository**
2. Enter repo name
3. Choose Public/Private
4. Create Repository

---

# 🖥️ **6. Create Local Project Folder**

```bash
mkdir myproject
cd myproject
```

# Customizing Default: 
For ease of use with github you can configure Git to use main (or any other name) as the default branch for new repositories you create locally.
This is done using the init.defaultBranch configuration setting. Now default branch would be main which matches with github.

```bash
git config --global init.defaultBranch main
```

Initialize Git:
```bash
git init
```



# 🔄 **7. Connect Local Repo to GitHub Repo**

Copy the **SSH URL** from your repo.

Example:

```bash
git remote add origin git@github.com:username/myproject.git
```

Check:

```bash
git remote -v
```



# 📌 **8. Add Files & Commit**

Add all files:

```bash
git add .
```

Commit:

```bash
git commit -m "Initial commit"
```



# 🚀 **9. Push Code to GitHub**

First push:

```bash
git branch -M main
git push -u origin main
```

Next pushes:

```bash
git push
```



# 🌱 **10. Create a New Branch**

```bash
git checkout -b feature-login
```

Switch back:

```bash
git checkout main
```


# 🔁 **11. Pull Latest Changes from GitHub**

```bash
git pull
```



# 🔄 **12. Merge Branch Into Main**

```bash
git checkout main
git merge feature-login
```



# 🧹 **13. Delete Branch**

Local:

```bash
git branch -d feature-login
```

Remote:

```bash
git push origin --delete feature-login
```



# 🔍 **15. Useful Git Commands**

| Action              | Command                         |
| ------------------- | ------------------------------- |
| Check status        | `git status`                    |
| View log            | `git log --oneline --graph`     |
| Compare changes     | `git diff`                      |
| Undo file           | `git restore filename`          |
| Remove from staging | `git restore --staged filename` |



# 📦 **16. Example `.gitignore`**

```bash
# Python
__pycache__/
*.pyc

# Node
node_modules/

# IDE
.vscode/
.idea/

# Environment
.env

# OS
.DS_Store
```

---

# 🧳 **17. Push an Existing Project to GitHub**

```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:username/repo.git
git push -u origin main
```



# 🎉 You're Ready!

You now know everything to start using **Git & GitHub professionally**:

✔ Install Git
✔ Configure user
✔ Generate SSH keys
✔ Create repos
✔ Push code
✔ Branching & merging
✔ Git best practices




