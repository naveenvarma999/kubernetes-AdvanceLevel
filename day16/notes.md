# StatefulSet + volumeClaimTemplates

# The main idea:

Each StatefulSet Pod can automatically get its own PVC and its own persistent storage.

Kubernetes provides this through volumeClaimTemplates. Each StatefulSet Pod gets its own PVC, and a StorageClass can dynamically provision the backing PV.


# What is volumeClaimTemplates?

Simple definition:

volumeClaimTemplates is a template inside a StatefulSet that tells Kubernetes to create a separate PVC for each StatefulSet Pod.


StatefulSet
     ↓
volumeClaimTemplates
     ↓
Creates PVC for each Pod
     ↓
StorageClass
     ↓
Provisioner
     ↓
Creates PV for each PVC


# Important commands
# Command	Purpose

kubectl get sts	                  Show StatefulSets
kubectl get pods	              Show StatefulSet Pods
kubectl get pvc	                  Show each Pod's PVC
kubectl get pv	                  Show backing PVs
kubectl get sc	                  Show StorageClasses
kubectl describe pvc <name>	      Inspect a claim
kubectl delete pod demo-db-1	  Test persistent identity/storage
kubectl scale sts demo-db --replicas=4	Scale StatefulSet