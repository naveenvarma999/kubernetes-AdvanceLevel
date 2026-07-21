# Kubernetes Commands Cheat Sheet

## Cluster Information

```bash
kubectl cluster-info
kubectl get nodes
kubectl get namespaces
kubectl api-resources
```

## Workloads

```bash
kubectl get pods -A
kubectl get deployments
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl logs <pod-name> --previous
kubectl exec -it <pod-name> -- sh
```

## Apply and Delete

```bash
kubectl apply -f file.yaml
kubectl delete -f file.yaml
```

## Rollouts

```bash
kubectl rollout status deployment/<name>
kubectl rollout history deployment/<name>
kubectl rollout undo deployment/<name>
```

## Troubleshooting

```bash
kubectl get events --sort-by=.metadata.creationTimestamp
kubectl get pods -o wide
kubectl get endpointslices
kubectl top pods
kubectl top nodes
kubectl auth can-i --list
```
