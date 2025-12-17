# 🚀 DevOps CI/CD Project

An end-to-end **DevOps CI/CD pipeline** that demonstrates how to build, containerize, deploy, secure, and migrate an application from **on-premises (local)** to **AWS cloud**, using industry-standard DevOps tools and best practices.

---

## 📌 Project Overview

This project showcases a **real-world DevOps workflow**, starting from a local development environment and progressively evolving into a cloud-ready architecture.

The pipeline automates:

* Application build
* Docker image creation
* Infrastructure provisioning with Terraform
* Configuration management with Ansible
* Kubernetes deployment
* Security scanning
* Monitoring
* Cloud migration (AWS)

---

## 🧱 Architecture (High-Level)

```
Developer
   |
   |  (git push)
   v
GitHub
   |
   v
Jenkins CI/CD Pipeline
   |
   |-- Docker Build
   |-- Security Scan (Trivy)
   |-- Push Image (AWS ECR)
   |
   v
Kubernetes (Local → AWS EKS)
   |
   v
Application Service
```

---

## 🛠️ Tech Stack

| Category                 | Tools                   |
| ------------------------ | ----------------------- |
| CI/CD                    | Jenkins                 |
| Infrastructure as Code   | Terraform               |
| Configuration Management | Ansible                 |
| Containerization         | Docker                  |
| Orchestration            | Kubernetes (KIND → EKS) |
| Cloud                    | AWS (EC2, ECR, EKS)     |
| Monitoring               | Prometheus              |
| Security                 | Trivy                   |
| Application              | Node.js (Express)       |
| OS                       | Ubuntu / Amazon Linux 2 |

---

## 📂 Project Structure

```
DevOps-CI-CD-project/
├── app/
│   ├── index.js
│   ├── Dockerfile
│   ├── package.json
│
├── terraform/
│   ├── provider.tf
│   ├── main.tf
│
├── ansible/
│   ├── inventory
│   ├── playbook.yml
│
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│
├── Jenkinsfile
└── README.md
```

---

## ⚙️ CI/CD Pipeline Stages

1. **Source Code Checkout**
2. **Docker Image Build**
3. **Security Scan (Trivy)**
4. **Infrastructure Provisioning (Terraform)**
5. **Configuration Management (Ansible)**
6. **Kubernetes Deployment**
7. **Monitoring Setup**
8. **Cloud Migration (AWS)**

---

## ☁️ Cloud Migration Strategy

| Stage            | Environment  |
| ---------------- | ------------ |
| Development      | Local Ubuntu |
| Kubernetes       | KIND (local) |
| Registry         | Local Docker |
| Cloud Registry   | AWS ECR      |
| Cloud Kubernetes | AWS EKS      |

> ⚡ The application is migrated **without changing application code**, only infrastructure and pipeline configuration.

---

## 🔐 Security & Best Practices

* Infrastructure as Code (Terraform)
* Configuration as Code (Ansible)
* Docker image vulnerability scanning with **Trivy**
* Least-privilege AWS IAM usage
* Immutable infrastructure approach
* Automated deployments

---

## 📊 Monitoring

* Prometheus for metrics collection
* Kubernetes-native monitoring
* Designed for easy extension with Grafana

---

## 🚀 How to Run (Local)

```bash
docker build -t devops-node-app .
docker run -p 3000:3000 devops-node-app
```

---

## 📈 Future Enhancements

* Add Grafana dashboards
* Add Blue/Green deployments
* Add GitHub Actions as alternative CI
* Add Helm charts
* Add Canary deployments

---

## 🧠 Key Learning Outcomes

* CI/CD pipeline design
* Infrastructure automation
* Kubernetes deployments
* DevSecOps practices
* Cloud migration strategies
* Troubleshooting real-world DevOps issues

---

## 👤 Author

**Godspower**
DevOps / Cloud / DevSecOps Engineer

---

## ⭐ Why This Project Matters

This project demonstrates **hands-on DevOps engineering skills** aligned with real production workflows and is suitable for:

* DevOps Engineer roles
* Cloud Engineer roles
* DevSecOps roles
* Platform Engineer roles

---
