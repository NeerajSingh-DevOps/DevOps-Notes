Haan bhai 👍 Tumhare AWS README jaisa hi **Git + GitHub Notes** ke liye ek professional README hona chahiye—sirf commands ki list nahi, balki **Git fundamentals → branching → merge/rebase → GitHub → PR → Actions → security → real DevOps workflow** tak.

<div align="center">

# 🐙 Git & GitHub — Complete DevOps Notes

### Learn → Practice → Collaborate → Automate → Deploy 🚀

<img src="https://img.shields.io/badge/Git-Version_Control-F05032?style=for-the-badge&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub-Collaboration-181717?style=for-the-badge&logo=github&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub_Actions-CI%2FCD-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" />
<img src="https://img.shields.io/badge/DevOps-Workflow-2496ED?style=for-the-badge" />

<br/>

**Complete Git & GitHub learning repository by [Neeraj Singh](https://github.com/NeerajSingh-DevOps)**

📚 Concepts • 🛠️ Commands • 🌿 Branching • 🔀 Merging • 🔐 Security • 🚀 CI/CD

</div>

---

# 👋 About This Repository

Welcome to my **Git & GitHub DevOps Notes** repository.

This repository contains structured notes, commands, workflows, best practices and hands-on examples for learning **Git, GitHub and Git-based DevOps workflows**.

The objective is to understand Git beyond basic commands:

> **Understand → Practice → Collaborate → Review → Automate → Deploy**

---

# 🎯 What You'll Learn

```text
                    🐙 Git
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
     Fundamentals             Repository
          │                       │
          ▼                       ▼
      Branching               GitHub
          │                       │
          ▼                       ▼
      Merge/Rebase          Pull Requests
          │                       │
          └───────────┬───────────┘
                      ▼
                    CI/CD
                      │
                      ▼
              GitHub Actions
                      │
                      ▼
               🚀 DevOps Workflow
```

---

# 📚 Table of Contents

- [🐙 Git vs GitHub](#-git-vs-github)
- [⚙️ Git Architecture](#️-git-architecture)
- [🚀 Git Installation](#-git-installation)
- [📁 Git Repository](#-git-repository)
- [🔄 Git Workflow](#-git-workflow)
- [📝 Basic Git Commands](#-basic-git-commands)
- [🌿 Branching](#-branching)
- [🔀 Merge](#-merge)
- [♻️ Rebase](#️-rebase)
- [🍒 Cherry Pick](#-cherry-pick)
- [↩️ Reset & Revert](#️-reset--revert)
- [📦 Stash](#-stash)
- [🐙 GitHub](#-github)
- [🔑 SSH Authentication](#-ssh-authentication)
- [🔀 Pull Requests](#-pull-requests)
- [👥 Collaboration Workflow](#-collaboration-workflow)
- [🛡️ Git Security](#️-git-security)
- [⚡ GitHub Actions](#-github-actions)
- [🚀 Git DevOps Workflow](#-git-devops-workflow)
- [🧪 Hands-on Projects](#-hands-on-projects)
- [🎯 Interview Questions](#-interview-questions)
- [📋 Quick Command Cheat Sheet](#-quick-command-cheat-sheet)

---

# 🐙 Git vs GitHub

## Git

**Git is a distributed version control system.**

It tracks changes in files and allows developers to collaborate safely.

```text
Developer
   ↓
Git
   ↓
Version History
```

## GitHub

**GitHub is a cloud-based platform for hosting Git repositories and collaboration.**

```text
Git
 ↓
GitHub
 ↓
Collaboration
 ↓
Pull Requests
 ↓
Code Review
 ↓
CI/CD
```

### Simple Difference

| Git | GitHub |
|---|---|
| Version Control System | Hosting & Collaboration Platform |
| Works locally | Cloud platform |
| Tracks changes | Hosts repositories |
| Branching | Pull Requests |
| Commit history | Code Review |
| Local repository | Remote repository |

> 💡 **Git = Tool**  
> 💡 **GitHub = Platform**

---

# ⚙️ Git Architecture

Git has three important areas:

```text
┌─────────────────┐
│ Working Directory│
└────────┬────────┘
         │ git add
         ▼
┌─────────────────┐
│ Staging Area     │
└────────┬────────┘
         │ git commit
         ▼
┌─────────────────┐
│ Local Repository │
└────────┬────────┘
         │ git push
         ▼
┌─────────────────┐
│ Remote GitHub    │
└─────────────────┘
```

---

# 🚀 Git Installation

Check Git:

```bash
git --version
```

Configure username:

```bash
git config --global user.name "Neeraj Singh"
```

Configure email:

```bash
git config --global user.email "your-email@example.com"
```

Check configuration:

```bash
git config --list
```

---

# 📁 Git Repository

Initialize repository:

```bash
git init
```

Check status:

```bash
git status
```

Git creates:

```text
.git/
```

The `.git` directory stores Git repository metadata.

---

# 🔄 Git Basic Workflow

```text
Create / Modify File
        ↓
   git status
        ↓
     git add
        ↓
   Staging Area
        ↓
   git commit
        ↓
 Local Repository
        ↓
    git push
        ↓
      GitHub
```

---

# 📝 Basic Git Commands

## Check Status

```bash
git status
```

## Add File

```bash
git add file.txt
```

## Add Everything

```bash
git add .
```

## Commit

```bash
git commit -m "Add project documentation"
```

## View History

```bash
git log
```

Compact history:

```bash
git log --oneline
```

---

# 🔗 Connect Local Repository to GitHub

Add remote:

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
```

Check remote:

```bash
git remote -v
```

Push:

```bash
git push -u origin main
```

---

# 📥 Clone Repository

Clone an existing repository:

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
```

Workflow:

```text
GitHub Repository
       ↓
   git clone
       ↓
Local Repository
       ↓
Modify
       ↓
Commit
       ↓
Push
```

---

# 📥 Git Pull

Fetch and integrate changes from remote:

```bash
git pull
```

Typical workflow:

```text
GitHub
  ↓
git pull
  ↓
Local Repository
  ↓
Modify
  ↓
Commit
  ↓
Push
```

---

# 📡 Git Fetch

Download remote changes without integrating them into your current branch:

```bash
git fetch
```

Difference:

```text
git fetch
→ Download remote changes

git pull
→ Fetch + integrate changes
```

---

# 🌿 Branching

Branching is one of Git's most important features.

```text
                 main
                  │
          ┌───────┴───────┐
          ▼               ▼
      feature-A       feature-B
```

Create branch:

```bash
git branch feature-login
```

Switch branch:

```bash
git switch feature-login
```

Create + switch:

```bash
git switch -c feature-login
```

List branches:

```bash
git branch
```

Delete branch:

```bash
git branch -d feature-login
```

---

# 🔀 Merge

Merge combines changes from one branch into another.

```text
main
 │
 ├───────●───────●
 │                \
 │                 ● feature
 │                /
 └───────●───────●
```

Example:

```bash
git switch main
git merge feature-login
```

---

# ⚠️ Merge Conflict

A conflict occurs when Git cannot automatically reconcile changes.

```text
Branch A
   │
   ├── change same line
   │
   ▼
   Conflict
   ▲
   │
   ├── change same line
   │
Branch B
```

Workflow:

```text
Conflict
   ↓
Open File
   ↓
Resolve Conflict
   ↓
git add .
   ↓
git commit
```

---

# ♻️ Rebase

Rebase moves or reapplies commits onto another base.

Example:

```text
Before:

main     A──B──C
              \
feature        D──E
```

After rebase:

```text
main     A──B──C
                  \
feature            D'──E'
```

Command:

```bash
git switch feature
git rebase main
```

### ⚠️ Important

Avoid rebasing shared/public history unless you understand the consequences.

---

# 🔀 Merge vs Rebase

| Merge | Rebase |
|---|---|
| Creates merge commit when needed | Rewrites commit ancestry |
| Preserves branch history | Produces linear-looking history |
| Safer for shared history | Requires more care |
| Common in collaborative workflows | Useful for local feature cleanup |

---

# 🍒 Cherry Pick

Apply a specific commit to another branch.

```bash
git cherry-pick <commit-id>
```

Example:

```text
main
 │
 A──B──C

feature
 │
 A──B──C──D
```

Cherry-pick `D`:

```text
main
 │
 A──B──C──D'
```

Useful when you need one particular change without merging an entire branch.

---

# ↩️ Git Reset

Reset moves the current branch pointer.

### Soft

```bash
git reset --soft HEAD~1
```

Keeps changes staged.

### Mixed

```bash
git reset HEAD~1
```

Keeps changes in working directory but unstaged.

### Hard

```bash
git reset --hard HEAD~1
```

⚠️ Can discard local changes.

---

# ↩️ Git Revert

Creates a new commit that reverses an earlier commit.

```bash
git revert <commit-id>
```

### Reset vs Revert

```text
reset
→ Rewrites/moves local history

revert
→ Creates a new commit that undoes a previous commit
```

For shared branches, `revert` is generally safer.

---

# 📦 Git Stash

Temporarily store uncommitted changes.

```bash
git stash
```

View stashes:

```bash
git stash list
```

Apply:

```bash
git stash apply
```

Apply and remove:

```bash
git stash pop
```

---

# 🐙 GitHub

GitHub provides:

- 📦 Repository hosting
- 🔀 Pull Requests
- 👀 Code Reviews
- 🐛 Issues
- 📋 Projects
- 🔐 Security features
- ⚡ GitHub Actions
- 📦 Packages
- 📊 Insights

---

# 🔑 SSH Authentication

SSH allows secure authentication with GitHub without repeatedly entering credentials.

Generate key:

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

Test:

```bash
ssh -T git@github.com
```

Use SSH remote:

```bash
git remote set-url origin git@github.com:USERNAME/REPOSITORY.git
```

---

# 🔀 Pull Requests

A Pull Request is a request to merge changes from one branch into another.

Typical workflow:

```text
Developer
   ↓
Feature Branch
   ↓
Commit
   ↓
Push
   ↓
Pull Request
   ↓
Code Review
   ↓
CI Checks
   ↓
Approval
   ↓
Merge
```

---

# 👥 GitHub Collaboration Workflow

Recommended team workflow:

```text
main
 │
 ├── feature/login
 │
 ├── feature/payment
 │
 └── bugfix/api
```

Developer:

```bash
git switch main
git pull

git switch -c feature/login

# Make changes

git add .
git commit -m "Add login functionality"

git push -u origin feature/login
```

Then:

```text
GitHub
  ↓
Pull Request
  ↓
Review
  ↓
CI/CD Checks
  ↓
Approval
  ↓
Merge
```

---

# 🌿 Recommended Branch Strategy

Simple workflow:

```text
main
 │
 ├── feature/*
 ├── bugfix/*
 └── hotfix/*
```

Example:

```text
main
 ├── feature/user-login
 ├── feature/payment-api
 ├── bugfix/login-error
 └── hotfix/production-issue
```

---

# 🔐 Git Security

Never commit:

```text
❌ Passwords
❌ API Keys
❌ Cloud Credentials
❌ Private Keys
❌ Tokens
❌ .env files
❌ Terraform sensitive state
```

Use `.gitignore`.

Example:

```gitignore
.env
*.pem
*.key
terraform.tfstate
terraform.tfstate.*
.terraform/
*.log
```

---

# 🚨 If Secret Is Accidentally Committed

Do not assume deleting it from the latest file removes it from Git history.

Recommended response:

```text
Secret exposed
     ↓
Rotate / Revoke Secret
     ↓
Investigate Usage
     ↓
Remove from Repository History if required
     ↓
Add Protection
     ↓
Use Secret Manager
```

For AWS workloads, use appropriate services such as:

- AWS Secrets Manager
- AWS Systems Manager Parameter Store
- IAM Roles

---

# ⚡ GitHub Actions

GitHub Actions provides CI/CD automation.

```text
GitHub
   ↓
Push / Pull Request
   ↓
GitHub Actions
   ↓
Build
   ↓
Test
   ↓
Security Scan
   ↓
Deploy
```

Example workflow structure:

```text
.github/
└── workflows/
    └── ci.yml
```

---

# 🔄 CI/CD Workflow

```text
Developer
    │
    ▼
Git Push
    │
    ▼
GitHub
    │
    ▼
GitHub Actions
    │
 ┌──┼────────────┐
 ▼  ▼            ▼
Build Test    Security
    │
    ▼
Artifact / Image
    │
    ▼
Deployment
    │
    ▼
☁️ Cloud
```

---

# 🐳 Git + Docker + AWS

A modern DevOps workflow:

```text
Developer
    ↓
Git
    ↓
GitHub
    ↓
GitHub Actions
    ↓
Docker Build
    ↓
Container Registry
    ↓
AWS ECS / EKS
    ↓
Application
```

---

# 🏗️ Git + Terraform + AWS

Infrastructure workflow:

```text
Developer
    ↓
Terraform Code
    ↓
GitHub
    ↓
Pull Request
    ↓
Code Review
    ↓
CI Validation
    ↓
terraform plan
    ↓
Approval
    ↓
terraform apply
    ↓
AWS Infrastructure
```

---

# 🚀 Complete DevOps Workflow

```text
                         👨‍💻 Developer
                              │
                              ▼
                         Local Git
                              │
                              ▼
                           Commit
                              │
                              ▼
                            Push
                              │
                              ▼
                           GitHub
                              │
                              ▼
                       Pull Request
                              │
                    ┌─────────┴─────────┐
                    ▼                   ▼
               Code Review         CI Pipeline
                                        │
                              ┌─────────┼─────────┐
                              ▼         ▼         ▼
                           Build      Test     Security
                              │         │         │
                              └─────────┼─────────┘
                                        ▼
                                    Artifact
                                        │
                                        ▼
                                  Deployment
                                        │
                                        ▼
                                  ☁️ AWS Cloud
                                        │
                                        ▼
                                   Monitoring
```

---

# 🧪 Hands-on Projects

## 🚀 Project 01 — Git Basics

Practice:

```text
git init
git add
git commit
git log
git status
git push
git pull
```

---

## 🚀 Project 02 — Branching & Merge

```text
main
 │
 ├── feature-A
 ├── feature-B
 └── bugfix
```

Practice:

- Branch creation
- Merge
- Conflict resolution
- Delete branches

---

## 🚀 Project 03 — Team Collaboration

Practice:

```text
Clone
 ↓
Branch
 ↓
Code
 ↓
Commit
 ↓
Push
 ↓
Pull Request
 ↓
Review
 ↓
Merge
```

---

## 🚀 Project 04 — GitHub Actions CI

```text
GitHub
 ↓
Push
 ↓
GitHub Actions
 ↓
Build
 ↓
Test
 ↓
Success / Failure
```

---

## 🚀 Project 05 — Terraform + GitHub Actions

```text
Terraform
    ↓
GitHub
    ↓
Pull Request
    ↓
Validation
    ↓
terraform plan
    ↓
Approval
    ↓
terraform apply
    ↓
AWS
```

---

# 🎯 Interview Questions

## 🐙 Git

- What is Git?
- Git vs GitHub?
- What is a repository?
- What is a commit?
- What is staging?
- What is HEAD?
- What is `.git`?
- What is `.gitignore`?

## 🌿 Branching

- What is a branch?
- Git merge vs rebase?
- What is merge conflict?
- How do you resolve a conflict?
- What is cherry-pick?

## ↩️ Undo Operations

- Git reset vs revert?
- Soft vs mixed vs hard reset?
- How do you undo a commit?
- How do you recover lost work?

## 🐙 GitHub

- What is a Pull Request?
- What is code review?
- What is fork?
- What is clone?
- What is GitHub Actions?
- How do you protect the main branch?

## 🔐 Security

- Why should secrets not be committed?
- What is `.gitignore`?
- What should you do if AWS credentials are pushed to GitHub?
- How should CI/CD access AWS securely?

---

# 📋 Git Command Cheat Sheet

| Purpose | Command |
|---|---|
| Version | `git --version` |
| Initialize | `git init` |
| Status | `git status` |
| Add file | `git add file` |
| Add all | `git add .` |
| Commit | `git commit -m "message"` |
| Log | `git log` |
| Short log | `git log --oneline` |
| Clone | `git clone <url>` |
| Remote | `git remote -v` |
| Add remote | `git remote add origin <url>` |
| Push | `git push` |
| Pull | `git pull` |
| Fetch | `git fetch` |
| Branch list | `git branch` |
| Create branch | `git branch name` |
| Switch | `git switch name` |
| Create + switch | `git switch -c name` |
| Merge | `git merge branch` |
| Rebase | `git rebase branch` |
| Cherry-pick | `git cherry-pick <commit>` |
| Stash | `git stash` |
| Stash pop | `git stash pop` |
| Revert | `git revert <commit>` |
| Reset | `git reset` |
| Tags | `git tag` |

---

# 🧠 Git Mental Model

Remember Git like this:

```text
                 🐙 GIT
                   │
        ┌──────────┴──────────┐
        ▼                     ▼
     LOCAL                  REMOTE
        │                     │
        ▼                     ▼
 Working Directory          GitHub
        │                     │
     git add                  │
        ▼                     │
    Staging Area              │
        │                     │
   git commit                 │
        ▼                     │
 Local Repository             │
        │                     │
      git push ───────────────┘
```

---

# 🏆 Git & GitHub Learning Path

```text
Git Basics
    ↓
Repository
    ↓
Commit
    ↓
Branch
    ↓
Merge
    ↓
Conflict Resolution
    ↓
Rebase
    ↓
Cherry Pick
    ↓
Reset / Revert
    ↓
GitHub
    ↓
Pull Requests
    ↓
Code Review
    ↓
GitHub Actions
    ↓
CI/CD
    ↓
Docker
    ↓
Terraform
    ↓
AWS
    ↓
🚀 DevOps Engineer
```

---

# 📁 Recommended Repository Structure

```text
Git-GitHub-Notes/
│
├── README.md
│
├── 01-Git-Basics/
│   ├── Git-Introduction.md
│   ├── Installation.md
│   └── Configuration.md
│
├── 02-Git-Workflow/
│   ├── Working-Directory.md
│   ├── Staging.md
│   └── Commit.md
│
├── 03-Branching/
│   ├── Branches.md
│   ├── Merge.md
│   ├── Rebase.md
│   └── Conflict-Resolution.md
│
├── 04-Git-Advanced/
│   ├── Reset.md
│   ├── Revert.md
│   ├── Stash.md
│   └── Cherry-Pick.md
│
├── 05-GitHub/
│   ├── Repository.md
│   ├── Clone.md
│   ├── Pull-Request.md
│   └── Code-Review.md
│
├── 06-Security/
│   ├── Gitignore.md
│   ├── Secrets.md
│   └── Best-Practices.md
│
├── 07-GitHub-Actions/
│   ├── CI.md
│   ├── CD.md
│   └── Workflows.md
│
├── 08-DevOps-Workflow/
│   └── Git-DevOps-Workflow.md
│
└── 09-Projects/
    ├── Git-Practice/
    ├── GitHub-Actions/
    └── Terraform-CI-CD/
```

---

# 👨‍💻 About Me

<div align="center">

### Neeraj Singh

**Cloud & DevOps Engineer | Azure | AWS | Terraform | Linux | Docker | Kubernetes**

I'm building my Cloud & DevOps engineering skills through hands-on projects, infrastructure automation and practical implementation.

My goal is to understand not only **how tools work**, but how they work together in a real-world **DevOps environment**.

</div>

---

# 🤝 Connect With Me

<div align="center">

<a href="https://github.com/NeerajSingh-DevOps">
<img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="https://www.linkedin.com/in/NeerajSingh-DevOps">
<img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

</div>

---

<div align="center">

### 🐙 Git → 🐙 GitHub → ⚡ CI/CD → 🐳 Docker → ☁️ AWS → 🏗️ Terraform

**Learn it. Practice it. Automate it. Build it. 🚀**

⭐ **If these notes help you, consider starring the repository!**

<br/>

<i>From version-controlling code to automating cloud infrastructure — building DevOps one commit at a time. 🚀</i>

</div>
