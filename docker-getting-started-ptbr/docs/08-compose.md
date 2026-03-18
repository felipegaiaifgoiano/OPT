# Docker Compose

**Progresso do tutorial:** 8 / 8

[🏠 Início](../README.md) | [◀ Anterior](07-multi-container.md)

Docker Compose permite definir múltiplos containers em um único arquivo.

## Exemplo

Arquivo `docker-compose.yml`:

```yaml
services:
  app:
    image: node:18
    container_name: getting-started
    working_dir: /app
    volumes:
      # Bind mount (código)
      - .:/app
      # Volume para persistência do SQLite
      - todo-db:/app/data
    command: sh -c "npm install && node src/index.js"
    ports:
      - "3000:3000"

volumes:
  todo-db:
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

---

## Próximo passo

Agora que você já sabe trabalhar com múltiplos containers, é possível migrar sua aplicação para Kubernetes.

➡ Continue para [**Kompose + Kubernetes Local**](../../kompose-getting-started-ptbr/README.md)
