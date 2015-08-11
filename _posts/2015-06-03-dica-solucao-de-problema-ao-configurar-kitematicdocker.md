---
title: 'Dica: Solução de problema ao configurar Kitematic/Docker'
author: Adler Medrado
layout: post
permalink: /2015/06/dica-solucao-de-problema-ao-configurar-kitematicdocker/
categories:
  - Ambiente
  - Mac
tags:
  - dicas
  - docker
  - kitematic
  - mac
  - virtualizacao
---
**Este é o tipo de post que eu escrevo para servir de referência futura mas que também pode acabar ajudando outras pessoas.**

Um projeto que estou trabalhando usa o [RabbitMQ][1] e para tentar manter o meu
OS X o mais higienizado possível e também para manter a uniformidade entre o meu
ambiente e os demais envolvidos no projeto, nós decidimos utilizar o [Docker][2]
e um container do RabbitMQ.  

Para facilitar, existe um projeto chamado [Kitematic][3] que auxilia na
configuração do Docker e na instalação de containers, entretanto, o Kitematic
está em versão beta ainda e por isso ele possui algumas arestas que precisam ser
aparadas, mas no geral ele funciona bem.

### Problema na instalação

Na hora em que o Kitematic é instalado ele verifica se o Virtualbox está
instalado no computador, caso não esteja, ele baixa e faz a instalação
automaticamente, após isso prossegue com a instalação, mas quando chegou em 99%
ele ficou parado e não avançou mais, conforme a imagem abaixo:

<img src="/media/uploads/2015/06/kitematic_erro_ao_instalar.png" alt="Kitematic erro ao instalar"/>

Eu quase desisti após xingar bastante, mas então eu executei os seguintes
comandos no terminal:

```docker-machine rm -f dev```

```docker-machine create -d virtualbox dev```

E tudo passou a funcionar corretamente.

Durante o período em que eu esperava a instalação finalizar, eu abri uma issue
no [Github do projeto][4] e em seguida ao conseguir resolver eu postei a solução
na [própria issue][5] e a fechei, como o projeto ainda está na fase beta é normal
ter problemas e aparentemente os desenvolvedores já estão cientes deste.

<img src="/media/uploads/2015/06/github_issue_kitematic.png" alt="Github Issue Kitematic"/>

[1]: https://www.rabbitmq.com
[2]: https://www.docker.com/
[3]: https://kitematic.com/
[4]: https://github.com/kitematic/kitematic
[5]: https://github.com/kitematic/kitematic/issues/585
