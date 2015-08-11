---
title: Por que é importante criptografar seus dados e o que pode ser aprendido com o caso Sony
author: Adler Medrado
layout: post
permalink: /2014/12/por-que-e-importante-criptografar-seus-dados-e-o-que-pode-ser-aprendido-com-o-caso-sony/
categories:
  - Cracking
  - Criptografia
  - Política
  - Segurança
tags:
  - cracking
  - criptografia
  - invasão
  - segurança
  - sony
---
Se você não estava em uma caverna, provavelmente assistiu, leu ou ouviu sobre o
caso de cracking e vazamento de dados da Sony Pictures Entertainment, onde um
grupo de crackers (provavelmente norte-coreanos) invadiram os computadores dela
e obtiveram dados sigilosos como informações a respeito de futuros lançamentos
e conversas via e-mail de executivos da empresa.

Basicamente, estes criminosos estão ameaçando a empresa dizendo que vazarão
dados sigilosos dela ao mundo caso suas demandas não sejam atendidas, além de
tornar públicas informações como os salários de executivos da empresa, números
do seguro social de funcionários da empresa, incluindo celebridades.

Não vou falar muito sobre o caso em si porque uma simples busca fornece tudo
com detalhes a respeito do ataque, eu quero apenas aproveitar a ocasião para
perguntar: **Será que dados sigilosos como esses estavam descriptografados?**

## Parece amadorismo

Eu posso estar enganado, mas eu sou livre para pensar: **Acho que eles foram
amadores e deixavam tudo descriptografado**.

Conversando na lista do [Área 31 Hackerspace][1], um colega fez as seguintes
perguntas:

* Por que uma empresa bilionária usava certificados &#8220;self signed&#8221;
vencidos desde 2012.
* Por que uma empresa bilionária usava alguns certificados reais de empresas
certificadoras que foram invadidas e os mesmos certificados estão revogados
desde 2013 por causa das invasões.
* Quem deu os nomes dos servidores e o range da rede?

<img src="/media/uploads/2014/12/N7OJVxB-300x225.jpg" alt="Wat" />

## Adotar o uso sistemático de criptografia poderia diminuir os prejuízos

Eu não conheço nada da infra-estrutura deles, mas mesmo com o meu modesto
jeito de ser eu arrisco a dizer que o simples e sistemático uso de [OpenPGP][3]
poderia ter evitado o estrago que essas invasões causaram, bem como eliminar
muitas das ameaças e chantagens que hoje a Sony Pictures está sofrendo,
sem falar no abalo do relacionamento entre os executivos da empresa com as
celebridades que eles atacavam sem dó nos e-mails que trocavam entre si.

Utilizar volumes criptografados para guardar as informações sigilosas também é
algo que poderia ser considerado para evitar vazamentos em caso de invasão.

## Resumindo &#8230;

A falta de cuidado da Sony custará caro, que este caso fique como uma lição
aprendida e as empresas passem a levar a sério o uso da criptografia em seu
dia-a-dia, não apenas as empresas grandes, mas qualquer empresa hoje em dia
está sujeita a passar por situações complicados causadas pela incapacidade de
proteger suas informações.

Eu gostaria de saber sua opinião, deixe-a nos comentários.

[1]: http://area31.net.br
[2]: http://i2.wp.com/blog.adlermedrado.com.br/wp-content/uploads/2014/12/N7OJVxB.jpg
[3]: http://pt.wikipedia.org/wiki/OpenPGP
