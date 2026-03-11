# 4 - Compartilhando a aplicação

Depois de construir uma imagem Docker, muitas vezes queremos
compartilhá-la com outras pessoas ou utilizá-la em outros ambientes.

Para isso utilizamos um **registry de imagens**.

O registry mais comum é o Docker Hub.

----------------------------------------------------

O que é o Docker Hub?

Docker Hub é um serviço online que permite:

• armazenar imagens Docker  
• compartilhar imagens  
• baixar imagens públicas  
• versionar imagens  

Ele funciona de forma semelhante ao GitHub,
mas para imagens Docker.

----------------------------------------------------

Criando uma conta

Caso ainda não tenha conta, crie uma em:

https://hub.docker.com/

Depois faça login pelo terminal.

----------------------------------------------------

Login no Docker Hub

Execute:

docker login

O terminal solicitará:

username  
password  

Após autenticação, você poderá enviar imagens para sua conta.

----------------------------------------------------

Nomeando corretamente a imagem

Antes de enviar uma imagem para o Docker Hub,
ela precisa seguir o padrão:

usuario/nome-da-imagem

Exemplo:

felipe/getting-started

Para renomear a imagem utilizamos o comando:

docker tag getting-started SEU_USUARIO/getting-started

----------------------------------------------------

Enviando a imagem

Agora podemos enviar a imagem para o Docker Hub:

docker push SEU_USUARIO/getting-started

O Docker enviará todas as camadas da imagem para o registry.

----------------------------------------------------

Baixando a imagem em outro computador

Qualquer pessoa (ou servidor) pode executar essa imagem usando:

docker run -dp 3000:3000 SEU_USUARIO/getting-started

Se a imagem não existir localmente, o Docker irá baixá-la automaticamente.

----------------------------------------------------

Resumo

Neste passo você aprendeu:

• o que é um registry de containers  
• como utilizar o Docker Hub  
• como autenticar no Docker Hub  
• como enviar imagens usando docker push  

No próximo passo vamos aprender como **persistir dados
em containers Docker**.