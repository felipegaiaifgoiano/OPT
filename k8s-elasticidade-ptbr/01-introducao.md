# Elasticidade no Kubernetes — Conceitos

## O que é Elasticidade?

Elasticidade é a capacidade de um sistema de ajustar dinamicamente seus recursos de acordo com a demanda, ou seja, aumentando/reduzindo automaticamente a quantidade de instâncias (réplicas) ou de recursos computacionais.

---

## Tipos de Elasticidade

O Kubernetes oferece mecanismos para escalar automaticamente:

1. Horizontalmente: escala o número de pods.

2. Verticalmente: escala os recursos do pod.

3. A nível de cluster: escala o número de nós do cluster.

### Como o Kubernetes escala?

| Tipo | Nome                            | Recurso                  |
|------|---------------------------------|--------------------------|
| 1    | Horizontal Pod Autoscaler (HPA) | CPU / RAM / métricas     |
| 2    | Vertical Pod Autoscaler (VPA)   | CPU / RAM                |
| 3    | Cluster Autoscaler              | Número de nós            |

---

## Vantagens

- Maior eficiência no uso de recursos: usa apenas o necessário;
- Alta disponibilidade: lida com picos de acesso (requisições) automaticamente;
- Redução de custos: em ambientes em nuvem, evita pagar por recursos ociosos;
- Escalabilidade automatizada: reduz necessidade de intervenção manual.

---

## Requisitos para Elasticidade

- Metrics Server instalado.
- Requests e Limits definidos.
- Aplicação stateless (preferencialmente).

---

## Resumo

Elasticidade permite que aplicações sejam resilientes, eficientes e preparadas para variações de carga.
