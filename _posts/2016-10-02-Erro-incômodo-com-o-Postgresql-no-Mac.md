---
title: Erro incômodo com PostgreSQL no Mac.
author: Adler Medrado
layout: post
permalink: /2016/10/erro-incomodo-com-postgresql-no-mac/
categories:
  - General
---
=====================================



Esse é um post bem curto que resolvi escrever depois de me incomodar com
um erro esquisito no Postgresql no Mac após a atualização para o…









------------------------------------------------------------------------







### Erro incômodo com o Postgresql no Mac 

Esse é um post bem curto que resolvi escrever depois de me incomodar com
um erro esquisito no Postgresql no Mac após a atualização para o MacOS
Sierra.

O servidor do Postgresql estava funcionando OK mas o client cli me
retorna o erro abaixo sempre que eu o executava:







![](https://cdn-images-1.medium.com/max/1600/1*nKXkh2PzTW85hhl59x3-3w.png)



WTF?
Eu costumo usar o *homebrew* para instalar a maioria das coisas no meu
mac, primeiramente eu pensei que fosse algum problema com algum link
simbólico incorreto, então eu executei o comando abaixo para ver se
resolvia:







![](https://cdn-images-1.medium.com/max/1600/1*aOcgI9fU746SkcSacFKqNA.png)



Recriando os links
Mesmo assim o erro persistu, então eu removi o readline e reinstalei:







![](https://cdn-images-1.medium.com/max/1600/1*mpcBc2Tu-ShIzR770ebQrg.png)



Reinstalando …
Mas nada. :(

Tentei reinstalar forçando o *build from source*:







![](https://cdn-images-1.medium.com/max/1600/1*eLE49JvI5vtL6ieIYF_eyQ.png)



Nessa hora eu já tava ficando puto
E nada … resolvi então chutar o balde o reinstalar o PostgreSQL:







![](https://cdn-images-1.medium.com/max/1600/1*n7GMinuLwIcIqldxekZb8w.png)



Reinstalando a porra toda
E funcionou. :)







![](https://cdn-images-1.medium.com/max/1600/1*qUqQk3QyIsE0YejWnjO9CA.png)



Tcham :)
Fica a dica para quem estiver passando pelo mesmo problema que eu.

Acredito que na atualização do sistema operacional alguma lib ficou
desatualizada o que gerou este problema. Em outros tempos não muito
distantes, eu teria feito uma instalação limpa do sistema todo, ainda
bem que hoje eu estou aprendendo a lidar de forma diferente com este
tipo de problema.













