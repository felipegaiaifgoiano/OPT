# Executando a aplicação

**Progresso do tutorial:** 2 / 8

[🏠 Início](../README.md) | [◀ Anterior](01-workshop.md) | [Próximo ▶](03-update-app.md)

Agora vamos executar uma aplicação utilizando Docker.

Execute o seguinte comando:

docker run -dp 3000:3000 docker/getting-started

---

## Explicação do comando

docker run  
Cria e executa um container.

-d  
Executa o container em segundo plano (detached mode).

-p 3000:3000  
Mapeia a porta 3000 do container para a porta 3000 da máquina local.

Se a imagem **docker/getting-started** não existir localmente, o Docker irá baixá-la automaticamente.

---

## Acessando a aplicação

Abra o navegador e acesse:

http://localhost:3000

Você deverá ver a aplicação funcionando.

---

## Listando containers

Para verificar containers em execução:

docker ps

---

## Observação

Neste passo utilizamos uma **imagem pronta disponibilizada pela Docker**.

Nos próximos passos iremos **trabalhar diretamente com o código da aplicação**, construindo nossa própria imagem Docker.

---

## Próximo passo

Agora vamos baixar o código da aplicação e construir nossa própria imagem.

➡ Continue para [**03-update-app.md**](03-update-app.md)
