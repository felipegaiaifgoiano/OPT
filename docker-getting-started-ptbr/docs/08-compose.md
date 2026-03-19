# Docker Compose

**Progresso do tutorial:** 8 / 8

[🏠 Início](../README.md) | [◀ Anterior](07-multi-container.md)

Docker Compose permite definir **múltiplos containers** em um único arquivo.

## Exemplo

Neste exemplo, temos:
- um contêiner para a aplicação TODO;
- outro que armazena os dados em um BD.

Crie o arquivo `docker-compose.yml`:

```yaml

services:
  app:
    image: node:24-alpine
    container_name: getting-started-compose
    command: sh -c "npm install && npm run dev"
    ports:
      - 127.0.0.1:3000:3000
    working_dir: /app
    volumes:
      - ./:/app
    environment:
      MYSQL_HOST: mysql
      MYSQL_USER: root
      MYSQL_PASSWORD: secret
      MYSQL_DB: todos

  mysql:
    image: mysql:8.0
    volumes:
      - todo-mysql-data:/var/lib/mysql
    environment:
      MYSQL_ROOT_PASSWORD: secret
      MYSQL_DATABASE: todos

volumes:
  todo-mysql-data:
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
