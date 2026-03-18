# Persistindo dados

**Progresso do tutorial:** 5 / 8

[🏠 Início](../README.md) | [◀ Anterior](04-share-app.md) | [Próximo ▶](06-bind-mounts.md)

Containers não foram feitos para armazenar dados permanentemente.

Quando um container é removido, os dados também são perdidos.

Para resolver isso utilizamos **volumes Docker**.

---

## Criando um volume

```bash
docker volume create todo-db
```
---

## Executando container com volume

```bash
docker run -dp 3001:3000 -v todo-db:/etc/todos getting-started
```

Observações: 
- Geralmente utilizamos volume em um container de banco de dados.
- Este é apenas um exemplo ilustrativo.

---

## Próximo passo

Agora vamos ver outra forma de compartilhar arquivos usando bind mounts.

➡ Continue para [**06-bind-mounts.md**](06-bind-mounts.md)
