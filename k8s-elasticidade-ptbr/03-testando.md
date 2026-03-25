# Testando Elasticidade no Kubernetes

## Objetivo

Validar o comportamento do HPA sob carga.

---

## Monitoramento

```bash
kubectl get hpa
kubectl top pods
kubectl get pods -w
```

---

## Gerando carga

### Opção 1 — Curl (loop)

```bash
while true; do curl http://SEU-SERVICO; done
```

---

### Opção 2 — Ferramenta de carga (hey)

```bash
hey -z 1m -c 10 http://SEU-SERVICO
```

---

## O que observar

- Uso de CPU aumentando
- Novos pods sendo criados
- Redução após queda de carga

---

## Após o teste

Pare a carga e observe:

- Pods sendo reduzidos automaticamente

---

## Problemas comuns

| Problema | Causa |
|--------|------|
| Não escala | Metrics Server não instalado |
| CPU não aparece | Requests não definidos |
| Escala lenta | Threshold alto |

---

## Dica

Use aplicações que gerem carga real (ex: loops, cálculos intensivos) para testar melhor o HPA.
