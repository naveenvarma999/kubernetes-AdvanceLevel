# StorageClass & Dynamic Provisioning

StorageClass tells Kubernetes how to create storage.

PVC
 ↓
StorageClass
 ↓
Provisioner
 ↓
Actual storage system


# Important commands
# Command	Purpose

kubectl get sc	                       Show StorageClasses
kubectl describe sc local-path	       Inspect StorageClass
kubectl get pvc	                       Check claims
kubectl get pv	                       Check generated PV
kubectl describe pvc dynamic-pvc	   Troubleshoot PVC
kubectl apply -f dynamic-pvc.yaml	   Request storage
kubectl apply -f storage-pod.yaml	   Use storage



# Interview answer

# What is StorageClass?
StorageClass defines a type of storage and tells Kubernetes which provisioner should be used to dynamically create PersistentVolumes.

# What is dynamic provisioning?
Dynamic provisioning automatically creates storage and a PersistentVolume when a PersistentVolumeClaim requests storage, instead of requiring an administrator to create the PV manually first.

# PV vs PVC vs StorageClass
PV represents storage, PVC requests storage, and StorageClass defines how storage can be dynamically provisioned.


# Day 15 — StorageClass and Dynamic Provisioning

## StorageClass

StorageClass describes how Kubernetes storage should be provisioned.

## Static Provisioning

Admin creates PV manually.

PV
→ PVC
→ Pod

## Dynamic Provisioning

Developer creates PVC.

PVC
→ StorageClass
→ Provisioner
→ PV automatically created
→ Pod

## Important

PV = storage resource

PVC = storage request

StorageClass = describes how storage should be created

Provisioner = component that creates the storage

## Commands

kubectl get sc

kubectl get pv

kubectl get pvc

kubectl describe sc local-path

kubectl describe pvc dynamic-pvc