# 1 - Introdução ao Workshop

Este tutorial apresenta os conceitos básicos do Docker através da criação
e execução de uma aplicação simples dentro de um container.

A ideia do workshop é aprender Docker de forma prática, executando comandos
reais e entendendo os conceitos fundamentais da tecnologia.

----------------------------------------------------

O que você vai aprender

Ao longo deste tutorial você irá aprender:

• O que são containers  
• Como executar aplicações usando Docker  
• Como construir imagens Docker  
• Como compartilhar imagens  
• Como persistir dados em containers  
• Como executar aplicações com múltiplos containers  

----------------------------------------------------

O que é Docker?

Docker é uma plataforma que permite empacotar aplicações junto com todas
as suas dependências em unidades chamadas **containers**.

Esses containers podem ser executados em qualquer ambiente que tenha Docker,
garantindo que a aplicação funcione da mesma forma em:

• máquina local  
• servidores  
• ambientes de cloud  
• pipelines de CI/CD  

Isso resolve o famoso problema:

"Funciona na minha máquina."

----------------------------------------------------

O que é um Container?

Um **container** é um ambiente isolado que contém:

• aplicação  
• bibliotecas  
• dependências  
• configurações necessárias para execução

Containers são:

• leves  
• rápidos de iniciar  
• portáveis  
• reproduzíveis

----------------------------------------------------

O que é uma Imagem Docker?

Uma **imagem Docker** é o modelo usado para criar containers.

Podemos pensar da seguinte forma:

Imagem Docker  →  Receita  
Container      →  Instância executando

Ou seja:

Uma imagem pode gerar vários containers.

----------------------------------------------------

Fluxo básico do Docker

Normalmente o fluxo de trabalho com Docker é:

1. Criar ou obter uma imagem Docker
2. Executar um container baseado nessa imagem
3. Interagir com a aplicação dentro do container

Durante este workshop você irá seguir exatamente esse fluxo.

----------------------------------------------------

Próximo passo

No próximo capítulo iremos executar nossa primeira aplicação
utilizando Docker.