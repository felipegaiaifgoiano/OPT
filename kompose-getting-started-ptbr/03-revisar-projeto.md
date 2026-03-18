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

  db:
    image: mysql
    environment:
      MYSQL_ROOT_PASSWORD: root
```

---

# Observações

- Deve haver pelo menos dois serviços.

- Banco de dados é altamente recomendado.

- Uso de volumes melhora o resultado da conversão.