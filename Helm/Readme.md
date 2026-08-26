<div align="center">

# ⎈ Helm — Complete Notes & Commands

### 🚀 Kubernetes Package Manager • Deploy • Upgrade • Rollback • Manage

<img src="https://img.shields.io/badge/Helm-0F1689?style=for-the-badge&logo=helm&logoColor=white"/>
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/DevOps-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"/>

### 🌱 Beginner → Advanced | Charts | Templates | Values | Releases | CI/CD

</div>

---

# 📚 Topics

- ⎈ What is Helm?
- ☸️ Helm & Kubernetes
- 🏗️ Helm Architecture
- 📦 Helm Charts
- 📁 Chart Structure
- 📝 `Chart.yaml`
- ⚙️ `values.yaml`
- 🧩 Templates
- 🔧 Template Functions
- 🔀 Conditionals
- 🔁 Loops
- 📋 Named Templates
- 📦 Chart Dependencies
- 🚀 Install Charts
- 🔄 Upgrade Charts
- ↩️ Rollback
- 📜 Releases
- 🌐 Helm Repositories
- 🔍 Helm Search
- 🧪 Helm Template & Lint
- 🔐 Secrets
- 🪝 Helm Hooks
- 📦 Package & Push
- 🔄 Helm + CI/CD
- ☁️ Helm + Cloud
- 🛠️ Troubleshooting
- 🏆 Best Practices
- 🎯 Interview Questions

---

# ⎈ What is Helm?

Helm is a package manager for Kubernetes.

Instead of manually maintaining many Kubernetes YAML files, Helm allows us to package Kubernetes resources into reusable **Charts**.

```text
Kubernetes YAML
      ↓
   Helm Chart
      ↓
   Helm Release
      ↓
☸️ Kubernetes Cluster
