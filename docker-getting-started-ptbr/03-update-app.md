# 3 - Atualizando a aplicação

Agora que já executamos a aplicação dentro de um container,
vamos aprender como atualizar a aplicação.

No Docker, quando o código da aplicação muda, precisamos
reconstruir a imagem Docker.

----------------------------------------------------

O que é um Dockerfile?

O Dockerfile é um arquivo que descreve como construir
uma imagem Docker.

Ele contém instruções como:

• qual sistema base usar
• quais dependências instalar
• quais arquivos copiar
• qual comando executar

Exemplo simplificado:

FROM node:18
WORKDIR /app
COPY . .
RUN npm install
CMD ["node", "src/index.js"]

Esse arquivo diz ao Docker como criar a imagem da aplicação.

----------------------------------------------------

Construindo uma imagem

Para construir a imagem da aplicação usamos o comando:

docker build -t getting-started .

Explicação:

docker build

comando usado para construir uma imagem Docker.

----------------------------------------------------

Parâmetro -t

-t significa "tag".

Ele define o nome da imagem criada.

Neste caso:

getting-started

----------------------------------------------------

O ponto final (.)

O ponto indica que o Docker deve usar
o diretório atual como contexto de build.

Ou seja, todos os arquivos da aplicação
serão enviados para o processo de build.

----------------------------------------------------

Executando a nova versão

Depois de construir a imagem, precisamos executar
um novo container com essa imagem.

docker run -dp 3000:3000 getting-started

Isso iniciará um container usando a imagem que
acabamos de criar.

----------------------------------------------------

Removendo containers antigos

Se já existir um container rodando na mesma porta,
precisamos parar e remover o container antigo.

Primeiro liste os containers:

docker ps

Depois pare o container:

docker stop CONTAINER_ID

E remova:

docker rm CONTAINER_ID

----------------------------------------------------

Resumo

Neste passo você aprendeu:

• o que é um Dockerfile
• como construir imagens Docker
• como executar containers a partir de imagens próprias
• como atualizar uma aplicação containerizada

No próximo passo vamos aprender como compartilhar
imagens usando o Docker Hub.