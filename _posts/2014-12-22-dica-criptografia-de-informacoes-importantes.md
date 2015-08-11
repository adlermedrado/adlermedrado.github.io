---
title: 'Dica: Criptografia de informações importantes'
author: Adler Medrado
layout: post
permalink: /2014/12/dica-criptografia-de-informacoes-importantes/
categories:
  - Criptografia
  - Segurança
tags:
  - criptografia
  - dicas
  - segurança
---
<center>
<img src="/media/uploads/2014/12/safe-225x300.jpg" alt="Cofre - Safe" />
</center>

Imagine a seguinte situação: Quando você sai da sua casa você tranca as janelas,
as portas e o portão, entretanto você possui um cofre para garantir que itens
valiosos como documentos, dinheiro, jóias, etc. fiquem seguros, pois você sabe
que para abri-lo é necessário uma chave que somente você tem e um código que
somente você sabe.  

Você sabe que o cofre não garante 100% de segurança contra arrombamentos mas
tem consciência que ele dará muito mais trabalho para quem quiser roubar suas coisas.

Agora imagine a mesma situação só que a casa é seu computador e seus itens
valiosos são arquivos digitais como documentos, imagens, etc.

Só você tem a senha para *logar* em seu computador, mas você quer garantir que
caso alguém o acesse sem autorização, estes arquivos importantes não estejam
acessíveis ou na pior das hipóteses, seja muito trabalhoso para o ladrão ter
acesso a eles.

**Manjou?**

Meus próximos *posts* abordarão a [criptografia][2], e hoje eu pretendo mostrar
de maneira bem simples uma ferramenta que auxilia na tarefa de encriptação de
dados para usuários de sistemas operacionais Windows e Mac OS X.

## Safe

[Safe][3] é uma aplicação multiplataforma baseada no projeto Open-Source
[EncFS][4] que cria volumes que salvam todos os arquivos dentro deles de forma
criptografada, basicamente depois de criar uma pasta e definir uma senha a ela,
você acessa esta pasta como se fosse uma outra unidade de disco (um pen-drive
por exemplo) e os arquivos dentro desta pasta sempre que forem acessados sem a
 senha estarão encriptados impossibilitando que seu conteúdo seja interpretado.

A maior vantagem em usar o Safe em vez de truecrypt (não recomendável atualmente)
ou ferramentas como os contêineres de dados criptografados da Kaspersky é que
nestes últimos o espaço alocado para armazenar os dados criptografados
será fixo, por exemplo, se você criar uma unidade com 10GB será criado um
arquivo de 10GB independente de ter algum arquivo ou não criptografado nela,
o Safe por sua vez, criptografa os arquivos individualmente facilitando a
manipulação deles, como enviar para o dropbox por exemplo.

## Para finalizar

Agora não tem mais desculpas para você que usa Windows ou Mac OS X guardar
dados descriptografados, a ferramenta é livre ([GPLv3][5]) e fácil de usar.

Dê uma olhada no site do [Safe][3], faça o download e comece a guardar suas
informações com um pouco mais de segurança.

[1]: http://i0.wp.com/blog.adlermedrado.com.br/wp-content/uploads/2014/12/safe-e1419294796139.jpg
[2]: http://pt.wikipedia.org/wiki/Criptografia
[3]: www.getsafe.org
[4]: http://en.wikipedia.org/wiki/EncFS
[5]: https://www.gnu.org/copyleft/gpl.html
