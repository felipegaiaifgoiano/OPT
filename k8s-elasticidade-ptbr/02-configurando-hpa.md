# Configurando HPA no Kubernetes

## Pré-requisitos

- Kubernetes funcionando;
- kubectl configurado.

---

## Instalando Metrics Server

```bash
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```

Verifique:

```bash
kubectl top nodes
kubectl top pods
```

---

## Configurando Elasticidade (Deployment)

1. Adicione resources ao container da aplicação:

```yaml
resources:
  requests:
    cpu: "200m"
  limits:
    cpu: "500m"
```

2. Crie um arquivo `hpa.yaml`:

```yaml
apiVersion: autoscaling/v2
kind: HorizontalPodAutoscaler
metadata:
  name: app-hpa
spec:
  scaleTargetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: app
  minReplicas: 1
  maxReplicas: 5
  metrics:
  - type: Resource
    resource:
      name: cpu
      target:
        type: Utilization
        averageUtilization: 50
```

3. Aplique o HPA:

```bash
kubectl apply -f hpa.yaml
```

4. Verifique se funcionou:

```bash
kubectl get hpa
```
