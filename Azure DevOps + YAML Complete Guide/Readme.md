<div align="center">

# ☁️ Azure DevOps + YAML — Learning Notes & Practice Lab

**Hands-on notes, architecture diagrams aur ek working 3-stage Terraform pipeline**
*DevOps Insiders — Batch 18*

![Azure DevOps](https://img.shields.io/badge/Azure_DevOps-0078D7?style=for-the-badge&logo=azuredevops&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![YAML](https://img.shields.io/badge/YAML-CB171E?style=for-the-badge&logo=yaml&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft_Azure-0089D6?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

</div>

---

## 📌 Is Repo Mein Kya Hai

Ye repo meri Azure DevOps learning journey ka documentation hai — theory notes se lekar actually chalne wali pipeline tak. Har concept ko maine **pehle samjha, phir apne Azure environment mein banaya**, phir yahan document kiya.

| Section | Kya milega |
|---------|-----------|
| 📘 **Notes** | Azure DevOps architecture, hierarchy, agents ka complete breakdown |
| 🧩 **YAML Basics** | 4 core rules + pipeline hierarchy, beginner-friendly |
| 🏗️ **Terraform Lab** | Working infrastructure code with remote backend |
| ⚙️ **Pipelines** | 3-stage CI/CD pipeline (Validate → Plan → Apply) |
| 📄 **Cheat Sheet** | Print-ready PDF revision guide |

---

## 🧠 Azure DevOps — Quick Architecture

Azure DevOps ek **SaaS platform** hai jo pure SDLC ko ek chhat ke neeche laata hai. Pehle ye **TFS → VSTS** tha, 2019 mein rebrand hua.

```
Organization  (e.g. Vistara Technologies)
     │
   Project    (e.g. Vistara Sense)
     │
     ├── Azure Boards      →  JIRA / Rally ki jagah
     ├── Azure Repos       →  GitHub / BitBucket ki jagah
     ├── Azure Pipelines   →  Jenkins / TeamCity ki jagah
     ├── Azure Artifacts   →  Nexus / JFrog ki jagah
     ├── Azure Test Plans  →  JUnit / VSTest ki jagah
     └── Azure Wiki        →  Confluence ki jagah
```

> ⚠️ **Common confusion:** `dev.azure.com` (DevOps) aur `portal.azure.com` (Azure resources) do alag systems hain. Management Group → Subscription → Resource Group wali hierarchy sirf Azure Portal mein chalti hai, DevOps mein nahi.

---

## 🧩 Tool Mapping — Generic vs Azure vs AWS

| Kaam | Generic Tool | Azure | AWS |
|------|-------------|-------|-----|
| Project Management | JIRA, Rally | Azure Boards | CodeCatalyst |
| Source Control (SCM) | Git, GitLab, BitBucket | Azure Repos | CodeCommit |
| CI/CD Pipeline | Jenkins, TeamCity | Azure Pipelines | CodePipeline |
| Artifact Management | Nexus, JFrog | Azure Artifacts | CodeArtifact |
| Testing | JUnit, VSTest | Azure Test Plans | Device Farm |
| Documentation | Confluence | Azure Wiki | — |
| Infrastructure as Code | **Terraform** | ARM / Bicep | CloudFormation |

---

## ⚙️ Agents — Pipeline Kahan Chalti Hai

Pipeline sirf ek "robot" hai jo steps follow karta hai. Actual commands **Agent** pe chalti hain.

```
Git Repo  →  Pipeline  →  Agent  →  Azure Infrastructure
 (code)      (config)    (compute)      (resources)
```

| Agent Type | Kab use karein |
|-----------|----------------|
| **Microsoft Hosted** | Quick start, koi setup nahi, har run pe fresh machine |
| **Self Hosted** | Custom tools chahiye, cache bachana hai, network restrictions hain |

**Self-hosted agent setup:**
```
Project Settings → Agent Pools → New Agent
→ PAT token generate karo
→ config.cmd / ./config.sh run karo
→ Organization URL + PAT daalo
→ Status "Online" dikhna chahiye
```

---

## 📐 Pipeline Hierarchy

```
Stages
  └── Stage          (department — e.g. Validate)
       └── Jobs
            └── Job  (team ka kaam — ek agent pe)
                 └── Steps
                      └── Task / Script  (actual command)
```

---

## 🧾 YAML — 4 Rules Jo Kaafi Hain

<details>
<summary><b>1️⃣ key: value</b></summary>

```yaml
country: India
job: DevOps
```
Colon ke **baad space zaroori hai** — `key:value` galat, `key: value` sahi.
</details>

<details>
<summary><b>2️⃣ Indentation = Hierarchy</b></summary>

```yaml
person:
  name: Neeraj
  role: DevOps
```
Jo andar hai wo upar wali cheez ke andar hai.

> ⚠️ **TAB kabhi mat use karo** — sirf spaces (2 per level). Ye sabse common pipeline failure hai.
</details>

<details>
<summary><b>3️⃣ List ke liye hyphen</b></summary>

```yaml
tools:
  - Git
  - Docker
  - Terraform
```
Pipeline mein stages, jobs, steps — sab lists hain.
</details>

<details>
<summary><b>4️⃣ Data Types</b></summary>

```yaml
name: Neeraj        # string
replicas: 3         # number
enabled: true       # boolean (lowercase)
```
</details>

---

## 🚀 Practice Lab — 3-Stage Terraform Pipeline

### Repository Structure
```
.
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   └── backend.tf
├── pipelines/
│   └── azure-pipelines.yml
├── docs/
│   └── Azure-DevOps-YAML-Guide.pdf
└── README.md
```

### Pipeline Flow

```
FEATURE BRANCH                      MAIN BRANCH
     │                                   │
     ▼                                   ▼
┌─────────────┐                   ┌─────────────┐
│  VALIDATE   │                   │  VALIDATE   │
│ init · fmt  │                   │ init · fmt  │
│  validate   │                   │  validate   │
└──────┬──────┘                   └──────┬──────┘
       ▼                                 ▼
┌─────────────┐                   ┌─────────────┐
│    PLAN     │                   │    PLAN     │
│  az login   │                   │  az login   │
│    plan     │                   │    plan     │
└─────────────┘                   └──────┬──────┘
                                         ▼
       ⛔ ruk jata hai            ┌─────────────┐
                                  │ ⏸ APPROVAL  │
                                  └──────┬──────┘
                                         ▼
                                  ┌─────────────┐
                                  │   APPLY     │
                                  │   apply     │
                                  └─────────────┘
```

### Pipeline Skeleton

```yaml
trigger:
  - main

pool:
  vmImage: ubuntu-latest

stages:
  - stage: Validate
    jobs:
      - job: ValidateJob
        steps:
          - script: terraform init
          - script: terraform fmt -check
          - script: terraform validate
```

---

## 🔐 Terraform State — Best Practice

State file mein **credentials plain text mein** store hote hain. Isiliye ye kabhi Git pe push nahi hoti — **Azure Storage Account (blob container)** mein remote backend ke roop mein rakhte hain.

| Kyun | Faayda |
|------|--------|
| **Security** | RBAC se limited access |
| **Locking** | Do log ek saath apply nahi kar sakte |
| **Versioning** | Rollback possible |
| **Replication** | LRS / ZRS / GRS backup |
| **SLA** | 99.99% availability |

---

## 🌿 Git Workflow

```
feature branch → push → pipeline trigger → scan stage → plan stage
→ Pull Request → review + merge → manual approval → apply
```

**Scan stage** mein security/quality tools: `tfsec` · `checkov` · `terratest` · `tflint`

---

## 🗺️ Learning Roadmap

- [x] Azure DevOps architecture & hierarchy
- [x] Organization / Project / Repo setup
- [x] Microsoft Hosted vs Self Hosted agents
- [x] YAML fundamentals
- [x] 3-stage Terraform pipeline
- [ ] Service Connection (App Registration + OIDC)
- [ ] Variables & Variable Groups
- [ ] Parameters & conditional stages
- [ ] Secrets via Azure Key Vault
- [ ] Pipeline Templates (reusable)
- [ ] Approvals & Checks
- [ ] Parallel jobs & optimization

---

## 📄 Documentation

Complete revision guide (9 pages, print-ready) `docs/` folder mein available hai — architecture, org setup steps, YAML rules aur practice workflow ke saath.

---

<div align="center">

### 🤝 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/neerajsingh-devops)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/NeerajSingh-DevOps)

**Neeraj Singh** · Cloud & DevOps Engineer

⭐ Agar helpful laga to star zaroor karna!

</div>


