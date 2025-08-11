# Kubernetes Deployment with Minikube

## 📌 Overview
This repository contains Kubernetes configuration files for deploying and exposing an **Nginx application** locally using **Minikube**.

## 🛠 Tools Used
- **Minikube** – Local Kubernetes cluster
- **kubectl** – Kubernetes CLI
- **Docker** – Container runtime

## 📂 Files in This Repository
- `deployment.yaml` – Defines the Nginx Deployment (replicas, containers, ports)
- `service.yaml` – Defines the Service to expose the Nginx app
- `README.md` – Documentation for setup and usage

## 🚀 Setup Instructions

### 1️⃣ Start Minikube
```bash
minikube start --driver=docker --cpus=2 --memory=4096




### Deploy Application

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

Verify Resources

kubectl get pods
kubectl get services

4️⃣ Access Application

minikube service nginx-service


### If running on EC2 and want external access:

Change service.yaml to type: NodePort.

Allow the NodePort in your EC2 Security Group.

Access via:
http://<EC2-PUBLIC-IP>:<NodePort>
