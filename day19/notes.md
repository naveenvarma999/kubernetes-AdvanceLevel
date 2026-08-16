# Day 19 command table
# Command	Purpose

kubectl get ingress	                                      Show Ingress resources
kubectl get ing	                                          Short version
kubectl describe ingress <name>	                          Inspect routing rules
kubectl get ingressclass	                              Show available controllers/classes
kubectl get svc	                                          Check backend Services
kubectl get endpointslices	                              Check Service backends
kubectl get pods -A	                                      Look for an Ingress controller


# Interview answers

# What is Ingress?
Ingress is a Kubernetes API object that defines HTTP/HTTPS routing rules from outside the cluster to Kubernetes Services. Kubernetes

# What is an Ingress Controller?
An Ingress Controller is the component that watches Ingress resources and actually implements their routing rules. An Ingress resource alone does not route traffic. Kubernetes

# Service vs Ingress?
A Service provides stable access to Pods, while Ingress routes external HTTP/HTTPS requests to Services.

# Day 19 summary
# Remember this:

Internet
    ↓
Ingress Controller
    ↓
Ingress rules
    ↓
Service
    ↓
Pods
Example:
/
→ frontend-service

/api
→ backend-service
And the most important distinction:
Ingress
→ routing rules

# Ingress Controller
→ actually performs routing

Day 19 = one HTTP/HTTPS entry point that routes requests to different Kubernetes Services