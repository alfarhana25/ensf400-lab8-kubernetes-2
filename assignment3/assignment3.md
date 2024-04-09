
```bash
#!/bin/bash

# Change to the assignment3 directory
cd assignment3 || exit

# Start Minikube and enable the Ingress addon
minikube start
minikube addons enable ingress

# Apply the Kubernetes configuration files
kubectl apply -f '*.yaml'

# Access the application using curl
curl http://$(minikube ip)/

# Get information about pods
kubectl get pods

# Get information about deployments
kubectl get deployments

# Get information about ingresses
kubectl get ingresses
