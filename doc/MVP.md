# MVP Demo — ArgoCD на Kubernetes (AsciiArtify)

## 1) Обзор
Цель: показать развернутый ArgoCD в кластере Kubernetes и рабочий GitOps-контур для проекта **AsciiArtify**.

## 2) Среда
- **Платформа:** GitHub Codespaces (Ubuntu)
- **Kubernetes:** kind (внутри Codespaces)
- **Namespace:** `argocd`
- **ArgoCD:** stable (официальные манифесты)

## 3) Установка ArgoCD
```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl wait -n argocd --for=condition=Available deploy/argocd-server --timeout=300s
kubectl wait ...).
