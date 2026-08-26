```markdown
<div align="center">

# ☁️ Google Cloud Platform (GCP) — Complete Notes & Commands

### 🚀 Build • Deploy • Secure • Scale • Automate

<img src="https://img.shields.io/badge/GCP-Cloud-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white"/>
<img src="https://img.shields.io/badge/Compute_Engine-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white"/>
<img src="https://img.shields.io/badge/Kubernetes-GKE-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white"/>
<img src="https://img.shields.io/badge/Terraform-844FBA?style=for-the-badge&logo=terraform&logoColor=white"/>
<img src="https://img.shields.io/badge/DevOps-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"/>

### 🌱 Beginner → Advanced | GCP Services | CLI | Networking | Security | DevOps

</div>

---

# 📚 Topics

- ☁️ GCP Fundamentals
- 🏢 GCP Global Infrastructure
- 📁 Projects & Resources
- 📍 Regions & Zones
- 💻 Compute Engine
- 🖥️ VM Instances
- 🖼️ Machine Images
- 💾 Persistent Disks
- 🌐 VPC Networking
- 🔢 Subnets & IP Addresses
- 🛣️ Routes
- 🔥 Firewall Rules
- ⚖️ Load Balancing
- 🌍 Cloud DNS
- 📦 Cloud Storage
- 🗄️ Cloud SQL
- 🔐 IAM
- 👤 Service Accounts
- 🔑 Secret Manager
- 🔒 Cloud KMS
- ☸️ Google Kubernetes Engine
- ⚡ Cloud Run
- 🧩 Cloud Functions
- 📊 Cloud Monitoring
- 📝 Cloud Logging
- 🛡️ Security
- 🔄 CI/CD
- 🏗️ Terraform on GCP
- 🐳 Docker on GCP
- ☸️ Kubernetes on GCP
- 💰 Cost Management
- 🎯 Interview Questions

---

# ☁️ What is GCP?

Google Cloud Platform (GCP) is Google's cloud computing platform that provides infrastructure, networking, storage, databases, security, analytics, AI and DevOps services.

```text
Developer
    ↓
☁️ Google Cloud
    ↓
┌─────────────────────────────┐
│ Compute                     │
│ Networking                  │
│ Storage                     │
│ Database                    │
│ Security                    │
│ Kubernetes                  │
│ DevOps                      │
└─────────────────────────────┘
    ↓
🚀 Applications
```

---

# 🏢 GCP Global Infrastructure

GCP infrastructure is organized into:

```text
🌍 Global
   ↓
📍 Regions
   ↓
🏢 Zones
   ↓
🖥️ Resources
```

### Region

A geographical location containing multiple zones.

### Zone

An isolated location within a region where resources can run.

Example:

```text
Region
│
├── Zone A
├── Zone B
└── Zone C
```

---

# 📁 GCP Projects

Projects are the main organizational boundary for GCP resources.

```text
Organization
      ↓
   Folder
      ↓
   Project
      ↓
  Resources
```

Resources may include:

```text
VM
VPC
Bucket
Database
GKE Cluster
Load Balancer
```

---

# 🛠️ Google Cloud CLI

Install and authenticate:

```bash
gcloud auth login
```

Check account:

```bash
gcloud auth list
```

Set project:

```bash
gcloud config set project PROJECT_ID
```

Show configuration:

```bash
gcloud config list
```

---

# 📋 Useful gcloud Commands

```bash
gcloud projects list
gcloud compute instances list
gcloud compute networks list
gcloud compute firewall-rules list
gcloud storage buckets list
```

Get help:

```bash
gcloud help
gcloud compute --help
```

---

# 💻 Compute Engine

Compute Engine provides virtual machines in Google Cloud.

```text
User
 ↓
VPC
 ↓
Subnet
 ↓
Compute Engine VM
 ↓
Application
```

---

# 🖥️ Create VM

Example:

```bash
gcloud compute instances create my-vm \
  --zone=us-central1-a \
  --machine-type=e2-micro
```

List VMs:

```bash
gcloud compute instances list
```

Describe VM:

```bash
gcloud compute instances describe my-vm \
  --zone=us-central1-a
```

---

# ▶️ Start / Stop VM

```bash
gcloud compute instances start my-vm \
  --zone=us-central1-a
```

```bash
gcloud compute instances stop my-vm \
  --zone=us-central1-a
```

Reset VM:

```bash
gcloud compute instances reset my-vm \
  --zone=us-central1-a
```

Delete VM:

```bash
gcloud compute instances delete my-vm \
  --zone=us-central1-a
```

---

# 🔐 Connect to VM

SSH:

```bash
gcloud compute ssh my-vm \
  --zone=us-central1-a
```

For Windows/RDP environments, use the appropriate OS access mechanism and avoid exposing management ports unnecessarily.

---

# 💾 Persistent Disk

Persistent Disk provides durable block storage for Compute Engine.

Types include:

```text
Balanced
SSD
Standard
Extreme
```

Example:

```bash
gcloud compute disks list
```

Create disk:

```bash
gcloud compute disks create my-disk \
  --size=20GB \
  --zone=us-central1-a
```

---

# 🌐 VPC Networking

VPC = Virtual Private Cloud.

```text
☁️ VPC
│
├── Subnet
│
├── Routes
│
├── Firewall Rules
│
└── VM Instances
```

List VPCs:

```bash
gcloud compute networks list
```

---

# 🏗️ Create VPC

```bash
gcloud compute networks create my-vpc \
  --subnet-mode=custom
```

Create subnet:

```bash
gcloud compute networks subnets create my-subnet \
  --network=my-vpc \
  --region=us-central1 \
  --range=10.0.1.0/24
```

List subnets:

```bash
gcloud compute networks subnets list
```

---

# 🔢 IP Addressing

GCP supports:

```text
Private IP
Public IP
Static IP
Ephemeral IP
IPv4
IPv6
```

Check VM IPs:

```bash
gcloud compute instances list
```

---

# 🛣️ Routes

Routes determine where network traffic goes.

```text
Source
  ↓
Route
  ↓
Destination
```

List routes:

```bash
gcloud compute routes list
```

---

# 🔥 Firewall Rules

Firewall rules control network traffic to VM instances.

Example:

```bash
gcloud compute firewall-rules create allow-http \
  --network=my-vpc \
  --allow=tcp:80 \
  --source-ranges=0.0.0.0/0
```

List rules:

```bash
gcloud compute firewall-rules list
```

---

# ⚖️ Load Balancing

GCP provides different load-balancing capabilities for:

```text
HTTP(S)
TCP
UDP
Internal Applications
External Applications
```

Basic architecture:

```text
🌍 Internet
      ↓
⚖️ Load Balancer
      ↓
┌─────┼─────┐
↓     ↓     ↓
VM1   VM2   VM3
```

Benefits:

✅ High Availability

✅ Scalability

✅ Traffic Distribution

---

# 🌍 Cloud DNS

Cloud DNS is a scalable DNS service.

```text
Domain
  ↓
DNS
  ↓
Application IP
```

Common records:

```text
A
AAAA
CNAME
MX
TXT
```

---

# 📦 Cloud Storage

Cloud Storage is an object storage service.

```text
Bucket
│
├── file1
├── file2
├── image
└── backup
```

List buckets:

```bash
gcloud storage buckets list
```

Create bucket:

```bash
gcloud storage buckets create gs://MY-BUCKET
```

Upload:

```bash
gcloud storage cp file.txt gs://MY-BUCKET/
```

Download:

```bash
gcloud storage cp gs://MY-BUCKET/file.txt .
```

List objects:

```bash
gcloud storage ls gs://MY-BUCKET/
```

---

# 🔐 Cloud Storage Security

Protect buckets using:

```text
IAM
Uniform Bucket-Level Access
Encryption
Public Access Prevention
Versioning
Lifecycle Policies
Audit Logging
```

Avoid:

```text
❌ Public Bucket
❌ Anonymous Access
❌ Excessive IAM Permissions
```

---

# 🗄️ Cloud SQL

Cloud SQL provides managed relational databases.

Supported engines include:

```text
MySQL
PostgreSQL
SQL Server
```

Architecture:

```text
Application
     ↓
Private Network
     ↓
☁️ Cloud SQL
     ↓
Database
```

---

# 🔐 IAM

IAM controls:

```text
WHO
 ↓
CAN DO WHAT
 ↓
ON WHICH RESOURCE
```

Main components:

```text
Principal
Role
Permission
Policy
```

---

# 👤 IAM Roles

Common role types:

```text
Basic Roles
Predefined Roles
Custom Roles
```

Examples:

```text
Viewer
Editor
Owner
Compute Admin
Storage Admin
```

### Best Practice

```text
❌ Owner for everyone

✅ Least Privilege
```

---

# 🤖 Service Accounts

Service accounts provide identities for applications and workloads.

```text
Application
     ↓
Service Account
     ↓
IAM Role
     ↓
GCP Resource
```

List service accounts:

```bash
gcloud iam service-accounts list
```

---

# 🔑 Secret Manager

Never store secrets directly in:

```text
❌ GitHub
❌ Source Code
❌ Dockerfile
❌ Plain-text configuration
```

Use:

```text
🔐 Secret Manager
```

Typical flow:

```text
Application
     ↓
Service Account
     ↓
Secret Manager
     ↓
Secret
```

---

# 🔒 Cloud KMS

Cloud KMS manages cryptographic keys.

```text
Data
 ↓
🔐 Encryption Key
 ↓
Encrypted Data
```

Important concepts:

```text
Key Ring
Crypto Key
Key Version
Key Rotation
Access Control
```

---

# ☸️ Google Kubernetes Engine (GKE)

GKE is Google's managed Kubernetes service.

```text
Developer
    ↓
Docker Image
    ↓
Container Registry
    ↓
GKE Cluster
    ↓
Pods
    ↓
Application
```

---

# ☸️ GKE Architecture

```text
                 GKE Cluster
                     │
          ┌──────────┴──────────┐
          ↓                     ↓
     Control Plane            Nodes
                                │
                       ┌────────┼────────┐
                       ↓        ↓        ↓
                      Pod      Pod      Pod
                       │
                   Container
```

---

# 🚀 GKE Commands

Create cluster:

```bash
gcloud container clusters create my-cluster \
  --zone=us-central1-a \
  --num-nodes=2
```

Get credentials:

```bash
gcloud container clusters get-credentials my-cluster \
  --zone=us-central1-a
```

List clusters:

```bash
gcloud container clusters list
```

Delete:

```bash
gcloud container clusters delete my-cluster \
  --zone=us-central1-a
```

---

# ☸️ Kubernetes Commands

```bash
kubectl get nodes
kubectl get pods
kubectl get services
kubectl get deployments
kubectl get namespaces
```

Describe:

```bash
kubectl describe pod POD_NAME
```

Logs:

```bash
kubectl logs POD_NAME
```

Execute:

```bash
kubectl exec -it POD_NAME -- sh
```

---

# ⚡ Cloud Run

Cloud Run runs containerized applications without managing servers directly.

```text
Dockerfile
    ↓
Container Image
    ↓
Cloud Run
    ↓
🚀 Application
```

Deploy:

```bash
gcloud run deploy my-app \
  --image=IMAGE_URL \
  --region=us-central1
```

List services:

```bash
gcloud run services list
```

---

# 🧩 Cloud Functions

Cloud Functions provides event-driven serverless execution.

```text
Event
 ↓
Function
 ↓
Code Execution
 ↓
Response
```

Use cases:

```text
Automation
Events
API Logic
File Processing
Scheduled Tasks
```

---

# 📊 Cloud Monitoring

Cloud Monitoring provides:

```text
Metrics
Dashboards
Alerts
Uptime Monitoring
Performance Monitoring
```

Monitor:

```text
CPU
Memory
Disk
Network
Application
```

---

# 📝 Cloud Logging

Cloud Logging collects logs from cloud resources.

```text
VM Logs
Application Logs
Audit Logs
GKE Logs
Load Balancer Logs
```

Typical workflow:

```text
Application
    ↓
Logs
    ↓
Cloud Logging
    ↓
Alert / Investigation
```

---

# 🛡️ GCP Security

Important security services/features:

```text
IAM
Cloud KMS
Secret Manager
Security Command Center
Cloud Armor
VPC Firewall
Cloud Audit Logs
Organization Policies
```

Security principles:

```text
🔐 Least Privilege
🎯 Zero Trust
🌐 Network Segmentation
🔒 Encryption
📊 Monitoring
🚨 Detection
```

---

# 🛡️ Cloud Armor

Cloud Armor helps protect applications against:

```text
DDoS
Web Attacks
Malicious Requests
Application Layer Threats
```

Typical architecture:

```text
🌍 Internet
      ↓
🛡️ Cloud Armor
      ↓
⚖️ Load Balancer
      ↓
Application
```

---

# 🔄 CI/CD on GCP

Typical workflow:

```text
👨‍💻 Developer
      ↓
GitHub
      ↓
CI Pipeline
      ↓
🧪 Test
      ↓
🔍 Security Scan
      ↓
🐳 Docker Build
      ↓
📦 Container Registry
      ↓
☸️ GKE / Cloud Run
      ↓
🚀 Production
```

---

# 🐳 Docker + GCP

Build image:

```bash
docker build -t myapp:v1 .
```

Tag image:

```bash
docker tag myapp:v1 \
  REGION-docker.pkg.dev/PROJECT_ID/REPOSITORY/myapp:v1
```

Push:

```bash
docker push \
  REGION-docker.pkg.dev/PROJECT_ID/REPOSITORY/myapp:v1
```

---

# 📦 Artifact Registry

Artifact Registry stores:

```text
Docker Images
Packages
Build Artifacts
Dependencies
```

List repositories:

```bash
gcloud artifacts repositories list
```

---

# 🏗️ Terraform + GCP

Terraform can provision GCP infrastructure using the Google provider.

Example:

```hcl
terraform {
  required_providers {
    google = {
      source = "hashicorp/google"
    }
  }
}

provider "google" {
  project = var.project_id
  region  = var.region
}
```

---

# 🚀 Terraform Workflow

```text
Terraform Code
      ↓
terraform fmt
      ↓
terraform init
      ↓
terraform validate
      ↓
terraform plan
      ↓
terraform apply
      ↓
☁️ GCP Infrastructure
```

Commands:

```bash
terraform init
terraform fmt
terraform validate
terraform plan
terraform apply
terraform destroy
```

---

# 🔐 Terraform Security

Never commit:

```text
❌ Service Account Private Keys
❌ Passwords
❌ API Keys
❌ Secrets
❌ .tfstate with sensitive data
```

Use:

```text
Secret Manager
Environment Variables
Workload Identity
Remote Backend
IAM
```

---

# 💰 GCP Cost Management

Control cloud costs using:

```text
Budgets
Billing Alerts
Labels
Resource Monitoring
Rightsizing
Autoscaling
Lifecycle Policies
```

Best practices:

```text
✅ Delete unused VMs
✅ Remove unused disks
✅ Monitor storage growth
✅ Use appropriate machine types
✅ Set billing alerts
```

---

# 🔄 High Availability

A highly available architecture distributes workloads across zones.

```text
                🌍 Users
                   ↓
             ⚖️ Load Balancer
                   ↓
        ┌──────────┴──────────┐
        ↓                     ↓
     Zone A                Zone B
       VM                     VM
        ↓                     ↓
        └──────────┬──────────┘
                   ↓
                Database
```

---

# 🏗️ Production GCP Architecture

```text
                         🌍 INTERNET
                              │
                              ▼
                       🛡️ CLOUD ARMOR
                              │
                              ▼
                      ⚖️ LOAD BALANCER
                              │
                ┌─────────────┴─────────────┐
                ▼                           ▼
             WEB TIER                    WEB TIER
                │                           │
                └─────────────┬─────────────┘
                              ▼
                         APP / GKE
                              │
                              ▼
                         PRIVATE DB
                              │
                              ▼
                       📦 CLOUD STORAGE

        ┌─────────────────────────────────────┐
        │              SECURITY               │
        │ IAM │ KMS │ Secrets │ Firewall     │
        └─────────────────────────────────────┘

        ┌─────────────────────────────────────┐
        │            MONITORING               │
        │ Logging │ Monitoring │ Alerts       │
        └─────────────────────────────────────┘
```

---

# 🔄 Complete GCP DevOps Workflow

```text
👨‍💻 Developer
      ↓
💻 Code
      ↓
Git / GitHub
      ↓
🔄 CI/CD
      ↓
🧪 Testing
      ↓
🔍 Security Scan
      ↓
🐳 Docker Build
      ↓
📦 Artifact Registry
      ↓
🏗️ Terraform
      ↓
☁️ GCP Infrastructure
      ↓
☸️ GKE / Cloud Run
      ↓
⚖️ Load Balancer
      ↓
🚀 Production
      ↓
📊 Monitoring
      ↓
🚨 Alerts
      ↓
🔄 Continuous Improvement
```

---

# 🎯 GCP Interview Questions

## 🟢 Beginner

- What is GCP?
- What is a GCP Project?
- Region vs Zone?
- What is Compute Engine?
- What is VPC?
- What is Cloud Storage?
- What is IAM?
- What is a Service Account?
- What is Cloud SQL?
- What is GKE?

---

## 🟡 Intermediate

- What is a custom VPC?
- What is a subnet?
- How do GCP firewall rules work?
- How do you secure a VM?
- What is Cloud Load Balancing?
- What is Cloud Run?
- Cloud Run vs GKE?
- Cloud Storage vs Persistent Disk?
- IAM Role vs Permission?
- How do you secure Cloud Storage?

---

## 🔴 Advanced

- Design a highly available GCP architecture.
- How would you secure a production GCP environment?
- How do you implement least privilege?
- How would you secure GKE?
- How do you implement CI/CD on GCP?
- How do you manage secrets securely?
- How do you implement Terraform for GCP?
- How would you troubleshoot a VM with no internet connectivity?
- How would you investigate suspicious activity?
- How would you reduce GCP infrastructure cost?

---

# ⚡ Quick Revision

```text
gcloud auth login
        ↓
gcloud config set project
        ↓
gcloud compute instances list
        ↓
gcloud compute networks list
        ↓
gcloud compute firewall-rules list
        ↓
gcloud storage buckets list
        ↓
gcloud container clusters list
        ↓
gcloud artifacts repositories list
```

---

# 🧠 GCP Core Services

```text
💻 Compute Engine
☸️ GKE
⚡ Cloud Run
🧩 Cloud Functions
🌐 VPC
⚖️ Load Balancing
🌍 Cloud DNS
📦 Cloud Storage
🗄️ Cloud SQL
🔐 IAM
🔑 Secret Manager
🔒 Cloud KMS
🛡️ Cloud Armor
📊 Cloud Monitoring
📝 Cloud Logging
📦 Artifact Registry
🏗️ Terraform
```

---

# 🗺️ GCP Learning Roadmap

```text
☁️ GCP Fundamentals
        ↓
Projects / Regions / Zones
        ↓
Compute Engine
        ↓
VPC Networking
        ↓
Subnets / Routes / Firewall
        ↓
Cloud Storage
        ↓
IAM / Service Accounts
        ↓
Load Balancing
        ↓
Cloud SQL
        ↓
Security
        ↓
Docker
        ↓
GKE / Kubernetes
        ↓
Cloud Run
        ↓
Monitoring / Logging
        ↓
Terraform
        ↓
CI/CD
        ↓
🚀 GCP Cloud / DevOps Engineer
```

---

# 📌 GCP Security Checklist

### 👤 Identity

- [ ] MFA enabled
- [ ] Least privilege
- [ ] IAM roles reviewed
- [ ] Service accounts secured
- [ ] Unused accounts removed

### 🌐 Network

- [ ] Private subnets where appropriate
- [ ] Firewall rules restricted
- [ ] No unnecessary public IPs
- [ ] Secure management access
- [ ] Load Balancer + Cloud Armor where required

### 🔐 Data

- [ ] Encryption enabled
- [ ] KMS configured where required
- [ ] Secrets stored securely
- [ ] Storage access restricted
- [ ] Backup configured

### 📊 Monitoring

- [ ] Cloud Logging enabled
- [ ] Cloud Monitoring enabled
- [ ] Audit logs reviewed
- [ ] Alerts configured
- [ ] Security events monitored

---

# 🏆 GCP Best Practices

```text
🔐 Least Privilege
🌐 Secure Networking
🛡️ Defense in Depth
🔒 Encrypt Sensitive Data
🔑 Protect Secrets
📊 Monitor Resources
🚨 Configure Alerts
🏗️ Use Infrastructure as Code
🔄 Automate Deployments
💰 Monitor Costs
📋 Document Everything
```

---

# 👨‍💻 About Me

<div align="center">

## 👋 Hi, I'm Neeraj Singh

### ☁️ Cloud & DevOps Engineer | Azure | AWS | GCP | Terraform

I'm building hands-on expertise in **Cloud & DevOps Engineering**, focusing on cloud infrastructure, automation, networking, containerization, Kubernetes, CI/CD and cloud security.

My learning stack:

`Azure` • `AWS` • `GCP` • `Terraform` • `Linux` • `Git/GitHub` • `Docker` • `Kubernetes` • `CI/CD`

I use GitHub to document my learning, practical projects, commands and interview preparation.

---

### 🚀 Follow me for more Cloud & DevOps updates

<a href="https://github.com/NeerajSingh-DevOps">
<img src="https://img.shields.io/badge/GitHub-NeerajSingh--DevOps-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="https://www.linkedin.com/in/NeerajSingh-DevOps">
<img src="https://img.shields.io/badge/LinkedIn-NeerajSingh--DevOps-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

<a href="https://www.youtube.com/@NeerajSingh-DevOps">
<img src="https://img.shields.io/badge/YouTube-@NeerajSingh--DevOps-FF0000?style=for-the-badge&logo=youtube&logoColor=white"/>
</a>

<br><br>

⭐ **Star the repository if these notes help you!**

### ☁️ Learn • Build • Deploy • Secure • Automate 🚀

**— Neeraj Singh**

</div>
```
