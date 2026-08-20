# ☁️ AWS Cloud & DevOps Notes

<div align="center">

# 🚀 AWS Cloud Engineering — Complete Notes

### Learn → Build → Secure → Automate → Deploy → Monitor

<img src="https://img.shields.io/badge/AWS-Cloud-orange?style=for-the-badge&logo=amazonaws&logoColor=white" />
<img src="https://img.shields.io/badge/EC2-Compute-orange?style=for-the-badge&logo=amazonec2&logoColor=white" />
<img src="https://img.shields.io/badge/VPC-Networking-blue?style=for-the-badge&logo=amazonaws&logoColor=white" />
<img src="https://img.shields.io/badge/S3-Storage-green?style=for-the-badge&logo=amazons3&logoColor=white" />
<img src="https://img.shields.io/badge/IAM-Security-red?style=for-the-badge&logo=amazonaws&logoColor=white" />
<img src="https://img.shields.io/badge/Terraform-IaC-purple?style=for-the-badge&logo=terraform&logoColor=white" />

<br/>

**A structured AWS learning repository by [Neeraj Singh](https://github.com/NeerajSingh-DevOps)**

📚 Concepts • 🛠️ Hands-on Labs • 🏗️ Architecture • 🔐 Security • 🚀 DevOps

</div>

---

# 👋 About This Repository

Welcome to my **AWS Cloud & DevOps Notes** repository.

This repository documents my hands-on journey of learning and implementing **AWS Cloud, Networking, Security, Infrastructure as Code and DevOps practices**.

The goal is not just to memorize AWS services, but to understand:

> **Why a service is used → How it works → How services communicate → How to secure it → How to automate it → How to deploy it in a production-style environment.**

---

# 🎯 Learning Philosophy

```text
                    ☁️ AWS CLOUD
                         │
              ┌──────────┴──────────┐
              │                     │
          Fundamentals          Architecture
              │                     │
              ▼                     ▼
          Networking             Security
              │                     │
              └──────────┬──────────┘
                         ▼
                      Compute
                         │
                         ▼
                      Storage
                         │
                         ▼
                     Database
                         │
                         ▼
                    Monitoring
                         │
                         ▼
                    Containers
                         │
                         ▼
                      CI/CD
                         │
                         ▼
                    Terraform
                         │
                         ▼
                 🚀 DevOps Engineer
```

---

# 🗂️ AWS Learning Roadmap

| # | Area | Topics |
|---|---|---|
| 01 | ☁️ AWS Fundamentals | Cloud Computing, Regions, AZs, Pricing |
| 02 | 🔐 IAM | Users, Groups, Roles, Policies, MFA |
| 03 | 🖥️ EC2 | AMI, Instance Types, EBS, Key Pair |
| 04 | 🌐 VPC | CIDR, Subnets, Routes, IGW, NAT |
| 05 | 🔒 Security | SG, NACL, KMS, Encryption |
| 06 | 📦 S3 | Buckets, Objects, Versioning, Lifecycle |
| 07 | 🗄️ Database | RDS, DynamoDB |
| 08 | ⚖️ High Availability | ALB, Auto Scaling |
| 09 | 🌍 DNS | Route 53 |
| 10 | 📊 Monitoring | CloudWatch, CloudTrail |
| 11 | 🚨 Security Monitoring | GuardDuty |
| 12 | ⚡ Serverless | Lambda, API Gateway |
| 13 | 🐳 Containers | Docker, ECR, ECS |
| 14 | ☸️ Kubernetes | EKS |
| 15 | 🔄 DevOps | CI/CD |
| 16 | 🏗️ IaC | Terraform |
| 17 | 🚀 Projects | Real-world AWS architectures |

---

# 📚 Table of Contents

- [☁️ AWS Fundamentals](#️-aws-fundamentals)
- [🌍 AWS Global Infrastructure](#-aws-global-infrastructure)
- [🔐 IAM](#-iam)
- [🖥️ EC2](#️-ec2)
- [🌐 VPC](#-vpc)
- [📦 S3](#-s3)
- [🗄️ Databases](#️-databases)
- [🔒 Data Encryption](#-data-encryption)
- [🚨 GuardDuty](#-guardduty)
- [📊 CloudWatch](#-cloudwatch)
- [📝 CloudTrail](#-cloudtrail)
- [⚖️ Load Balancing](#️-load-balancing)
- [📈 Auto Scaling](#-auto-scaling)
- [🌍 Route 53](#-route-53)
- [⚡ Lambda](#-lambda)
- [🐳 ECR & ECS](#-ecr--ecs)
- [☸️ EKS](#️-eks)
- [🔄 CI/CD](#-cicd)
- [🏗️ Terraform with AWS](#️-terraform-with-aws)
- [🔐 AWS Security Architecture](#-aws-security-architecture)
- [🏢 Production Architecture](#-production-architecture)
- [🔄 Complete AWS DevOps Workflow](#-complete-aws-devops-workflow)
- [🧪 Hands-on Projects](#-hands-on-projects)
- [🎯 Interview Preparation](#-interview-preparation)

---

# ☁️ AWS Fundamentals

## What is AWS?

**Amazon Web Services (AWS)** is a cloud computing platform that provides on-demand infrastructure and managed services.

Instead of purchasing physical servers:

```text
Traditional IT
     │
     ├── Physical Servers
     ├── Storage
     ├── Networking
     ├── Data Center
     └── Maintenance
```

AWS provides:

```text
                ☁️ AWS
                  │
      ┌───────────┼───────────┐
      ▼           ▼           ▼
   Compute      Storage    Networking
      │           │           │
     EC2          S3          VPC
```

---

# 🌍 AWS Global Infrastructure

## Region

A Region is a geographical location containing multiple Availability Zones.

Example:

```text
AWS Region
│
├── Availability Zone A
├── Availability Zone B
└── Availability Zone C
```

## Availability Zone

An AZ is an isolated location within a Region.

Multiple AZs help achieve:

- High Availability
- Fault Tolerance
- Disaster Recovery

---

# 🔐 IAM — Identity & Access Management

IAM answers:

> **Who can access what?**

```text
                    IAM
                     │
       ┌─────────────┼─────────────┐
       ▼             ▼             ▼
     Users         Roles        Policies
       │             │             │
       └─────────────┼─────────────┘
                     ▼
                Permissions
```

## IAM Components

### 👤 User

Identity representing a person/application identity where appropriate.

### 👥 Group

Collection of users with common permissions.

### 🎭 Role

Temporary permissions that can be assumed by AWS services or identities.

Example:

```text
EC2
 │
 ▼
IAM Role
 │
 ▼
S3 Access
```

### 📜 Policy

JSON document defining permissions.

---

# 🔐 IAM Best Practices

- ✅ Least privilege
- ✅ MFA
- ✅ IAM Roles
- ❌ Avoid using root for daily operations
- ❌ Don't hardcode credentials
- ✅ Review permissions regularly

---

# 🖥️ EC2 — Elastic Compute Cloud

> **EC2 = Virtual Server in AWS**

```text
Developer
   │
   ▼
AWS EC2
   │
   ├── CPU
   ├── RAM
   ├── OS
   ├── Storage
   └── Network
```

## EC2 Components

```text
EC2
│
├── AMI
├── Instance Type
├── Key Pair
├── EBS
├── Security Group
├── VPC
├── Subnet
└── IP Address
```

---

# 💿 AMI

AMI = Amazon Machine Image.

Used to launch EC2 instances with a defined OS/software configuration.

Examples:

- Amazon Linux
- Ubuntu
- Windows Server

---

# ⚙️ Instance Type

Instance type determines:

- CPU
- Memory
- Network capability
- Instance family characteristics

Example:

```text
t3.micro
t3.small
t3.medium
```

---

# 🔑 EC2 Key Pair

Used for secure authentication.

Linux example:

```bash
ssh -i key.pem ec2-user@<public-ip>
```

---

# 🛡️ Security Group

Security Group acts as a virtual firewall for EC2 network traffic.

Example:

```text
Internet
    │
    ▼
Security Group
    │
    ▼
   EC2
```

Common ports:

| Port | Protocol | Purpose |
|---:|---|---|
| 22 | SSH | Linux |
| 80 | HTTP | Web |
| 443 | HTTPS | Secure Web |
| 3389 | RDP | Windows |

> ⚠️ Never expose unnecessary ports publicly.

---

# 💾 EBS

**Elastic Block Store** provides persistent block storage for EC2.

```text
EC2
 │
 ▼
EBS Volume
 │
 ▼
Application Data
```

---

# 🌐 VPC — Virtual Private Cloud

VPC is a logically isolated virtual network in AWS.

> **Think of VPC as your private network inside AWS.**

```text
                     VPC
                      │
          ┌───────────┴───────────┐
          │                       │
     Public Subnet          Private Subnet
          │                       │
       Load Balancer          Application
          │                       │
       NAT / EC2                  RDS
```

---

# 🧱 VPC Components

```text
VPC
│
├── CIDR
├── Subnets
├── Route Tables
├── Internet Gateway
├── NAT Gateway
├── Security Groups
├── Network ACL
├── VPC Endpoints
└── Elastic IP
```

---

# 📐 CIDR

Example VPC:

```text
10.0.0.0/16
```

Subnets:

```text
10.0.1.0/24
10.0.2.0/24
10.0.3.0/24
```

---

# 🌍 Public vs Private Subnet

## Public Subnet

Has a route to an Internet Gateway.

```text
Internet
   │
   ▼
IGW
   │
   ▼
Public Subnet
```

Typical resources:

- Load Balancer
- Bastion host where required
- Public-facing components

---

## 🔒 Private Subnet

No direct route to the Internet Gateway.

```text
Application
     │
     ▼
Private Subnet
     │
     ▼
Database
```

Typical resources:

- Application servers
- Containers
- Databases

---

# 🚪 Internet Gateway

Provides internet connectivity for resources that have appropriate public addressing and routing.

```text
VPC
 │
 ▼
Internet Gateway
 │
 ▼
Internet
```

---

# 🔄 NAT Gateway

Allows private subnet resources to initiate outbound Internet connections.

```text
Private EC2
    │
    ▼
NAT Gateway
    │
    ▼
Internet Gateway
    │
    ▼
Internet
```

---

# 🛣️ Route Table

Route tables determine where network traffic is directed.

Example:

```text
0.0.0.0/0 → Internet Gateway
```

Private subnet example:

```text
0.0.0.0/0 → NAT Gateway
```

---

# 🛡️ Security Group vs NACL

| Feature | Security Group | NACL |
|---|---|---|
| Level | Instance/ENI | Subnet |
| Stateful | ✅ | ❌ |
| Rules | Allow rules | Allow + Deny |
| Main purpose | Instance traffic control | Subnet traffic control |

---

# 📦 S3 — Simple Storage Service

S3 is AWS object storage.

Use cases:

- Documents
- Images
- Videos
- Backups
- Logs
- Static website assets
- Data lakes
- Terraform state

```text
S3
 │
 └── Bucket
      ├── Object
      ├── Object
      └── Object
```

---

# 🪣 S3 Bucket

Important concepts:

- Bucket
- Object
- Key
- Versioning
- Lifecycle
- Encryption
- Bucket Policy
- Block Public Access

---

# 🔄 S3 Versioning

```text
file.txt
│
├── Version 1
├── Version 2
└── Version 3
```

Useful for recovering from accidental overwrites/deletions.

---

# 🧹 S3 Lifecycle

Example:

```text
S3 Standard
     ↓
Infrequent Access
     ↓
Archive
     ↓
Delete
```

Lifecycle rules help automate storage management and cost optimization.

---

# 🗄️ AWS Databases

## RDS

Managed relational database service.

Supports engines such as:

- MySQL
- PostgreSQL
- MariaDB
- Oracle
- SQL Server

```text
Application
    │
    ▼
   RDS
    │
    ▼
Database
```

---

# ⚡ DynamoDB

Managed NoSQL database.

Suitable for:

- High-scale applications
- Low-latency workloads
- Serverless architectures

---

# 🔒 Data Encryption

Data exists in two important states:

```text
                 DATA
                  │
          ┌───────┴───────┐
          ▼               ▼
     At Rest          In Transit
          │               │
       Storage           Network
```

---

# 🔐 Encryption at Rest

Protects stored data.

Examples:

- S3
- EBS
- RDS
- EFS

---

# 🔐 Encryption in Transit

Protects data while moving between systems.

```text
Client
  │
  │ HTTPS / TLS
  ▼
Application
```

---

# 🔑 AWS KMS

**AWS Key Management Service** helps create and control cryptographic keys.

```text
Application
    │
    ▼
   KMS
    │
    ▼
Encryption Key
    │
    ▼
Encrypted Data
```

---

# 🚨 GuardDuty

**Amazon GuardDuty** is a threat detection service.

It continuously analyzes supported AWS activity and data sources to identify potential security threats.

```text
AWS Environment
      │
      ▼
  GuardDuty
      │
      ▼
Threat Detection
      │
      ▼
   Finding
      │
      ▼
Investigation
      │
      ▼
Response
```

### 🔍 GuardDuty can identify signals related to:

- Suspicious API activity
- Credential compromise
- Reconnaissance
- Malicious network behavior
- Potentially compromised resources
- Cryptocurrency-related activity

---

# 📊 CloudWatch

CloudWatch is used for monitoring and observability.

```text
EC2 / Application
       │
       ▼
  CloudWatch
       │
 ┌─────┼─────┐
 ▼     ▼     ▼
Metrics Logs Alarms
```

Example:

```text
CPU > 80%
    ↓
CloudWatch Alarm
    ↓
Notification / Automation
```

---

# 📝 CloudTrail

CloudTrail records AWS API activity.

```text
User
 │
 ▼
AWS API Call
 │
 ▼
CloudTrail
 │
 ▼
Audit Record
```

### CloudWatch vs CloudTrail

| Service | Purpose |
|---|---|
| CloudWatch | Monitoring, metrics and logs |
| CloudTrail | API activity and auditing |

---

# ⚖️ Load Balancing

Elastic Load Balancing distributes traffic across healthy targets.

```text
                 Users
                   │
                   ▼
              Load Balancer
              /     |     \
             ▼      ▼      ▼
           EC2     EC2     EC2
```

Benefits:

- High Availability
- Fault tolerance
- Traffic distribution
- Health checks
- Scalability

---

# 📈 Auto Scaling

Auto Scaling adjusts capacity according to workload and scaling policies.

```text
Traffic ↑
   │
   ▼
Auto Scaling
   │
   ▼
Instances ↑
```

When traffic decreases:

```text
Traffic ↓
   │
   ▼
Instances ↓
```

---

# 🌍 Route 53

Route 53 is AWS DNS service.

```text
www.example.com
       │
       ▼
   Route 53
       │
       ▼
Load Balancer
       │
       ▼
Application
```

Features include:

- DNS
- Health checks
- Routing policies
- Domain management

---

# ⚡ AWS Lambda

Serverless compute service.

```text
Event
  │
  ▼
Lambda
  │
  ▼
Code Execution
```

Possible event sources:

- S3
- API Gateway
- EventBridge
- SQS
- Scheduled events

---

# 🐳 ECR & ECS

## ECR

**Elastic Container Registry**

Stores container images.

```text
Developer
   │
   ▼
Docker Build
   │
   ▼
Docker Image
   │
   ▼
ECR
```

## ECS

**Elastic Container Service**

Runs containers.

```text
ECR
 │
 ▼
ECS
 │
 ▼
Container
 │
 ▼
Application
```

---

# ☸️ EKS

**Elastic Kubernetes Service** provides managed Kubernetes control plane capabilities.

```text
Developer
    │
    ▼
Kubernetes
    │
    ▼
   EKS
    │
    ▼
 Pods / Containers
```

---

# 🔄 CI/CD

A typical AWS DevOps pipeline:

```text
Developer
    │
    ▼
GitHub
    │
    ▼
CI Pipeline
    │
 ┌──┼─────────┐
 ▼  ▼         ▼
Build Test   Security Scan
    │
    ▼
Docker Image
    │
    ▼
ECR
    │
    ▼
ECS / EKS
    │
    ▼
Production
```

Possible tools:

- GitHub Actions
- Jenkins
- AWS CodeBuild
- AWS CodePipeline
- AWS CodeDeploy

---

# 🏗️ Terraform with AWS

Terraform allows AWS infrastructure to be defined as code.

```text
Terraform
    │
    ▼
AWS Provider
    │
    ├── VPC
    ├── Subnets
    ├── EC2
    ├── S3
    ├── ALB
    └── RDS
```

---

# 🔄 Terraform Workflow

```text
Write Code
    │
    ▼
terraform init
    │
    ▼
terraform fmt
    │
    ▼
terraform validate
    │
    ▼
terraform plan
    │
    ▼
terraform apply
    │
    ▼
AWS Infrastructure
```

---

# 🗂️ Recommended Terraform Structure

```text
terraform-aws-project/
│
├── provider.tf
├── versions.tf
├── main.tf
├── variables.tf
├── terraform.tfvars
├── outputs.tf
│
├── modules/
│   ├── vpc/
│   ├── ec2/
│   ├── s3/
│   └── alb/
│
└── README.md
```

---

# 🔐 Terraform Remote State

For collaborative environments, Terraform state should be stored remotely using an appropriate backend.

Example architecture:

```text
Developer
    │
    ▼
Terraform
    │
    ▼
Remote Backend
    │
    ▼
AWS Infrastructure
```

---

# 🔐 AWS Security Architecture

```text
                       ☁️ AWS
                         │
        ┌────────────────┼────────────────┐
        ▼                ▼                ▼
       IAM           CloudTrail       GuardDuty
        │                │                │
        ▼                ▼                ▼
   Permissions        Audit           Detection
        │                │                │
        └────────────────┼────────────────┘
                         ▼
                    Security Ops
```

---

# 🏢 Production Architecture

```text
                         🌍 Internet
                              │
                              ▼
                         Route 53
                              │
                              ▼
                    ┌─────────────────┐
                    │ Load Balancer   │
                    └────────┬────────┘
                             │
                 ┌───────────┴───────────┐
                 ▼                       ▼
           Availability Zone A      Availability Zone B
                 │                       │
                 ▼                       ▼
          Private App Tier          Private App Tier
                 │                       │
                 └───────────┬───────────┘
                             ▼
                       Database Tier
                             │
                             ▼
                            RDS

                    ┌─────────────────┐
                    │      S3         │
                    │ Files / Assets  │
                    └─────────────────┘
```

---

# 🔄 Complete AWS DevOps Workflow

```text
                    👨‍💻 Developer
                         │
                         ▼
                      GitHub
                         │
                         ▼
                    CI Pipeline
                         │
              ┌──────────┼──────────┐
              ▼          ▼          ▼
            Build       Test      Security
              │          │          │
              └──────────┼──────────┘
                         ▼
                     Docker
                         │
                         ▼
                       ECR
                         │
                         ▼
                    ECS / EKS
                         │
                         ▼
                   Load Balancer
                         │
                         ▼
                      Users
                         │
                         ▼
                    Monitoring
                         │
              ┌──────────┼──────────┐
              ▼          ▼          ▼
          CloudWatch  CloudTrail  GuardDuty
```

---

# 🔐 Secure Application Flow

```text
User
 │
 ▼
Route 53
 │
 ▼
HTTPS / TLS
 │
 ▼
Load Balancer
 │
 ▼
Private Application
 │
 ├──────────────► S3
 │
 └──────────────► RDS
                    │
                    ▼
                 Encrypted
                    │
                    ▼
                   KMS
```

---

# 🧪 Hands-on Projects

## 🚀 Project 01 — EC2 Web Server

```text
VPC
 ↓
Public Subnet
 ↓
Security Group
 ↓
EC2
 ↓
Nginx / Apache
 ↓
Internet
```

### Skills

`EC2` `VPC` `Security Groups` `Linux` `SSH`

---

## 🚀 Project 02 — Custom VPC

Build:

```text
VPC
├── Public Subnet
├── Private Subnet
├── Internet Gateway
├── NAT Gateway
├── Route Tables
├── Security Groups
└── NACL
```

---

## 🚀 Project 03 — Highly Available Application

```text
Route 53
    ↓
   ALB
  /   \
EC2   EC2
  \   /
   RDS
```

Skills:

`ALB` `EC2` `Auto Scaling` `RDS` `VPC`

---

## 🚀 Project 04 — Docker + AWS

```text
GitHub
  ↓
Docker Build
  ↓
ECR
  ↓
ECS
  ↓
ALB
  ↓
Application
```

---

## 🚀 Project 05 — Terraform AWS Infrastructure

```text
Terraform
    │
    ├── VPC
    ├── Public/Private Subnets
    ├── NAT
    ├── Security Groups
    ├── EC2
    ├── ALB
    └── S3
```

---

# 🎯 AWS Interview Preparation

Important questions to prepare:

### ☁️ AWS

- What is AWS?
- What is a Region?
- What is an Availability Zone?
- What is the shared responsibility model?

### 🖥️ EC2

- What is EC2?
- What is AMI?
- What are instance types?
- What is EBS?
- What is a Security Group?

### 🌐 VPC

- What is VPC?
- Public vs Private Subnet?
- What is CIDR?
- What is Internet Gateway?
- What is NAT Gateway?
- Security Group vs NACL?
- What is Route Table?

### 🔐 Security

- What is IAM?
- User vs Role?
- What is KMS?
- Encryption at Rest vs Transit?
- What is GuardDuty?
- What is CloudTrail?

### 📦 Storage

- What is S3?
- What is S3 Versioning?
- What is Lifecycle Policy?
- S3 vs EBS?

### 🚀 DevOps

- How do you deploy Docker containers to AWS?
- ECR vs ECS?
- ECS vs EKS?
- How would you design CI/CD?
- How would you provision AWS using Terraform?

---

# 🧠 AWS Quick Revision

| Service | Remember |
|---|---|
| 🖥️ EC2 | Compute |
| 📦 S3 | Object Storage |
| 💾 EBS | Block Storage |
| 🌐 VPC | Networking |
| 🔐 IAM | Identity & Access |
| 🔑 KMS | Encryption Keys |
| 🗄️ RDS | Relational Database |
| ⚡ DynamoDB | NoSQL |
| 🚪 IGW | Internet Connectivity |
| 🔄 NAT Gateway | Private → Internet |
| ⚖️ ALB | Load Balancing |
| 📈 Auto Scaling | Capacity Scaling |
| 🌍 Route 53 | DNS |
| 📊 CloudWatch | Monitoring |
| 📝 CloudTrail | API Auditing |
| 🚨 GuardDuty | Threat Detection |
| ⚡ Lambda | Serverless |
| 🐳 ECR | Container Registry |
| 🚢 ECS | Containers |
| ☸️ EKS | Kubernetes |
| 📬 SQS | Queue |
| 📢 SNS | Notifications |
| 🏗️ Terraform | Infrastructure as Code |

---

# 📈 AWS → DevOps Roadmap

```text
                     ☁️ AWS
                       │
                       ▼
                AWS Fundamentals
                       │
                       ▼
                      IAM
                       │
                       ▼
                     EC2
                       │
                       ▼
                      VPC
                       │
                       ▼
                  S3 + RDS
                       │
                       ▼
              Load Balancer
                       │
                       ▼
                 Auto Scaling
                       │
                       ▼
             CloudWatch + CloudTrail
                       │
                       ▼
              Security + GuardDuty
                       │
                       ▼
                     Docker
                       │
                       ▼
                    ECR/ECS
                       │
                       ▼
                     EKS
                       │
                       ▼
                    CI/CD
                       │
                       ▼
                  Terraform
                       │
                       ▼
              🚀 Cloud DevOps
```

---

# 🛠️ Tech Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=aws,azure,terraform,linux,git,github,githubactions,docker,kubernetes,bash" />

<br/><br/>

<img src="https://img.shields.io/badge/AWS-Cloud-orange?style=flat-square&logo=amazonaws&logoColor=white" />
<img src="https://img.shields.io/badge/Terraform-IaC-844FBA?style=flat-square&logo=terraform&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-Containers-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Kubernetes-Orchestration-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-Administration-FCC624?style=flat-square&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/Git-Version_Control-F05032?style=flat-square&logo=git&logoColor=white" />

</div>

---

# 📌 Repository Structure

```text
AWS-Notes/
│
├── README.md
│
├── 01-AWS-Fundamentals/
│   ├── AWS-Introduction.md
│   ├── Regions-and-AZ.md
│   └── Pricing.md
│
├── 02-IAM/
│   ├── IAM-Users.md
│   ├── IAM-Roles.md
│   └── IAM-Policies.md
│
├── 03-EC2/
│   ├── EC2-Basics.md
│   ├── AMI.md
│   ├── EBS.md
│   └── Security-Groups.md
│
├── 04-VPC/
│   ├── VPC.md
│   ├── Subnets.md
│   ├── Route-Tables.md
│   ├── Internet-Gateway.md
│   └── NAT-Gateway.md
│
├── 05-S3/
│   ├── S3-Basics.md
│   ├── Versioning.md
│   └── Lifecycle.md
│
├── 06-Security/
│   ├── KMS.md
│   ├── Encryption.md
│   ├── GuardDuty.md
│   └── CloudTrail.md
│
├── 07-Monitoring/
│   └── CloudWatch.md
│
├── 08-Load-Balancing/
│   └── ALB.md
│
├── 09-Database/
│   ├── RDS.md
│   └── DynamoDB.md
│
├── 10-Containers/
│   ├── ECR.md
│   ├── ECS.md
│   └── EKS.md
│
├── 11-CICD/
│   └── AWS-CICD.md
│
├── 12-Terraform/
│   ├── AWS-Terraform.md
│   ├── Modules.md
│   └── Remote-State.md
│
└── 13-Projects/
    ├── EC2-Web-Server/
    ├── Custom-VPC/
    ├── Highly-Available-App/
    └── Docker-ECS/
```

---

# 🏆 What I Am Building

This repository is focused on practical Cloud & DevOps engineering:

```text
📚 Learn
   ↓
🧠 Understand
   ↓
🛠️ Practice
   ↓
🏗️ Build
   ↓
🔐 Secure
   ↓
🔄 Automate
   ↓
🚀 Deploy
   ↓
📊 Monitor
   ↓
♻️ Improve
```

---

# 👨‍💻 About Me

**Neeraj Singh**

### Cloud & DevOps Engineer | Azure | AWS | Terraform | Linux | Docker | Kubernetes

I'm transitioning from a finance operations background into **Cloud & DevOps Engineering**, focusing on practical infrastructure, automation, networking, security and deployment.

My learning journey combines:

**Finance discipline + Infrastructure thinking + Automation + Cloud**

---

# 🤝 Let's Connect

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

### ☁️ Learn Cloud. Build Infrastructure. Automate Everything. 🚀

**⭐ If these notes help you, consider starring the repository!**

<br/>

<i>From reconciling numbers to engineering infrastructure — one cloud at a time. ☁️</i>

</div>
