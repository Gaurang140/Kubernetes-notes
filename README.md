# Kubernetes `kubectl` Commands

This document provides a list of essential `kubectl` commands for managing Kubernetes clusters. The `kubectl` command-line tool is used to interact with Kubernetes clusters.

---

For more information about Minikube installation and usage, refer to the [Minikube Installation Guide](minikube.md).
```



## Basic Information and Status

- **View Cluster Info:**
  ```bash
  kubectl cluster-info
  ```
  This command displays information about the Kubernetes cluster.

- **View Nodes:**
  ```bash
  kubectl get nodes
  ```
  Use this command to list all nodes in the cluster.

## Pods and Deployments

- **List Pods:**
  ```bash
  kubectl get pods
  ```
  List all pods in the default namespace.

- **List Pods in All Namespaces:**
  ```bash
  kubectl get pods --all-namespaces
  ```
  List pods in all namespaces.

- **Describe a Pod:**
  ```bash
  kubectl describe pod <pod-name>
  ```
  Get detailed information about a specific pod.

- **Create a Deployment:**
  ```bash
  kubectl create deployment <deployment-name> --image=<image-name>
  ```
  Create a deployment with a specified image.

- **Scale a Deployment:**
  ```bash
  kubectl scale deployment <deployment-name> --replicas=<desired-replica-count>
  ```
  Scale the number of replicas for a deployment.

## Services

- **List Services:**
  ```bash
  kubectl get services
  ```
  List all services in the default namespace.

- **Expose a Deployment as a Service:**
  ```bash
  kubectl expose deployment <deployment-name> --type=LoadBalancer --port=<port-number>
  ```
  Create a service to expose a deployment externally.

## Logs and Debugging

- **Get Container Logs:**
  ```bash
  kubectl logs <pod-name> -c <container-name>
  ```
  Fetch logs from a specific container within a pod.

- **Interactive Shell in a Pod:**
  ```bash
  kubectl exec -it <pod-name> -- /bin/sh
  ```
  Open an interactive shell within a pod.

## Cleanup

- **Delete a Resource:**
  ```bash
  kubectl delete <resource-type> <resource-name>
  ```
  Delete a specific resource (pod, deployment, service, etc.).

- **Delete All Resources in Namespace:**
  ```bash
  kubectl delete all --all -n <namespace>
  ```
  Delete all resources in a specific namespace.

---






