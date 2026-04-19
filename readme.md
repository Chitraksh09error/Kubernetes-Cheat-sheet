# Kubernetes Commands Cheat Sheet

## Minikube Management
**Start Minikube cluster locally with Docker driver.**
```bash
minikube start --driver=docker
```

**Stop the running Minikube cluster.**
```bash
minikube stop
```

**Delete the entire Minikube cluster and its data.**
```bash
minikube delete
```

## Kubeconfig Management
**List all available Kubernetes contexts.**
```bash
kubectl config get-contexts
```

**Switch to Minikube context.**
```bash
kubectl config use-context minikube
```

**Switch to Docker Desktop context.**
```bash
kubectl config use-context docker-desktop
```

**Show currently active Kubernetes context.**
```bash
kubectl config current-context
```

## Cluster Inspection
**List all nodes in the cluster.**
```bash
kubectl get nodes
```

## Deployment Management
**Apply Kubernetes manifests from directory.**
```bash
kubectl apply -f k8s/
```

**Delete Kubernetes resources from directory.**
```bash
kubectl delete -f k8s/
```

## Resource Monitoring
**List pods in current namespace.**
```bash
kubectl get pods
```

**List all pods across all namespaces.**
```bash
kubectl get pods -A
```

**List all services in current namespace.**
```bash
kubectl get services
```

**List services in short format.**
```bash
kubectl get svc
```

## Pod Debugging
**Get detailed information about a specific pod.**
```bash
kubectl describe pod <pod-name>
```

**View logs from a specific pod.**
```bash
kubectl logs <pod-name>
```

**Delete a specific pod.**
```bash
kubectl delete pod <pod-name>
```

## Scaling & Deployment
**Scale deployment to specified number of replicas.**
```bash
kubectl scale deployment <deployment-name> --replicas=3
```

**Create a new deployment from Docker image.**
```bash
kubectl create deployment hello --image=nginx
```

**Expose deployment as a service.**
```bash
kubectl expose deployment hello --type=NodePort --port=80
```

## Service Access
**Open browser to access Minikube service.**
```bash
minikube service <service-name>
```

**Forward service port to local machine.**
```bash
kubectl port-forward service/<service-name> 3000:80
```

---

*Perfect for quick Kubernetes operations during development and debugging!*
