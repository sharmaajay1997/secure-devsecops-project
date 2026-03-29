# 🚀 End-to-End DevSecOps Pipeline on AWS EKS

## 📌 Project Overview

This project demonstrates a complete DevSecOps pipeline integrating CI/CD, security scanning, containerization, Kubernetes deployment, monitoring, and centralized logging.

---

## 🏗️ Architecture

GitHub → Jenkins → SonarQube → Docker → Trivy → Kubernetes (EKS) →
Falco (Runtime Security) → Prometheus & Grafana → Elasticsearch & Kibana

---

## ⚙️ Tech Stack

* CI/CD: Jenkins
* Code Quality: SonarQube
* Security: Gitleaks, Trivy, Falco
* Containerization: Docker
* Orchestration: Kubernetes (AWS EKS)
* Monitoring: Prometheus, Grafana
* Logging: Elasticsearch, Kibana

---

## 🔐 Security Implementation

* 🔍 Secrets Detection using Gitleaks
* 🛡️ Static Code Analysis using SonarQube
* 🐳 Container Vulnerability Scanning using Trivy
* 🚨 Runtime Threat Detection using Falco

---

## 📊 Monitoring & Logging

* 📈 Prometheus for metrics collection
* 📊 Grafana dashboards
* 📜 Elasticsearch for log storage
* 🔎 Kibana for log visualization

---

## 🚀 Deployment Steps

1. Push code to GitHub
2. Jenkins pipeline triggers
3. SonarQube scans code
4. Docker image build
5. Trivy scans image
6. Deploy to Kubernetes using manifests
7. Monitor via Prometheus & Grafana
8. Analyze logs via Kibana

---

## ⚠️ Challenges & Solutions

* ❌ Elasticsearch CrashLoopBackOff → Fixed using vm.max_map_count
* ❌ Resource exhaustion → Upgraded EKS nodes
* ❌ Kibana 503 error → Disabled X-Pack security
* ❌ Helm failures → Switched to lightweight deployments

---

## 🎯 Key Achievements

* Built complete DevSecOps pipeline from scratch
* Integrated security at every stage
* Solved real-world production issues
* Deployed scalable architecture on AWS EKS

---

## 📌 Future Improvements

* Terraform for Infrastructure as Code
* ArgoCD for GitOps
* HTTPS + IAM integration

---
