---
title: Configurando um repositório privado usando Composer e Satis
author: Adler Medrado
layout: post
permalink: /2015/06/configurando-um-repositorio-privado-usando-composer-e-satis/
categories:
  - Ambiente
  - Tutorial
tags:
  - ambiente
  - composer
  - packagist
  - php
  - satis
  - tutorial
---
Recentemente eu precisei incluir um repositório do Git cujo acesso é privado em
um projeto que estou trabalhando na [Coderockr][1] e este repositório deveria ser
importado no projeto por meio do composer, talvez isso não seja novidade para você,
mas, para mim é pelo fato de eu nunca ter precisado criar um ambiente acessível
pelo [composer][2] que utilizasse um repositório git privado.

### Como faz?

Após algumas pesquisas eu encontrei o projeto [Satis][3], que pelo que pude
compreender é mantido pelos mesmos desenvolvedores que mantém o composer.

O uso dele é bem simples e eu tentarei descrever os passos de uma forma bem
simples e objetiva:

#### Instale o Composer

Se ainda não o tiver feito, [(aprenda como)][4].

#### Instale o Satis

Crie um projeto usando o composer, basta rodar o seguinte comando no terminal:

<pre>php composer.phar create-project composer/satis --stability=dev --keep-vcs</pre>

#### Configure-o para prover o acesso ao seu repositório privado

A primeira coisa que deve ser feita é criar um arquivo chamado satis.json no
root do projeto que foi criado acima, segue um exemplo deste arqvivo:

<pre>{
    "name": "Repositório Local",
    "homepage": "http://localhost:8888",
    "archive": {
            "skip-dev": true
    },
    "repositories": [
        { "type": "vcs", "url": "https://url-para-seu-repositorio-git/nome-do-seu-repositorio.git" }
    ],
    "require": {
        "seu-pacote/sua-lib": "*"
    }
}</pre>

Como pode ser observado acima, eu configuro com o repositório que eu quero
disponibilizar, se precisar colocar mais do que um repositório basta adicionar
woutro elemento no array *repositories*.

Em seguida, informe o nome do seu pacote/library e qual versão deseja usar.

Acima, no atributo homepage é informado qual o endereço local que será usado para servir o projeto. Você pode usar uma URL diferente de localhost sem problemas.

#### Faça a *build* do seu repositório

Execute o comando abaixo sempre que houver mudanças no seu repositório:

<pre>php bin/satis build &lt;configuration file> &lt;build dir></pre>

Por exemplo, eu rodei assim:

<pre>php bin/satis build satis.json repo</pre>

O diretório repo será usado para disponibilizar os fontes do repositório privado.

#### Disponibilize o repositório

Você pode criar um virtual host apontando para o diretório *repo*, mas dependendo do caso, usar o webserver embutido no CLI do PHP:

<pre>php -S 0.0.0.0:8888 -t repo</pre>

Após rodar o comando acima (ou configurar um virtual host), acesse: **http://localhost:8888**

Se for mostrada uma tela com os repositórios que você configurou eles poderão ser usados adicionando no composer.json do seu projeto:

<pre>"repositories": [
    {
      "type": "composer",
      "url": "http://localhost:8888"
    }
  ],
  "require": {
    "seu-pacote/sua-lib": "dev-master"
  }</pre>

#### Conclusão

Existem muitas outras configurações que podem ser feitas, mas essa configuração básica já ajuda na maioria das situações.

Você conhece alguma outra maneira de lidar com uma situação como essa? Deixe seu comentário.

 [1]: http://coderockr.com
 [2]: https://getcomposer.org
 [3]: https://github.com/composer/satis
 [4]: https://getcomposer.org/doc/00-intro.md
