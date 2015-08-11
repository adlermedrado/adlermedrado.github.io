---
title: Introdução a Criptografia – Parte 2
author: Adler Medrado
layout: post
permalink: /2014/12/introducao-a-criptografia-parte-2/
dsq_thread_id:
  - 3805468776
categories:
  - Criptografia
  - Segurança
  - Tutorial
tags:
  - criptografia
  - dicas
  - segurança
---
Como eu havia prometido, continuo com a série de posts sobre criptografia,
se você chegou aqui sem ter visto a parte 1, sugiro que comece lendo por [aqui][1].

# Introdução

<center>
<img src="/media/uploads/2014/12/public-and-private-keys.jpg" alt="Public and Private Keys" />
</center>

Atualmente as duas formas mais comuns de criptografia são a **simétrica** e
a **assimétrica**, fique tranquilo pois apesar dos nomes intimidarem são dois
conceitos bem simples de serem compreendidos.

# Criptografia Simétrica

A criptografia é feita usando a mesma chave para criptografar e descriptografar
a informação, similar ao que foi mostrado na primeira parte deste tutorial.

Uma analogia clássica usada para ilustrar esta abordagem é o da chave da casa,
que é usada tanto para abrir quanto para trancar uma porta.

Esta forma exige menos poder computacional para criptografar e descriptografar
a informação, entretanto ela é mais sujeita a falhas na manipulação e proteção da chave.

# Criptografia Assimétrica

Esta abordagem é mais segura pois envolve um par de chaves ao invés de apenas uma.
Este par de chaves é composto pela chave pública e pela chave privada, uma para
criptografar e outra para descriptografar.

A chave pública pode ser disponibilizada ao público em geral, pois ela só pode
ser usada para criptografar uma informação cujo destinatário é quem possui a
chave privada que forma o par com esta pública.

Vamos imaginar a seguinte situação:

* José possui um par de chaves pública e privada;
* Maria também possui um par de chaves pública e privada;
* Ambos disponibilizaram entre si suas chaves públicas;

Ficou claro que cada ator neste cenário possui um par de chaves, cada uma usada
para seu propósito, criptografar e descriptografar.

Vamos continuar:

* José quer mandar uma mensagem criptografada para a Maria;
* José possui a chave pública da Maria, então ele escreve sua mensagem e
**usando a chave pública dela** ele a criptografa;
* A partir deste ponto, nem José pode mais descriptografar esta mensagem;
* José envia a mensagem criptografada para Maria através da internet (e-mail por exemplo);
* Maria recebe a mensagem;
* Maria usa a **sua chave privada** para **descriptografar** a mensagem;
* Maria lê a mensagem original;

Presumo que o exemplo ficou claro: José escreveu uma mensagem e a criptografou
usando a chave pública da Maria e como somente a Maria possui a chave privada
dela, somente ela pode descriptografar esta mensagem.

Mas e se a Maria quiser responder a mensagem para o José? Vamos continuar usando a imaginação:

* Maria recebeu a mensagem e deseja respondê-la e criptografá-la para José;
* Maria possui a chave pública do José;
* Maria escreve a mensagem e em seguida a criptografa usando a chave pública do José;
* Maria envia a mensagem criptografada para o José usando a internet (via e-mail por exemplo);
* José recebe a mensagem e usando a sua chave privada ele a descriptografa;
* José lê a mensagem enviada por Maria;

Nos dois casos, sempre o remetente utiliza a chave pública do destinatário para
criptografar a informação e o destinatário utiliza a sua chave privada para descriptografa-la.

# Considerações Finais

Espero que o conceito de chaves públicas e privadas tenha ficado claro, pois na
próxima parte eu ensinarei a configurar o ambiente necessário para poder criar
(manter em geral) chaves, criptografar e descriptografar arquivos e enviar
e-mails criptografados diretamente do cliente de e-mail.

Até lá.

[1]: http://blog.adlermedrado.com.br/2014/12/introducao-a-criptografia-parte-1/
