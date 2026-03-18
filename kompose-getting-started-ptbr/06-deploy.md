# Realizando Deploy no Kubernetes

**Progresso:** 6 / 6

[🏠 Início](README.md) | [◀ Anterior](05-kubernetes-local.md)

---

## Conceito

Agora vamos aplicar os arquivos gerados no cluster Kubernetes.

---

## Passo a passo

```bash
kubectl apply -f .

kubectl get pods
kubectl get services
```

---

## Observações

- Pods devem aparecer como **running**.

- Services devem estar disponíveis.

- Se algo estiver errado, utilize os comandos:
  ```bash
  kubectl describe pod <nome>
  kubectl logs <nome>
  ```
