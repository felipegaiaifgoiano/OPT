# Compartilhando a aplicação

**Progresso do tutorial:** 4 / 8

[🏠 Início](../README.md) | [◀ Anterior](03-update-app.md) | [Próximo ▶](05-persist-data.md)

Para compartilhar imagens Docker utilizamos um Docker registry.

O mais comum é o **Docker Hub**, sendo considerado o padrão de desenvolvimento.

---
## Crie um repositório

1. Crie uma conta no [Docker Hub](https://hub.docker.com/).
2. Crie um repositório **público** chamado ```getting-started```.

## Enviando a imagem

No terminal do seu sistema operacional, execute os comandos:

1. Acessando o Docker Hub:
```bash
docker login SEU_USUARIO
```

2. Criando uma tag da imagem:
```bash
docker tag getting-started SEU_USUARIO/getting-started
```

3. Enviando a imagem:
```bash
docker push SEU_USUARIO/getting-started
```

---

## Próximo passo

Agora vamos aprender como persistir dados em containers.

➡ Continue para [**05-persist-data.md**](05-persist-data.md)
