# Day 5 — Kubernetes Services

## What is a Service?

A Kubernetes Service provides a stable network name and virtual IP for
a group of matching Pods.

Pods can be deleted and receive new IP addresses, but the Service remains
stable while it exists.

## Traffic Flow

Client
→ Service
→ Matching Pod
→ Container

## Selector

The Service uses a label selector to find Pods.

Service selector:

app=nginx

Pod label:

app=nginx

## Ports

- port: The port provided by the Service.
- targetPort: The port inside the target Pod/container.

## ClusterIP

ClusterIP is the default Service type. It provides internal cluster access.

## Important Commands

```bash
kubectl apply -f nginx-service.yaml
kubectl get svc
kubectl describe svc nginx-service
kubectl get pods --show-labels
kubectl get endpointslices
kubectl port-forward svc/nginx-service 8080:80
kubectl delete svc nginx-service


| Command                                          | What it does                                | Why we use it                          |
| ------------------------------------------------ | ------------------------------------------- | -------------------------------------- |
| `kubectl get svc`                                | Lists Services                              | Check Service status and IP            |
| `kubectl describe svc nginx-service`             | Shows Service details                       | Inspect ports, selector and endpoints  |
| `kubectl apply -f nginx-service.yaml`            | Creates or updates the Service              | Manage the Service declaratively       |
| `kubectl port-forward svc/nginx-service 8080:80` | Connects local port 8080 to Service port 80 | Test the Service in a browser          |
| `kubectl get pods --show-labels`                 | Shows Pod labels                            | Confirm the Service selector can match |
| `kubectl get endpointslices`                     | Shows Service backend information           | Check which Pods receive traffic       |
| `kubectl delete svc nginx-service`               | Deletes the Service                         | Remove the stable network endpoint     |
| `kubectl expose deployment ...`                  | Creates a Service from a workload           | Quickly expose a Deployment            |
