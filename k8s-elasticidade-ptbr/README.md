# Elasticidade no Kubernetes (Guia Completo)

Este repositório contém um guia completo sobre **elasticidade no Kubernetes**, dividido em três partes:

## Conteúdo

1. [Conceitos de Elasticidade](01-conceitos-elasticidade-kubernetes.md)
2. [Configuração do HPA](02-configurando-hpa.md)
3. [Testes de Elasticidade](03-testando-elasticidade.md)

---

## Objetivo

Ensinar de forma prática e progressiva:

- Conceitos fundamentais
- Configuração real de autoescalonamento
- Testes práticos com geração de carga

---

## Tecnologias

- Kubernetes
- kubectl
- Metrics Server
- HPA (Horizontal Pod Autoscaler)

---

## Como usar este repositório

1. Comece pelos conceitos
2. Configure o HPA em um projeto existente
3. Execute os testes de carga

---

## Fluxo sugerido

```bash
# 1. Instalar metrics server
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml

# 2. Aplicar HPA
kubectl apply -f hpa.yaml

# 3. Monitorar
kubectl get hpa
kubectl top pods
```

---

## Licença

Uso educacional.
