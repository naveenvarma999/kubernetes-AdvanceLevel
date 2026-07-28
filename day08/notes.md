# Important commands

Command	Purpose
kubectl apply -f nginx-resources.yaml	Create the resource-controlled Deployment
kubectl get pods	Check Pod status
kubectl describe pod <name>	View requests, limits and events
kubectl get nodes	View cluster nodes
kubectl delete -f impossible-request-pod.yaml	Remove the Pending practice Pod
kubectl delete -f memory-limit-pod.yaml	Remove the OOM practice Pod
kubectl get pod <name> -o jsonpath="{.status.qosClass}"	Show the Pod’s QoS class



# Day 8 — CPU and Memory Requests and Limits

## Request

A request specifies how much CPU or memory a container expects.

Kubernetes uses requests when deciding which node can run the Pod.

## Limit

A limit specifies the maximum CPU or memory a container can use.

## Behaviour

CPU limit exceeded:
- The container is normally slowed down.

Memory limit exceeded:
- The container may be OOMKilled and restarted.

## Units

CPU:
- 100m = 0.1 CPU
- 500m = 0.5 CPU
- 1000m = 1 CPU

Memory:
- Mi = mebibytes
- Gi = gibibytes

## Easy Difference

Request = used for scheduling

Limit = controls maximum usage