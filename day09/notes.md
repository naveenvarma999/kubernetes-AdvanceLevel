# Day 9 — Namespaces, Labels, Selectors and Annotations

## Namespace

A Namespace logically separates resources inside one Kubernetes cluster.

Examples:

- development
- testing
- production

Resources can have the same name when they exist in different namespaces.

## Label

A label is a key-value pair used to identify and organise resources.

Examples:

- app=web
- environment=production
- tier=frontend

## Selector

A selector finds resources with matching labels.

Deployments use selectors to manage Pods.

Services use selectors to send traffic to Pods.

## Annotation

An annotation stores extra information about a resource.

Examples:

- Owner
- Description
- Contact
- Build information

## Easy Difference

Namespace = separates groups of resources

Label = identifies a resource

Selector = finds resources using labels

Annotation = stores extra notes


# Command	Purpose
kubectl get ns	                                              List namespaces
kubectl get pods -n development	                              Show development Pods
kubectl get pods -A	                                          Show Pods from all namespaces
kubectl get pods --show-labels	                              Show Pod labels
kubectl get pods -l app=web	                                  Select Pods using a label
kubectl get pods -l app=web,environment=production -A	      Select using multiple labels
kubectl label pod <name> version=v1	                          Add a label
kubectl label pod <name> version-	                          Remove a label
kubectl describe deployment <name>	                          View labels and annotations
kubectl annotate deployment <name> owner=team	              Add an annotation
kubectl annotate deployment <name> owner-	                  Remove an annotation


