---
title: Web Analytics e Privacidade
author: Adler Medrado
layout: post
permalink: /2013/09/web-analytics-e-privacidade/
categories:
  - General
---
## Intro

Recentemente, eu publiquei um post a respeito do meu novo blog, aproveitando
o embalo eu estou tentando torna-lo o mais transparente possível para aqueles
que o visitam, então a primeira iniciativa foi **descartar o uso do Google Analytics**.

<img src="/media/web-analytics-tools2.jpg" alt="Web Analytics Tools" />

### Rastreamento

Há muito tempo, bem antes desse burburinho todo por causa da NSA que eu me
preocupo com a minha privacidade na web, eu acho que comecei a me preocupar e a
me interessar por esse tipo de assunto por volta de 1998 ou 1999 quando lia
sobre echelon. Apesar de ser praticamente impossível possuir a tal da privacidade,
principalmente usando Google, Facebook, Twitter, Linkedin entre outros, não custa
nada tentar diminuir um pouco o acesso às nossas informações.

<img src="/media/banner-rastreamento-sitrace-300x184.jpg alt="rastreamento" />

Se você está por fora de como as empresas rastreiam e chegam ao ponto até de
conseguir identificar as pessoas, sugiro que dê uma [olhadinha neste site][3],
que rapidamente demonstra como as pessoas são rastreadas.

A propósito, recomendo muito o [DuckDuckGo][4] como mecanismo de busca.

### Ferramenta de web analytics

<img src="/media/piwikLogo-300x127.png" alt="piwikLogo" />

Eu sei que muitas pessoas, presumo que a maioria não se preocupa com os
rastreamentos e tal, mas em respeito a quem se preocupa, eu decidi não usar o
google analytics aqui, como mencionei acima, mas eu quero ter algumas
informações básicas a respeito dos visitantes do meu site, para que eu possa
sempre tentar melhorar o acesso a ele e me dedicar a escrever mais sobre
assuntos que despertam o interesse deles.

#### Como fazer ?

Depois de uma breve pesquisa, eu encontrei uma ferramenta chamada [Piwik][6]
e percebi que muitos a elogiavam.

Ela também é uma ferramenta open-source e é escrita em PHP, então para mim,
isso foi como unir o útil ao agradável.

Na documentação da [Piwik][6] possui uma seção voltada a
[melhorar o suporte da ferramenta no quesito privacidade][7] e eu estou tentando
 seguir todos os pontos e espero que em breve esteja tudo 100%.

#### Instalação

Eu fiz a instalação da ferramenta nos servers da Red Hat OpenShift,
sei que colocar esse tipo de informação num ambiente de cloud é meio incoerente,
mas ficará assim até eu conseguir melhorar a capacidade do meu servidor ou até
mesmo contratar um VPS só para esse fim.

A instalação no OpenShift foi bem tranquila e estou preparando um post sobre isso.

#### Monetização

Eu não estou usando o Google Adsense para monetizar o site pois seria incoerente,
então eu pensei em usar o boobox pois pesquisei e não encontrei queixas a
eles no que diz respeito á privacidade, no entanto eu gostaria de saber
sua opinião caso esta empresa também utilize de artifícios parecidos com o do google.

#### Considerações Finais

Como dizia o trio parada dura, na música “As Andorinhas”, “Uma andorinha
voando sozinha não faz verão”, mas eu me sinto bem em estar tentando fazer
minha parte na defesa da privacidade online, mesmo que isso hoje em dia seja
algo praticamente impossível e porque não, até utópico.

<img src="/media/lp-vinil-trio-parada-dura-barco-de-papel_MLB-F-2936432415_072012-297x300.jpg?" alt="trio parada dura" />

Eu estou testando o Piwik e até o momento estou gostando dos resultados, mas,
posso em algum momento mudar de idéia e procurar outra solução ou até mesmo
construir a minha, mas até lá continuarei o usando e da mesma forma como no
caso do Boo-box que citei acima, se você tiver alguma informação a respeito do
Piwik no sentido que ele comprometa a privacidade, por favor, me avise.

[1]: http://i2.wp.com/adlermedrado.com.br/images/2013-09-23-web-analytics-e-privacidade/web-analytics-tools2.jpg
[2]: http://i0.wp.com/adlermedrado.com.br/images/2013-09-23-web-analytics-e-privacidade/banner-rastreamento-sitrace.jpg
[3]: http://donttrack.us/
[4]: http://duckduckgo.com
[5]: http://i1.wp.com/adlermedrado.com.br/images/2013-09-23-web-analytics-e-privacidade/piwikLogo.png
[6]: http://piwik.org/
[7]: http://piwik.org/privacy/
