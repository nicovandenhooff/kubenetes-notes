# Udemy notes

## Core Concepts

### YAML Basics

- YAML is a human-readable data serialization standard.
- YAML stands for "YAML Ain't Markup Language".
- YAML files have the `.yaml` or `.yml` extension.
- YAML is case-sensitive.
- YAML uses indentation to define the structure of the document.
- YAML uses colons to separate keys and values.
- YAML uses hyphens to create lists.

### Pods

- A pod is the smallest deployable unit in Kubernetes.
- A pod can contain one or more containers.
- A pod can have multiple containers within it ("multi-container pods"), although this is not common.

#### Example `kubectl` commands

```bash
# Create a pod
kubectl run nginx --image=nginx

# Get pods
kubectl get pods -o wide

# Describe a pod
kubectl describe pod nginx

# Pod logs
kubectl logs nginx

# Exec into a pod
kubectl exec -it nginx -- /bin/bash

# Delete a pod
kubectl delete pod nginx

# Create a pod from a YAML file
kubectl apply -f pod-definition.yaml

# Generate a pod YAML file
kubectl run nginx --image=nginx --dry-run=client -o yaml > pod-definition.yaml

# Get a pod YAML file for a running pod
kubectl get pod nginx -o yaml > pod-definition.yaml
``
