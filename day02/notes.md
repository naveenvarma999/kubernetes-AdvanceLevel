# Day 2 — Local Kubernetes Cluster Setup

## Tools
- Docker Desktop runs containers.
- kind creates a local Kubernetes cluster using Docker containers.
- kubectl communicates with the Kubernetes API server.

## Cluster Name
kubernetes-learning

# Useful commands from today
docker version
kubectl version --client
kind version
kind get clusters
kubectl config current-context
kubectl config get-contexts
kubectl cluster-info
kubectl get nodes
kubectl get nodes -o wide
kubectl get pods -A
docker ps



kind creates a local Kubernetes cluster on your computer using Docker.

kind = creates the Kubernetes cluster

# Example:
kind create cluster


kubectl

kubectl sends commands to the Kubernetes cluster.
kubectl = controls and checks the cluster


# Examples:

kubectl get nodes
kubectl get pods
kubectl apply -f pod.yaml



# Simple comparison:

kind    → creates the cluster
kubectl → manages the cluster

#

kind uses Docker to create containers that behave like Kubernetes machines (nodes).

Think of it like this:

Your computer
   ↓
Docker
   ↓
Creates containers
   ↓
Each container acts as a Kubernetes node

# For example, when you run:
kind create cluster

# kind asks Docker to create a container such as:
kubernetes-learning-control-plane

# That Docker container contains Kubernetes components like:
API Server
Scheduler
Controller Manager
etcd
Kubelet
containerd

So Docker provides the environment where the Kubernetes node runs.