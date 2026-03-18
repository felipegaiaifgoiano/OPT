# Introdução ao Kompose

**Progresso:** 1 / 6

[🏠 Início](README.md) | [Próximo ▶](02-instalacao.md)

---

## Conceito

Até agora utilizamos o Docker Compose para executar múltiplos containers.

O problema é que o Docker Compose **não é utilizado em ambientes de produção modernos**.

O **Kubernetes** é a principal plataforma de **orquestração** utilizada atualmente.

O **Kompose** surge como uma ferramenta de migração, permitindo converter aplicações já existentes em Docker Compose para Kubernetes.

---

## Exemplo

Fluxo de migração:

```text
Docker Compose → Kompose → Kubernetes
```

## Observações

Kompose não substitui Kubernetes, apenas acelera a migração inicial.

Em projetos reais, geralmente ajustes são necessários após a conversão.
