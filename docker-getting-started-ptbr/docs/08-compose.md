# Docker Compose

**Progresso do tutorial:** 8 / 8

[🏠 Início](../README.md) | [◀ Anterior](07-multi-container.md)

Docker Compose permite definir múltiplos containers em um único arquivo.

## Exemplo

Arquivo `docker-compose.yml`:

```yaml
version: "3.8"

services:
  app:
    build: .
    ports:
      - "3000:3000"
```

---

## Executando a aplicação

```bash
docker compose up
```

Isso iniciará todos os serviços definidos no arquivo.

---

## Conclusão

Neste tutorial você aprendeu:

- executar containers
- construir imagens
- compartilhar imagens
- persistir dados
- executar aplicações com múltiplos containers
- utilizar Docker Compose
