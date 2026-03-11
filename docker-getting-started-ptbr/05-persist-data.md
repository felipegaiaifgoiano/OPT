# 5 - Persistindo dados

Até agora executamos containers que funcionam corretamente,
mas existe um problema importante.

Containers são **efêmeros**.

Isso significa que, quando um container é removido, todos
os dados armazenados dentro dele também são perdidos.

Para resolver isso utilizamos **volumes Docker**.

----------------------------------------------------

O que é um volume?

Um volume é um mecanismo que permite armazenar dados
fora do container.

Assim, mesmo que o container seja removido ou recriado,
os dados permanecem disponíveis.

----------------------------------------------------

Criando um volume

Para criar um volume execute:

docker volume create todo-db

Esse comando cria um volume chamado:

todo-db

----------------------------------------------------

Usando o volume em um container

Agora podemos executar o container usando esse volume.

docker run -dp 3000:3000 -v todo-db:/etc/todos getting-started

----------------------------------------------------

Explicação do parâmetro -v

-v significa "volume".

Estrutura do comando:

nome-do-volume : caminho-no-container

No nosso exemplo:

todo-db:/etc/todos

Isso significa:

volume "todo-db" → diretório /etc/todos dentro do container

----------------------------------------------------

Como isso ajuda?

Agora, quando a aplicação salvar dados no diretório:

/etc/todos

eles serão armazenados no volume Docker.

Mesmo que o container seja removido, os dados continuarão
existindo no volume.

----------------------------------------------------

Listando volumes

Para ver os volumes existentes execute:

docker volume ls

----------------------------------------------------

Inspecionando um volume

Para ver detalhes de um volume:

docker volume inspect todo-db

----------------------------------------------------

Resumo

Neste passo você aprendeu:

• por que containers são efêmeros  
• o que são volumes Docker  
• como criar volumes  
• como montar volumes em containers  

No próximo passo vamos aprender sobre **bind mounts**,
uma outra forma de compartilhar dados entre host e container.