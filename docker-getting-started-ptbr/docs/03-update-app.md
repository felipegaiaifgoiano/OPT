# Atualizando a aplicação

**Progresso do tutorial:** 3 / 8

[🏠 Início](../README.md) | [◀ Anterior](02-our-application.md) | [Próximo ▶](04-share-app.md)

Agora vamos trabalhar com o código da aplicação.

1. Clone o repositório da aplicação:
```bash
git clone https://github.com/docker/getting-started-app.git
```

2. Entre no diretório:
```bash
cd getting-started-app
```

3. Crie o arquivo Dockerfile:
```bash
nano Dockerfile
```

4. Salve o conteúdo:
```yaml
FROM node:18-alpine
WORKDIR /app
COPY package.json yarn.lock* ./
RUN yarn install --production && yarn add uuid@8
COPY . .
EXPOSE 3000
CMD ["node", "src/index.js"]
```

---

## Construindo a imagem

Execute:

```bash
docker build -t getting-started .
```

Esse comando constrói uma imagem Docker utilizando o **Dockerfile** do projeto.

---

## Executando a nova imagem

```bash
docker run -dp 3000:3000 getting-started
```

Agora nossa aplicação está "conteinerizada"!

---

## Próximo passo

Agora vamos compartilhar a imagem utilizando o Docker Hub.

➡ Continue para [**04-share-app.md**](04-share-app.md)
