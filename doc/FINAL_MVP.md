# 🚀 AsciiArtify — ArgoCD GitOps PoC (Final MVP)

## 🔍 Overview  
Proof of Concept (PoC) демонстрирует развертывание **ArgoCD** внутри **Kubernetes**-кластера  
в среде **GitHub Codespaces** для реализации GitOps-подхода.

Цель — подтвердить возможность автоматического управления приложениями  
через Git-репозиторий проекта **AsciiArtify**.

---

## ⚙️ Environment  
- **Platform:** GitHub Codespaces (Ubuntu)  
- **Kubernetes:** kind (локальный кластер)  
- **Namespace:** `argocd`  
- **ArgoCD:** stable manifests (`install.yaml` из официального репозитория)  
- **Tools:** `kubectl`, `kind`, `git`

---

## 🧩 Deployment  
```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl wait -n argocd --for=condition=Available deploy/argocd-server --timeout=300s
