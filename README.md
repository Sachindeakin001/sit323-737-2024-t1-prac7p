# SIT737 Task 9.1P – MongoDB Integration in Kubernetes

## 📌 Project Overview
This task demonstrates a cloud-native deployment of a Node.js application integrated with MongoDB, deployed using Docker and Kubernetes. It includes persistent storage, secure credential management, and basic CRUD functionality via RESTful endpoints.

## 🧱 Tech Stack
- Node.js + Express
- MongoDB + Mongoose
- Docker
- Kubernetes (kubectl)
- Secrets, PVCs, and Services

## 🚀 Setup Steps

### 1. Build & Push Docker Image

docker build -t sachinynr001/737_week9.1 .
docker push sachinynr001/737_week9.1

2. Create
   kubectl create secret generic mongo-secret \
  --from-literal=mongo-user=admin \
  --from-literal=mongo-password=admin123

3. Apply Kubernetics file
    kubectl apply -f mongo-pv.yaml
kubectl apply -f mongo-deployment.yaml
kubectl apply -f app-deployment.yaml

5. Access app
   kubectl get svc node-service
