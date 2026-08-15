# Important Day 18 commands
# Command	Purpose

kubectl get svc	Show Services
kubectl get pods -n kube-system -l k8s-app=kube-dns	Check CoreDNS
kubectl get svc -n kube-system	Check cluster DNS Service
nslookup backend-service	Test DNS
cat /etc/resolv.conf	Check Pod DNS configuration
kubectl get endpointslices	Check Service backends
kubectl logs -n kube-system -l k8s-app=kube-dns	Check DNS logs


# Interview answers

# What is Kubernetes DNS?

Kubernetes DNS allows Pods to find Services using DNS names instead of hard-coded IP addresses. CoreDNS commonly provides this cluster DNS functionality.

# What is Service Discovery?

Service Discovery is the process of one application finding another application. In Kubernetes, Services combined with DNS allow applications to find each other using stable Service names.



# Example?

Frontend
   ↓
http://backend-service
   ↓
CoreDNS
   ↓
backend-service
   ↓
Backend Pods




# Day 18 summary

# Remember only this:

# Pod IP
→ can change


# Service
→ provides stable networking


# DNS
→ provides stable name

# So instead of:

Frontend → 10.244.0.17

# use:

Frontend → backend-service

# And the complete flow is:

Application
    ↓
Service DNS name
    ↓
CoreDNS resolves it
    ↓
Service
    ↓
Matching Pods

Day 18 = Kubernetes applications find each other using Service names instead of remembering IP addresses.