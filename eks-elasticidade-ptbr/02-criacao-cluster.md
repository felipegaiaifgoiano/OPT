# 🏗️ Criando Cluster EKS

## Pré-requisitos
- AWS CLI
- eksctl
- kubectl

---

## Criando cluster

```bash
eksctl create cluster \
  --name eks-elasticidade \
  --region us-east-1 \
  --nodes 2 \
  --node-type t3.medium
```

---

## Verificar

```bash
kubectl get nodes
```

---

## Metrics Server

```bash
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```
