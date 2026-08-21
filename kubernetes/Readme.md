<div align="center">

# ☸️ Kubernetes

## 🚀 Complete Kubernetes Notes

### Beginner → Intermediate → Advanced → Production

**Learn • Deploy • Scale • Secure • Troubleshoot • Automate 🔥**

<br>

<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white">
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white">
<img src="https://img.shields.io/badge/Helm-0F1689?style=for-the-badge&logo=helm&logoColor=white">
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black">
<img src="https://img.shields.io/badge/DevOps-Cloud-2088FF?style=for-the-badge">

</div>

---

# 📚 Table of Contents

- [☸️ What is Kubernetes?](#️-what-is-kubernetes)
- [🏗️ Kubernetes Architecture](#️-kubernetes-architecture)
- [🧠 Kubernetes Components](#-kubernetes-components)
- [📦 Containers & Pods](#-containers--pods)
- [🚀 Deployments](#-deployments)
- [🔄 ReplicaSets](#-replicasets)
- [🌐 Services](#-services)
- [🔀 Ingress](#-ingress)
- [⚙️ ConfigMap](#️-configmap)
- [🔐 Secrets](#-secrets)
- [💾 Storage](#-storage)
- [📊 StatefulSets](#-statefulsets)
- [⚡ DaemonSets](#-daemonsets)
- [⏰ Jobs & CronJobs](#-jobs--cronjobs)
- [🧭 Namespaces](#-namespaces)
- [🏷️ Labels & Selectors](#️-labels--selectors)
- [🩺 Health Checks](#-health-checks)
- [📈 Scaling](#-scaling)
- [🔐 Kubernetes Security](#-kubernetes-security)
- [🌐 Kubernetes Networking](#-kubernetes-networking)
- [📦 Helm](#-helm)
- [📝 YAML](#-yaml)
- [💻 kubectl Commands](#-kubectl-commands)
- [🔄 Rolling Updates & Rollbacks](#-rolling-updates--rollbacks)
- [🛠️ Troubleshooting](#️-troubleshooting)
- [🚀 Kubernetes Deployment Workflow](#-kubernetes-deployment-workflow)
- [☁️ Kubernetes on Cloud](#️-kubernetes-on-cloud)
- [🏆 Best Practices](#-best-practices)
- [🎯 Interview Topics](#-interview-topics)
- [🧪 Practice Projects](#-practice-projects)
- [🗺️ Learning Roadmap](#️-learning-roadmap)
- [👨‍💻 About Me](#-about-me)

---

# ☸️ What is Kubernetes?

**Kubernetes (K8s)** is an open-source container orchestration platform used to:

- 🚀 Deploy applications
- 🔄 Manage containers
- 📈 Scale applications
- 🔁 Perform rolling updates
- 🩺 Monitor application health
- 🌐 Provide networking
- 💾 Manage persistent storage
- 🔐 Manage application configuration and secrets
- 🤖 Automate container workloads

### Simple Architecture

```text
Developer
    │
    ▼
Docker Image
    │
    ▼
Container Registry
    │
    ▼
Kubernetes Cluster
    │
    ├── Pod
    ├── Service
    ├── Deployment
    ├── ConfigMap
    ├── Secret
    └── Ingress
