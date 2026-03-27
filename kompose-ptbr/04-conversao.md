# Convertendo com Kompose

**Progresso:** 4 / 6

[🏠 Início](README.md) | [◀ Anterior](03-revisar-projeto.md) | [Próximo ▶](05-kubernetes-local.md)

---

## Conceito

O Kompose transforma automaticamente os serviços do Docker Compose em recursos Kubernetes.

Geralmente são gerados vários arquivos, que devem ser implantados em conjunto.

Cada serviço pode gerar diferentes recursos, como Deployment, Service e volumes persistentes.

---

## Passo a passo

Na pasta onde se encontra o arquivo do Docker Compose, execute:

```bash
kompose convert
```

---

## Observações

- Os arquivos gerados dependem da configuração do projeto.

- Para cada serviço, normalmente são criados arquivos com o nome do serviço, por exemplo:

  - ```app-deployment.yaml```

  - ```app-service.yaml```

  - ```db-deployment.yaml```

  - ```db-service.yaml```

- Quando há volume, também é criado:

  - ```db-data-pvc.yaml```
