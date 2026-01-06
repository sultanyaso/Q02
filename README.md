
# MERN App on Kubernetes

## Student Info
- Name: Yasir Sultan  
- Roll No: i221510  

---

## Project Overview
This project deploys a MERN stack application on Kubernetes using Minikube.  
It includes:
- Frontend   
- Backend  
- MongoDB database with persistent storage  

---

## How to Run
1. Make sure Minikube and kubectl are installed.  
2. Start Minikube:


minikube start --driver=docker


3. Apply namespace:


kubectl apply -f namespace.yaml


4. Apply MongoDB PVC and deployment:

kubectl apply -f mongo-pvc.yaml
kubectl apply -f mongodb-deployment.yaml


5. Apply backend deployment and service:


kubectl apply -f backend-deployment.yaml
kubectl apply -f backend-service.yaml


6. Apply frontend deployment and service:


kubectl apply -f frontend-deployment.yaml
kubectl apply -f frontend-service.yaml


7. Check pods:


kubectl get pods -n i221510-mern-app


8. Open frontend in browser:


minikube ip
http://<minikube-ip>:30173

