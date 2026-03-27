# Testando Elasticidade

## Monitoramento

```bash
kubectl get pods -w
kubectl get hpa
kubectl top pods
```

---

## Gerando carga

```bash
while true; do curl http://EXTERNAL-IP; done
```

---

## O que observar
- CPU aumenta
- Pods aumentam
- Sistema estabiliza

---

## Limitações
- Pode não escalar nós
- Sessão pode expirar
