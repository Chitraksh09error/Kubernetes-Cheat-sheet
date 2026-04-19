# KUBERNETES-COMMANDS

```bash
# Clone Repo
git clone <your-repo-url>
cd <your-project-folder>

# Start Minikube
```bash
minikube start --driver=docker
```

# Stop Minikube
minikube stop

# Delete Minikube
minikube delete

# Check Contexts
kubectl config get-contexts

# Switch to Minikube
kubectl config use-context minikube

# Switch to Docker Desktop
kubectl config use-context docker-desktop

# Current Context
kubectl config current-context

# Check Nodes
kubectl get nodes

# Apply Kubernetes Files
kubectl apply -f k8s/

# Delete Kubernetes Files
kubectl delete -f k8s/

# Get Pods
kubectl get pods

# Get All Pods
kubectl get pods -A

# Get Services
kubectl get services

# Get Services (Short)
kubectl get svc

# Describe Pod
kubectl describe pod <pod-name>

# View Logs
kubectl logs <pod-name>

# Delete Pod
kubectl delete pod <pod-name>

# Scale Deployment
kubectl scale deployment <deployment-name> --replicas=3

# Create Deployment
kubectl create deployment hello --image=nginx

# Expose Deployment
kubectl expose deployment hello --type=NodePort --port=80

# Access Service (Minikube)
minikube service <service-name>

# Access Service (Docker Desktop)
kubectl port-forward service/<service-name> 3000:80
