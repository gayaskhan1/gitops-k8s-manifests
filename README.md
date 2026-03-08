# gitops-k8s-manifests
# GitOps CI/CD Demo Project

This project demonstrates a simple DevOps pipeline using:

- Docker
- Kubernetes (Minikube)
- ArgoCD
- GitHub Actions

The application is a simple Flask app containerized with Docker and deployed to Kubernetes using GitOps principles.

---

## Project Architecture

Developer → GitHub → Docker Build → Kubernetes Deployment → ArgoCD Sync

---

## Technologies Used

- Python Flask
- Docker
- Kubernetes (Minikube)
- kubectl
- ArgoCD
- GitHub

---

## Step 1: Clone Repository

git clone https://github.com/gayaskhan1/gitops-demo-app.git

cd gitops-demo

---

## Step 2: Build Docker Image

docker build -t gitops-app .

---

## Step 3: Run Docker Container

docker run -p 5000:5000 gitops-app

Open browser:

http://localhost:5000

---

## Step 4: Deploy to Kubernetes

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

Check:

kubectl get pods
kubectl get svc

---

## Step 5: Access Application

minikube service gitops-service

---

## Step 6: Install ArgoCD

kubectl create namespace argocd

kubectl apply -n argocd \
-f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

---

## Author

Mohd Gayasuddin Khan  
DevOps Engineer
