## 🔐 DevSecOps Security Architecture Flow

The implemented DevSecOps pipeline follows a layered security approach integrated across the entire software delivery lifecycle.

### 🔄 Workflow

Developer → Code Push  
↓  
CI/CD Pipeline (Jenkins + Security Scans)  
↓  
Container Image (Docker + Trivy Scan)  
↓  
Kubernetes Cluster Deployment  
↓  
Security Layers Applied:  
- RBAC (Role-Based Access Control)  
- Network Policies (Pod-to-Pod Traffic Control)  
- SecurityContext (Container Security Hardening)  
↓  
Runtime Security Monitoring (Falco)  
↓  
Monitoring & Alerting (Prometheus + Grafana)

---

## 🧠 Explanation of Each Layer

### 1. Developer & Source Control
- Developers push code to GitHub
- Triggers automated CI/CD pipeline

### 2. CI/CD Pipeline
- Jenkins automates:
  - Code build
  - Security scanning (SonarQube, Gitleaks)
  - Image build and validation

### 3. Container Security
- Docker images are scanned using Trivy
- Ensures no vulnerable packages are deployed

### 4. Kubernetes Deployment
- Application deployed on AWS EKS cluster
- Uses Kubernetes manifests for orchestration

### 5. Kubernetes Security Layers
- RBAC: Restricts access to cluster resources  
- Network Policies: Controls communication between pods  
- SecurityContext: Enforces non-root containers and privileges  

### 6. Runtime Security
- Falco monitors system calls
- Detects anomalies like:
  - Privilege escalation  
  - Suspicious container behavior  

### 7. Monitoring & Alerts
- Prometheus collects metrics
- Grafana visualizes system health
- Alerts configured for anomalies

---

## 🎯 Key Security Benefits

- Security integrated at every stage (Shift-left + runtime)
- Reduced risk of vulnerabilities in production
- Real-time threat detection and response
- Strong Kubernetes security posture

---