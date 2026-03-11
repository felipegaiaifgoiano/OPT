# 2 - Executando nossa primeira aplicação

Agora vamos executar uma aplicação real usando Docker.

A Docker mantém várias imagens públicas que podem ser executadas
diretamente a partir do Docker Hub.

Neste tutorial utilizaremos uma aplicação de exemplo chamada:

docker/getting-started

----------------------------------------------------

Executando o container

Execute o seguinte comando no terminal:

docker run -dp 3000:3000 docker/getting-started

Vamos entender cada parte desse comando.

----------------------------------------------------

Explicação do comando

docker run

Este comando cria e executa um container baseado em uma imagem Docker.

----------------------------------------------------

Parâmetro -d

-d significa "detached mode".

Isso faz com que o container seja executado em segundo plano.

Sem esse parâmetro, o container rodaria no terminal atual.

----------------------------------------------------

Parâmetro -p

-p significa "port mapping".

Neste caso:

3000:3000

Isso significa:

porta_do_host : porta_do_container

Ou seja, estamos dizendo que:

porta 3000 da máquina local → porta 3000 do container

----------------------------------------------------

Imagem utilizada

docker/getting-started

Essa é a imagem da aplicação que estamos executando.

Se ela não existir localmente, o Docker irá automaticamente
baixá-la do Docker Hub.

----------------------------------------------------

Acessando a aplicação

Após executar o comando, abra o navegador e acesse:

http://localhost:3000

Se tudo estiver funcionando corretamente, você verá a aplicação
rodando no navegador.

----------------------------------------------------

Verificando containers em execução

Para listar os containers ativos, execute:

docker ps

Este comando mostra:

• ID do container
• imagem utilizada
• portas
• status de execução

----------------------------------------------------

Parando o container

Para parar um container você pode usar:

docker stop CONTAINER_ID

O CONTAINER_ID pode ser obtido usando o comando:

docker ps

----------------------------------------------------

Resumo

Neste passo você aprendeu:

• Como executar um container
• Como mapear portas
• Como acessar uma aplicação dentro de um container
• Como listar containers em execução

No próximo passo vamos modificar a aplicação e
reconstruir a imagem Docker.