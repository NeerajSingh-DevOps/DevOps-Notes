<div align="center">

# ☁️ Microsoft Azure

### 🚀 Complete Azure Cloud & DevOps Notes

**Beginner → Intermediate → Advanced → Production**

<br>

<img src="https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white"/>
<img src="https://img.shields.io/badge/Terraform-844FBA?style=for-the-badge&logo=terraform&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white"/>
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black"/>
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white"/>
<img src="https://img.shields.io/badge/CI%2FCD-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"/>

<br><br>

### ☁️ Learn • Build • Secure • Automate • Deploy • Monitor

</div>

---

# 📚 Table of Contents

- [☁️ About This Repository](#️-about-this-repository)
- [🌩️ What is Cloud Computing](#️-what-is-cloud-computing)
- [☁️ What is Microsoft Azure](#️-what-is-microsoft-azure)
- [🏗️ Azure Global Infrastructure](#️-azure-global-infrastructure)
- [🧱 Azure Architecture Hierarchy](#-azure-architecture-hierarchy)
- [📦 Resource Groups](#-resource-groups)
- [👤 Microsoft Entra ID](#-microsoft-entra-id)
- [🔐 Azure RBAC](#-azure-rbac)
- [🛡️ Azure Policy](#️-azure-policy)
- [🌐 Azure Networking](#-azure-networking)
- [🏠 Virtual Network](#-virtual-network)
- [📡 Subnets](#-subnets)
- [🛡️ Network Security Group](#️-network-security-group)
- [🛣️ Route Tables](#️-route-tables)
- [🌍 Public and Private IP](#-public-and-private-ip)
- [🚪 NAT Gateway](#-nat-gateway)
- [⚖️ Azure Load Balancer](#️-azure-load-balancer)
- [🌐 Application Gateway](#-application-gateway)
- [🛡️ Web Application Firewall](#️-web-application-firewall)
- [🚪 Azure Bastion](#-azure-bastion)
- [🔐 Private Endpoint](#-private-endpoint)
- [🌍 Azure DNS](#-azure-dns)
- [🔗 VNet Peering](#-vnet-peering)
- [🔒 VPN Gateway](#-vpn-gateway)
- [🚀 ExpressRoute](#-expressroute)
- [🖥️ Azure Virtual Machines](#️-azure-virtual-machines)
- [📈 Virtual Machine Scale Sets](#-virtual-machine-scale-sets)
- [📦 Azure App Service](#-azure-app-service)
- [⚡ Azure Functions](#-azure-functions)
- [💾 Azure Storage](#-azure-storage)
- [📦 Blob Storage](#-blob-storage)
- [📁 Azure Files](#-azure-files)
- [📨 Queue Storage](#-queue-storage)
- [📊 Table Storage](#-table-storage)
- [💽 Managed Disks](#-managed-disks)
- [🗄️ Azure Databases](#️-azure-databases)
- [🌎 Azure Cosmos DB](#-azure-cosmos-db)
- [📦 Azure Container Registry](#-azure-container-registry)
- [☸️ Azure Kubernetes Service](#️-azure-kubernetes-service)
- [🔐 Azure Key Vault](#-azure-key-vault)
- [🆔 Managed Identity](#-managed-identity)
- [🛡️ Defender for Cloud](#️-defender-for-cloud)
- [🔥 Azure Firewall](#-azure-firewall)
- [📊 Azure Monitor](#-azure-monitor)
- [📋 Log Analytics](#-log-analytics)
- [🚨 Azure Alerts](#-azure-alerts)
- [🔄 Backup & Disaster Recovery](#-backup--disaster-recovery)
- [💰 Azure Cost Management](#-azure-cost-management)
- [🔄 Azure DevOps](#-azure-devops)
- [🏗️ Terraform with Azure](#️-terraform-with-azure)
- [🧑‍💻 Azure CLI](#-azure-cli)
- [🏛️ Azure Resource Manager](#️-azure-resource-manager)
- [🏢 Azure Architecture](#-azure-architecture)
- [🔁 Complete Azure DevOps Workflow](#-complete-azure-devops-workflow)
- [🏆 Azure Best Practices](#-azure-best-practices)
- [🧪 Practical Projects](#-practical-projects)
- [🎯 Interview Topics](#-interview-topics)
- [🗺️ Azure Learning Roadmap](#️-azure-learning-roadmap)
- [📂 Repository Structure](#-repository-structure)
- [👨‍💻 About Me](#-about-me)
- [🤝 Let's Connect](#-lets-connect)

---

# ☁️ About This Repository

Welcome to my **Azure Cloud Notes** repository. 🚀

This repository is created to document my hands-on learning and practical understanding of **Microsoft Azure and Cloud Engineering**.

The notes cover Azure from **fundamentals to production-level concepts**, with a strong focus on:

- ☁️ Cloud Computing
- 🌐 Networking
- 🖥️ Compute
- 💾 Storage
- 🗄️ Databases
- 🔐 Identity & Security
- 📊 Monitoring
- 📦 Containers
- ☸️ Kubernetes
- 🔄 DevOps
- 🏗️ Terraform
- 💰 Cost Optimization
- 💾 Backup & Disaster Recovery

> 🎯 **Goal:** Learn Azure practically, build real infrastructure, automate it with Terraform, deploy applications using CI/CD, and understand production-ready cloud architecture.

---

# 🌩️ What is Cloud Computing?

Cloud Computing means using computing resources over the internet instead of maintaining physical infrastructure yourself.

### Major Cloud Service Models

```text
                    ☁️ CLOUD
                       │
          ┌────────────┼────────────┐
          ▼            ▼            ▼
         IaaS         PaaS         SaaS
          │            │            │
          ▼            ▼            ▼
         VM        App Service    Microsoft 365
       Network      Database      Web Apps
       Storage      Functions     Software
IaaS
Infrastructure as a Service.
Examples:
- Azure Virtual Machines
- Azure Virtual Network
- Managed Disks
You manage more of the infrastructure.
PaaS
Platform as a Service.
Examples:
- Azure App Service
- Azure SQL Database
- Azure Functions
Azure manages more infrastructure for you.
SaaS
Software as a Service.
Examples:
- Microsoft 365
- Outlook
- Teams
☁️ What is Microsoft Azure?
Microsoft Azure is Microsoft's cloud computing platform.
Azure provides services for:
☁️ Compute
🌐 Networking
💾 Storage
🗄️ Databases
🔐 Identity
🛡️ Security
📊 Monitoring
📦 Containers
☸️ Kubernetes
🔄 DevOps
🤖 AI
🏗️ Infrastructure as Code
🏗️ Azure Global Infrastructure
Azure infrastructure is organized into geographical locations.
Geography
    ↓
Region
    ↓
Availability Zone
    ↓
Datacenter
    ↓
Azure Resources
🌍 Region
A region is a geographical area containing Azure datacenters.
Examples:
Central India
South India
West Europe
East US
Southeast Asia
🏢 Availability Zone
Availability Zones provide physical separation within supported Azure regions.
                Azure Region
                     │
        ┌────────────┼────────────┐
        ▼            ▼            ▼
     Zone 1        Zone 2       Zone 3
        │            │            │
       VM-1         VM-2         VM-3
Benefits
- High Availability
- Fault Isolation
- Resilience
- Better application availability
🧱 Azure Architecture Hierarchy
Azure management hierarchy:
Management Group
       ↓
Subscription
       ↓
Resource Group
       ↓
Resources
Example:
Tenant
  │
  └── Management Group
        │
        └── Subscription
              │
              └── Resource Group
                    │
                    ├── VNet
                    ├── VM
                    ├── Storage
                    ├── NSG
                    └── Load Balancer
📦 Resource Groups
A Resource Group is a logical container for Azure resources.
Example:
rg-production
│
├── VNet
├── Subnets
├── NSG
├── VM
├── Public IP
├── Load Balancer
└── Storage Account
Environment-based structure
rg-dev
rg-test
rg-stage
rg-prod
Recommended Tags
Environment = Production
Owner       = DevOps
Application = FinanceApp
Department  = IT
CostCenter  = FIN001
👤 Microsoft Entra ID
Microsoft Entra ID provides identity and access management.
It manages:
- Users
- Groups
- Applications
- Service Principals
- Managed Identities
- Authentication
- Authorization
User
 ↓
Entra ID
 ↓
Authentication
 ↓
Authorization
 ↓
Azure Resource
🔐 Azure RBAC
RBAC = Role-Based Access Control.
It determines:
Who can do what on which resource?

Common Roles
