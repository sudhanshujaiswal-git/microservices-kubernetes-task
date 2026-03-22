# 🚀 Microservices Kubernetes Deployment Task

**Submitted by: Sudhanshu Jaiswal**  
**Date: March 22, 2026**

## ✅ Project Overview
Complete **4 Node.js microservices** successfully dockerized and deployed to **Docker Desktop Kubernetes cluster**.

## 📁 Project Structure


Microservices/
├── user-service/ ← User API (port 3000)
├── order-service/ ← Order API (port 3000)
├── gateway-service/ ← API Gateway (port 3000)
└── payment-service/ ← Payment API (port 3000)

sudhanshu/submission/
└── deployments/ ← Kubernetes YAML manifests
├── user-service.yaml
├── order-service.yaml
├── gateway-service.yaml
└── payment-service.yaml



## 🐳 Docker Commands Executed
```powershell
# Build all 4 images
docker build -t user-service:latest .\Microservices\user-service\
docker build -t order-service:latest .\Microservices\order-service\
docker build -t gateway-service:latest .\Microservices\gateway-service\
docker build -t payment-service:latest .\Microservices\payment-service\


☸️ Kubernetes Deployment
# Deploy all services
kubectl apply -f sudhanshu/submission/deployments/

# Fixed ErrImagePull issue with:
imagePullPolicy: IfNotPresent
