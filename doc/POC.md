# Proof of Concept: ArgoCD Deployment on Kubernetes

## 1. Overview
This Proof of Concept (PoC) demonstrates the deployment of **ArgoCD** on a local Kubernetes cluster to verify the GitOps concept for the AsciiArtify project.

## 2. Environment
- **OS:** Ubuntu 22.04 (WSL2)
- **Kubernetes:** Minikube v1.33.0
- **ArgoCD version:** stable (latest)
- **Namespace:** argocd

## 3. Steps to Deploy

### 1. Start Kubernetes Cluster
```bash
minikube start --driver=docker
kubectl get nodes
