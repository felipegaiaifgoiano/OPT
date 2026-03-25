# Elasticidade no Kubernetes — Conceitos

## O que é Elasticidade?

Elasticidade é a capacidade de um sistema ajustar automaticamente seus recursos conforme a demanda, aumentando ou reduzindo instâncias (pods).

---

## Tipos de Elasticidade

### 1. Horizontal (HPA)
- Escala o número de pods
- Baseado em CPU, memória ou métricas customizadas

### 2. Vertical (VPA)
- Ajusta CPU e memória do pod

### 3. Cluster Autoscaler
- Ajusta o número de nós do cluster

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
