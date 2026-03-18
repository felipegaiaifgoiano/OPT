# Executando a aplicação

**Progresso do tutorial:** 2 / 8

[🏠 Início](../README.md) | [◀ Anterior](01-workshop.md) | [Próximo ▶](03-update-app.md)

Agora vamos executar uma aplicação utilizando Docker.

Execute o seguinte comando:
```bash
docker run -dp 80:80 docker/getting-started
```

---

## Explicação do comando

 ```docker run```: cria e executa um container.

```-d```: executa o container em segundo plano (detached mode).

```-p 80:80```: mapeia a porta 80 do container para a porta 80 da máquina local.

Se a imagem **docker/getting-started** não existir localmente, o Docker irá baixá-la automaticamente.

---

## Acessando a aplicação

Abra o navegador e acesse:

http://localhost:80

Você deverá ver a aplicação funcionando.

---

## Listando containers

Para verificar containers em execução:
```bash
docker ps
```

---

## Observação

Neste passo utilizamos uma **imagem pronta disponibilizada pela Docker**.

Nos próximos passos iremos **trabalhar diretamente com o código da aplicação**, construindo nossa própria imagem Docker.

---

## Próximo passo

Agora vamos baixar o código da aplicação e construir nossa própria imagem.

➡ Continue para [**03-update-app.md**](03-update-app.md)
