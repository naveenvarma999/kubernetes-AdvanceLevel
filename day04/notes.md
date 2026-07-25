# Useful Day 4 commands
# Command	Purpose
kubectl apply -f nginx-deployment.yaml	                    Create or update the Deployment
kubectl get deployments	                                    Show Deployments
kubectl get rs	                                            Show ReplicaSets
kubectl get pods	                                        Show Pods
kubectl get pods -w	                                        Watch Pod changes
kubectl describe deployment nginx-deployment	            Show Deployment details
kubectl scale deployment nginx-deployment --replicas=5	    Increase Pods to five
kubectl scale deployment nginx-deployment --replicas=2	    Reduce Pods to two
kubectl delete pod <pod-name>	                         Delete a Pod and test self-healing
kubectl port-forward deployment/nginx-deployment 8080:80	Access one Deployment Pod locally



# Day 4 — Kubernetes Deployment

## Deployment

A Deployment manages application Pods. It maintains the required number
of replicas and recreates Pods when they fail or are deleted.

## Management Structure

Deployment
→ ReplicaSet
→ Pods
→ Containers

## ReplicaSet

A ReplicaSet ensures that the requested number of matching Pods are running.

## Self-Healing Test

I deleted one Deployment-managed Pod. Kubernetes created a new Pod because
the Deployment required three replicas.

## Scaling

Scaling increases or decreases the number of Pod copies.

## Important Commands

```bash
kubectl apply -f nginx-deployment.yaml
kubectl get deployments
kubectl get rs
kubectl get pods
kubectl get pods -w
kubectl describe deployment nginx-deployment
kubectl scale deployment nginx-deployment --replicas=5
kubectl scale deployment nginx-deployment --replicas=2
kubectl delete pod <pod-name>
kubectl port-forward deployment/nginx-deployment 8080:80
kubectl delete -f nginx-deployment.yaml