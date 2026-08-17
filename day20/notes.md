# Commands:

kubectl get gatewayclass
kubectl get gateway
kubectl describe gateway app-gateway
kubectl get httproute
kubectl describe httproute app-route
kubectl get svc
kubectl get endpointslices

#  Interview answer —

#  What is Gateway API?
Gateway API is a Kubernetes networking API made of resources such as GatewayClass, Gateway, and HTTPRoute. It provides a more flexible and extensible way to configure traffic routing than traditional Ingress. Kubernetes

# What is Gateway?
Gateway defines where and how traffic enters, such as listening for HTTP traffic on port 80. Gateway API

# What is HTTPRoute?
HTTPRoute defines how HTTP requests should be matched and forwarded from a Gateway to backend Services.



Day 20 summary

# Remember:

GatewayClass
→ which Gateway implementation

Gateway
→ traffic entry point

HTTPRoute
→ routing rules

Service
→ stable access to Pods


# Full flow:

User
 ↓
Gateway
 ↓
HTTPRoute
 ↓
Service
 ↓
Pods



# And compared with yesterday:

# Day 19:
Ingress + Ingress Controller

# Day 20:
GatewayClass + Gateway + HTTPRoute + Gateway implementation