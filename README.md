# Kubernetes Minikube Deployment - Task 5

## Objective
Build a local Kubernetes cluster using Minikube and deploy a simple application.

## Tools Used
- Minikube
- kubectl
- Docker

## Steps Performed
1. Installed Minikube and kubectl.
2. Started Minikube cluster using Docker driver.
3. Created `deployment.yaml` to deploy the app.
4. Created `service.yaml` to expose the app.
5. Verified pods and service status using kubectl commands.
6. Scaled deployment to 4 replicas.
7. Checked pod logs and deployment details.

## Files
- `deployment.yaml` - Kubernetes deployment configuration
- `service.yaml` - Service configuration exposing the deployment

## Screenshots

### Pods Status
![Pods Status](screenshots/pod_status.png)

### Deployment Description
![Deployment Description](screenshots/deployment_description.png)

### Pod Logs
![Pod Logs](screenshots/pod_logs.png)

### Service Access URL
![Service URL](screenshots/service_url.png)

## Commands Used
```bash
minikube start --driver=docker
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl get pods
kubectl scale deployment hello-deployment --replicas=4
kubectl describe deployment hello-deployment
kubectl logs hello-deployment-5c58ccc9b5-h8l9m
minikube service hello-service
