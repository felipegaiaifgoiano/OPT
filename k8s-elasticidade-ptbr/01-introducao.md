# Elasticidade no Kubernetes — Conceitos

## O que é Elasticidade?

Elasticidade é a capacidade de um sistema ajustar automaticamente seus recursos conforme a demanda, aumentando ou reduzindo instâncias (pods).

---

## Tipos de Elasticidade

### 1. Horizontal
- Escala o número de pods.

### 2. Vertical
- Escala os recursos do pod.

### 3. Cluster
- Escala o número de nós do cluster.


## 3. No Kubernetes

| Tipo | Nome                            | Recurso                  |
|------|---------------------------------|--------------------------|
| 1    | Horizontal Pod Autoscaler (HPA) | CPU / RAM / métricas     |
| 2    | Vertical Pod Autoscaler (VPA)   | CPU / RAM                |
| 3    | Cluster Autoscaler              | Número de nós            |

---

## Vantagens

- Melhor uso de recursos
- Alta disponibilidade
- Redução de custos
- Escalabilidade automática

---

## Requisitos para Elasticidade

- Metrics Server instalado
- Requests e Limits definidos
- Aplicação stateless (preferencialmente)

---

## Resumo

Elasticidade permite que aplicações sejam resilientes, eficientes e preparadas para variações de carga.
