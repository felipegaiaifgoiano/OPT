# Revisando o Projeto Docker Compose

**Progresso:** 3 / 6

[🏠 Início](README.md) | [◀ Anterior](02-instalacao.md) | [Próximo ▶](04-conversao.md)

---

## Conceito

Antes de converter, o projeto precisa estar bem estruturado.

O Kompose funciona melhor quando o Docker Compose segue boas práticas.

---

## Exemplo

```yaml
version: "3.8"

services:
  app:
    build: .
    ports:
      - "3000:3000"
    depends_on:
      - db

  db:
    image: mysql:8
    environment:
      MYSQL_ROOT_PASSWORD: root
      MYSQL_DATABASE: appdb
    volumes:
      - db-data:/var/lib/mysql

---

volumes:
  db-data:
```

---

## Observações

- Deve haver pelo menos **dois serviços**.

- Uso de banco de dados é altamente recomendado.

- Uso de volumes garante persistência de dados.

- Uso de ```depends_on``` ajuda organizar a ordem de inicialização.
