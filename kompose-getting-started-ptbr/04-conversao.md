# Convertendo com Kompose

**Progresso:** 4 / 6

[🏠 Início](README.md) | [◀ Anterior](03-revisar-projeto.md) | [Próximo ▶](05-kubernetes-local.md)

---

## Conceito

O Kompose transforma automaticamente os serviços do Docker Compose em recursos Kubernetes.

Cada serviço vira:

- Deployment
- Service

---

## Passo a passo

```bash
kompose convert
ls
```

---

## Observações

- Arquivos gerados:

- deployment.yaml

- service.yaml