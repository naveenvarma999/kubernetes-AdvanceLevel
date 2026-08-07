# Important Day 12 commands
# Command	Purpose

kubectl apply -f node-agent-daemonset.yaml	Create DaemonSet
kubectl get ds	List DaemonSets
kubectl get pods -o wide	See which node each Pod uses
kubectl describe ds node-agent	Detailed DaemonSet information
kubectl logs <pod>	View agent logs
kubectl delete pod <pod>	Test DaemonSet self-healing
kubectl delete -f node-agent-daemonset.yaml	Delete DaemonSet

# 27. Interview question — What is a DaemonSet?

A good simple answer:

A DaemonSet ensures that every required Kubernetes node runs a copy of a Pod. It is commonly used for node-level services such as monitoring agents, log collectors, networking components, and security agents.

# Very short answer

DaemonSet = one Pod on every selected node.

# 28. Deployment vs Job vs CronJob vs DaemonSet

# You now know four important workload types:

Resource	Purpose
Deployment	Keep application Pods running
Job	Run a task once
CronJob	Run tasks on a schedule
DaemonSet	Run a Pod on every selected node

# Easy memory:

Deployment
→ Keep my application running

Job
→ Do this task once

CronJob
→ Do this task repeatedly on schedule

DaemonSet
→ Run this agent on every node


# Day 12 — DaemonSets

## What is a DaemonSet?

A DaemonSet ensures that every required Kubernetes node runs a copy
of a Pod.

## Common Uses

- Log collection
- Node monitoring
- Networking agents
- Security agents
- Storage agents

## Example

3 nodes
→ DaemonSet
→ 3 Pods

One Pod runs on each node.

## Difference

Deployment = runs a requested number of application Pods.

DaemonSet = normally runs one Pod on every selected node.

## Important Commands

kubectl apply -f node-agent-daemonset.yaml
kubectl get ds
kubectl get pods -o wide
kubectl describe ds node-agent
kubectl logs <pod-name>
kubectl delete pod <pod-name>