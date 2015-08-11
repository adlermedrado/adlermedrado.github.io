---
layout: post
title: "Migrando para o Atom"
date: "2015-07-31"
---
Na primeira vez em que tive um Mac, um dos primeiros softwares que comprei
foi o Textmate.

![Textmate Logo](/media/textmate.png)

Na época ele era o editor de textos predileto dos desenvolvedores
e realmente ele era muito bom, tão bom que eu ainda usava ele até o início
desta semana, quando eu passei a ter alguns problemas principalmente
com bundles dele como o de ctags e quando eu busquei solução para eles eu
percebi que muitos dos bundles que eu usava, hoje não possuem mais suporte
porque os autores deixaram de usar o Textmate.

É compreensível, afinal de contas o desenvolvimento do Textmate ficou stagnado e
nesse meio tempo surgiram outros editores excelentes como por exemplo o Sublime
Text para suprir as necessidades dos usuários e com isso muitos desenvolvedores
de bundles acabaram migrando de plataforma também.

> Para ter uma idéia, tem bundle que não sofre atualizações a 4, 5 anos...

Eu pessoalmente gostaria de ter tempo de adotar alguns projetos desses bundles
e continuar mantendo, mas é bem difícil fazer isso principalmente porque a base
de usuários já não compensa tanto o esforço, um exemplo disso é que eu pedi
ajuda na lista de usuários do Textmate com um problema que eu tive e simplesmente
não tive resposta, o que demonstra que apesar de tudo, apesar de ser uma
excelente plataforma, o Textmate é um projeto em fase terminal.

Na verdade eu até tentei resolver o problema do bundle do Ctags mas não consegui
porque uma das dependências do projeto estava em formato binário e apesar de ser
um bundle open-source, os fontes para este binário, *que é parte crucial do bundle*,
estavam indisponíveis.

###Atom

![Textmate Logo](/media/atom.jpg)

Apesar de meu primeiro contato com o Atom não ter sido agradável, eu resolvi dar
uma nova chance a ele, me lembro que a impressão que tive quando o usei pela
primeira vez era a de que ele era um *mastodonte* de tão lento e tinha um tracking
code do analytics embutido que me incomodava, mas, hoje a situação é bem diferente.

Eu instalei alguns plugins os quais listarei a seguir que me auxiliam bastante
no dia-a-dia:

* Sublime-Style-Column-Selection

Basicamente, o _package_ "Sublime-Style-Column-Selection" permite fazer seleção
em colunas igual no Sublime Text, essa pelo menos é a descrição do pacote, mas
se levarmos em conta que o Sublime copiou o Textmate, ele implementa a seleção
em colunas do Textmate no Atom. Recomendo.

* atom-beautify

Dá uma ajeitada em código que ficou com indentação bagunçada, o que é muito
comum quando trabalhamos em código legado.

* atom-fuzzy-grep

Busca por arquivos usando ferramentas como grep, ack, etc. Por padrão, quando
é detectado que está sendo usado o Git, ele usa o git grep.

* autocomplete-ctags

Utiliza os índices gerados pelo ctag para fazer autocomplete.

* autocomplete-php

O nome já é auto-explicativo.

* ctags-status

Mostra na barra do rodapé detalhes do símbolo em questão, por exemplo: "Tal método
é de tal Classe".

* git-diff-details
* merge-conflicts

Git Diff e Merge usando o Atom.

* git-plus

Permite executar comandos do Git de dentro do Atom.

* jekyll

Disponibiliza comandos para usar o Jekyll de dentro do Atom.

* linter
* linter-php

Checa em tempo de digitação se há erro na sintaxe do código.

* markdown-writer

Melhora o suporte ao Markdown do Atom.

Além dos _packages_ que ele já tem, o visual dele é bem melhor, a quantidade de
temas disponíveis é muito grande e sinceramente, é agradavel trabalhar usando
uma ferramenta tão bonita :).

### O que eu sinto falta

* rmate

No textmate nós temos o rmate, que é um script ruby que permite editar arquivos
remotos via SSH, localmente no Textmate. É uma mão na roda, mas eu acho que
consigo conviver sem isso.

* Blogging

Apesar de não estar usando mais wordpress, este era um bundle excelente que
permitir blogar no wordpress e outros mecanismos de blogging, usando somente
o Textmate. Não uso mais para meu site pessoal, mas tenho clientes que usam
e ele me quebrava um galho, mas como no exemplo anterior, eu consigo viver sem
isso.


### Por que não usar o Sublime Text?

Simples, apesar se ele ser excelente, afinal é uma cópia turbinada do Textmate,
ele vai, em minha opinião, sofrer do mesmo mal que o Textmate e pelos mesmos
motivos: O desenvolvimento dele é artesanal, está na mão de poucos desenvolvedores,
o código é fechado e por isso a evolução da plataforma é lenta.

Por mais que ele seja bom, vai chegar uma hora em que os usuários vão sentir
falta de algumas funcionalidades e buscarão outras alternativas.

Alguns desses usuários, da mesma forma como eu fiz com o Textmate, ficarão com ele
até não terem mais escolha e se obrigarão a escolher outra opção e quando o(s)
dono(s) do Sublime Text perceberem que estão perdendo sua base de usuários e
tentarem reverter a situação e tornarem o projeto open-source, será tarde demais.

Posso estar errado, mas o cenário é o mesmo e tem todos os requisitos para que
a história se repita.

### Considerações finais

![Atom screen](/media/screenshot-atom.png)

O Atom ainda tem deficiências, ele é mais lento que o Sublime e Textmate, ele
as vezes ainda sofre alguns crashes, mas pelo que tenho usado eu estou gostando
e se levarmos em consideração que ele já é open-source, a comunidade dele é grande
e ativa, ele é mantido por uma grande empresa (Github) e players do mercado do
status do Facebook estão o utilizando, é provável que com o passar do tempo ele
melhore (óbvio) e se torne um padrão de mercado.

Estou apostando nisso, posso estar errado como estive quando apostei no Textmate,
pois pensei que ele duraria muito mais do que ele durou, mas hoje ele é um zumbi
que a qualquer momento tomará o tiro de misericórdia na cabeça, é triste dizer
isso, mas é a verdade e tudo indica que o Atom, se continuar recebendo o apoio
que recebe tanto da comunidade quanto do Github, terá muito tempo de vida.

Enquanto isso vou ficando com o Atom, por enquanto a lua de mel está indo a todo
vapor e espero que continue assim.

Você tem alguma preferência a respeito de editores? Deixe seu comentário.
