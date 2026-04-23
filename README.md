# 🧮 Multiservice Tax Calculator — Docker & Kubernetes

A production-style **microservices application** demonstrating 
containerization with Docker and orchestration with Kubernetes (K8s).
Built as part of the Full-Stack AI DevOps Masterclass.

---

# 🏗️ Architecture
Browser
↓
Frontend (React + Vite + Nginx)  →  NodePort 32500
↓
Service A (Node.js)              →  NodePort 32400
↓
Service B (Node.js)              →  ClusterIP (internal only)

---

## 🛠️ Tech Stack

| Layer | Technology |

| Frontend | React, Vite, Tailwind CSS, Nginx |
| Backend | Node.js (Service A & B) |
| Containerization | Docker, Docker Hub |
| Orchestration | Kubernetes (K8s) |
| Languages | JavaScript, Java, Python|

---

## 📁 Project Structure

📁 K8s/
└── app2-tax-calculator/
├── app-a.yaml        # Service A deployment + NodePort
├── app-b.yaml        # Service B deployment + ClusterIP
├── app-front.yaml    # Frontend deployment + NodePort
├── config2.yaml      # ConfigMap
└── secret2.yaml      # Secrets
📁 docker/
└── app2-tax-calculator/
├── docker-compose.yml
├── node/
│   ├── service-a/    # Node.js backend
│   └── service-b/    # Node.js tax service
├── spring/           # Java Spring Boot version
├── python/           # Python version
└── tax-calculator-frontend/  # React frontend
---

## 🐳 Docker Hub Images

| Service | Image |
|---|---|
| Frontend | `adarshhhh21/frontend:latest` |
| Service A | `adarshhhh21/service-a:latest` |
| Service B | `adarshhhh21/service-b:latest` |

---

## 🚀 Run with Kubernetes

```bash
# Apply all manifests
kubectl apply -f K8s/app2-tax-calculator/

# Check pods
kubectl get pods

# Check services
kubectl get svc
```
