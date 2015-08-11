---
title: Gerenciador de pacotes para Windows
author: Adler Medrado
layout: post
permalink: /2014/08/gerenciador-de-pacotes-para-windows/
dsq_thread_id:
  - 3259646105
categories:
  - Windows
tags:
  - chocolatey
  - dicas
  - tips
  - windows
---
Não é segredo que nos últimos meses eu tenho usado [Windows][1] como a minha
principal plataforma de trabalho, apesar de lidar com servidores linux
diariamente e também usar VMs linux como ambiente de trabalho em alguns projetos.

Como estou acostumado a trabalhar com diversas ferramentas comuns em ambientes
*nix* eu sempre busco por alternativas similares para a plataforma Windows e
hoje eu irei demonstrar rapidamente o [chocolatey][2], que é um gerenciador de
pacotes similar ao apt-get no linux, só que para windows.

Para instalar, basta abrir uma janela do
<a href="http://technet.microsoft.com/pt-br/library/bb978526.aspx">Powershell</a>
em modo administrador e digitar:
<pre>
iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))
</pre>

Após a instalação, o comando <em>choco</em> será disponibilizado no sistema,
e a partir daí diversas aplicações poderão ser instaladas (e desinstaladas se
for o caso) via linha de comando.

Os comandos básicos são:

*list*
<pre>choco list</pre>

Exemplo: Listar todos pacotes que possuem <em>git</em> no nome

<pre>choco list git</pre>

*update*

Ex: Atualiza todos os pacotes

<pre>choco update</pre>

Ex: Atualiza pacote específico

<pre>choco update git</pre>

*uninstall*

<pre>choco uninstall git</pre>

*help*

<pre>choco /?</pre>

É isso. Mais uma <em>hidden gem</em> do mundo windows que até pouco tempo atrás
eu não conhecia.

Para conhecer melhor, visite a <a href="https://github.com/chocolatey/chocolatey/wiki">documentação do projeto</a>.

[1]: http://windows.microsoft.com/pt-br/windows/home
[2]: https://chocolatey.org/
