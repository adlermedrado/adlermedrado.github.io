---
title: Meu ambiente de trabalho na plataforma Windows
author: Adler Medrado
layout: post
permalink: /2014/12/meu-ambiente-de-trabalho-na-plataforma-windows/
dsq_thread_id:
  - 3805468714
categories:
  - General
  - Windows
tags:
  - .net
  - android
  - atom
  - bitcoin
  - 'c#'
  - chocolatey
  - chrome
  - elixir
  - firefox
  - general
  - geral
  - git
  - github
  - gpodder
  - internet explorer
  - java
  - jvm
  - markdown
  - markdownpad
  - multibit
  - office
  - php
  - play
  - podcast
  - scala
  - sourcetree
  - windows
---
A cerca de um ano e alguns meses eu tenho usado a plataforma Microsoft Windows
de uma forma sistemática e eu achei interessante escrever um pouco sobre o que
eu costumo usar em meu computador.

## Multimídia

* Eu faço uso recorrente do player desktop do [Rdio][1] para ouvir música em
streaming. Este é um serviço que vale muito a pena e apesar de ver bastante
gente migrando para o Spotify eu estou feliz com o Rdio pois ele me atende bem;
* [VLC][2] &#8211; Player de vídeo open-source com suporte à maioria dos
formatos disponíveis no mercado;
* [gPodder][3] &#8211; Gerenciador de podcasts. Ele é bem simples de usar e
promete fazer sincronização dos podcasts com dispositivos móveis, no meu caso
nunca funcionou com o Android, mas eu não ligo porque faço a sincronização
manualmente mesmo. No geral é um software simples que em geral faz o que se
propõe a fazer;

## Gerenciamento de Pacotes

* [Chocolatey][4] &#8211; Tenta fazer em ambiente Windows o que o APT, Zypper,
Yum, etc., fazem em ambiente Linux. No geral ele é bom, hoje em dia não me
vejo usando o Windows sem ele. [Eu escrevi um post sobre ele algum tempo atrás][5];

## Emulador de terminal

* [Cmder][6] &#8211; Até o momento o melhor emulador de terminal para Windows
que eu já vi. Baixando o pacote completo ele já vem com Git e outras ferramentas
úteis de ambientes *nix* que o tornam além de uma opção mais atraente ao
_Prompt do DOS_ e ao _Powershell_ em uma ferramenta poderosa.
Se você gosta de usar o terminal e está usando o Windows, o Cmder é para você;

## Client de e-mail

* [Postbox][7] &#8211; Simplesmente o melhor cliente de e-mail do universo.
É baseado no Mozilla Thunderbird, ou seja, é o Thunderbird funcionando direito.
É pago mas não é caro, custa cerca de U$10 e vale cada centavo, além de suportar
a grande maioria dos plugins para o Thunderbird, alguns foram otimizados para
funcionar com ele como o Enigmail, sem falar na variedade de funcionalidades
*out of the box* que ele possui;

## Editores de texto e suíte de escritório

* [Atom][8] &#8211; Eu tenho usado o Atom em meu dia-a-dia e estou
gostando **mesmo ele sendo meio pesadinho**, mas como ele está numa fase beta
e no geral ele tem me atendido eu estou insistindo. Quando ele sair da fase beta
ele será uma ferramenta paga e eu estou considerando a hipótese de pagar por ela
dependendo do preço;</p>
* [Markdownpad][9] &#8211; Simplesmente o melhor editor Markdown para Windows.
Ele possui uma versão grátis e uma paga. Eu comprei ele por valer cada centavo.
É com ele que eu redijo os posts deste blog e
o [meu livro][10] (que espero finalizar em breve);
* [Microsoft Office][11] &#8211; É a melhor ferramenta do gênero e não adianta
me falar de LibreOffice (esse nome me dá vontade de vomitar), porque ele ainda
precisa comer muito feijão com arroz para se igualar ao seu congênere da
Microsoft, verdade seja dita;

## Ambiente de Desenvolvimento

* [Github for Windows][12] &#8211; As vezes eu o utilizo para gerir meus
repositórios no Github, apesar de estar aos poucos deixando de usa-lo para o
usar o sourcetree;
* [Sourcetree][13] &#8211; Ferramenta que facilita a gestão de repositórios
Git e Mercurial;
* [Visual Studio Community 2013][14] &#8211; Estou utilizando para estudar C#,
ASP.net MVC e ASP.net Web API;
* Para desenvolvimento [PHP][15] estou usando o Atom, mas estou realmente
considerando a compra da licença do [PHPStorm][16], que é a melhor IDE para
PHP do mercado;
* [IIS 8.0][17] e [Microsoft Web Platform Installer][18] &#8211; Eu tenho usado
este ambiente para rodar aplicações PHP e ASP.net localmente quando necessário,
eu já testei usa-lo com node.js também e aparentemente rodou suave. No caso do
PHP, eu tenho as versões do PHP 5.3,5.4,5.5 e 5.6 instaladas com ele.
* [Eclipse][19] &#8211; Para usar com Java e linguagens que rodam sob a JVM,
como Scala por exemplo, apesar de ainda não ter usado Scala e Play Framework
profissionalmente, eu tenho estudado e gostado bastante;
* Tenho estudado a linguagem [Elixir][20] e para isso tenho usado o editor
Atom também;
* Vim com o spf13-vim &#8211; Melhor distribuição do Vim que conheço e pode
ser instalada com o chocolatey usando o comando: *choco install spf13-vim*;

## Browsers

* Mozilla Firefox;
* Internet Explorer 11;
* Google Chrome;

*Estou usando nesta ordem de preferência*.

## Ambiente de Virtualização

* [Oracle Virtualbox][21];
* [Vagrant][22];

*A maioria das VMs são CentOS, mas possuo algumas Ubuntu 14.04, ambas distros
usadas com Vagrant e uma instalação desktop do CentOS com interface gráfica
para uso cotidiano*.

## Client SSH, SFTP e FTP

* [Putty][23] &#8211; Simples e objetivo, é o melhor *client* SSH que existe;
* [WinSCP][24] &#8211; Mesma coisa que o Putty, só que para SFTP e FTP
<img src="/media/images/smilies/simple-smile.png" alt=":)" />

## Criptografia

* [GPG4Win][25] &#8211; Port para Windows do GnuPG. Uso normalmente para criptografar e-mails;
* [Enigmail][26] &#8211; Plugin GPG/GnuPG para Thunderbird que uso com o Postbox;
* [Safe][27] &#8211; Ferramenta que me permite gerir volumes criptografados;

*Se quiser me mandar e-mail criptografado, minha chave pública PGP segue abaixo:*

<pre>
-----BEGIN PGP PUBLIC KEY BLOCK-----
Version: GnuPG v2

mQINBFR4VB0BEADGxlxNfeUes6JzqCpHf1ELfqcmqyhw9wOySoVTkebRTrLcLJ4T
PFjI4O/CWlO4hI7T0bKbGEqMHcmdMIVhJZWs3HuLaLEBEAuTptBQF2VNPwC6+RKh
0etBMA+qJY5hzD/cMo5wx/3YNiET6pRhadbY4+wa/bw3NeF6yJHCC0yKA6u017+c
ncu96Xlpvx8uV+TaizkDTatPttWWze+EwnFrMGwGEQlMRHdaQ9G6ATlfUHfm/FZu
94cs7zJnshV05R2HwiKBVrYuKddnIerEQng3+yPOplxJzFgn1NcUcTET3u/wCY4g
SR843RhDLUwkHbIxgNSOh1njDOdjtsqF7nYcYP/nK+FXa+YxqeL+t2q1EgKCNuPd
47pJVkMNhzwRzhKKdYr4h/cHvZx67lJLSdWkdAevMyrkZ0rwOFfwueD8o/IHOjpa
RKcDiK+h2GZSNDuaYmvmxCmT8FnFAAq+O23cwY/yaUnzntOfunduduTBbFexzPyT
678TXnzyhjDCgjby+EIZvdQ62xkUthpC4dGISbqzUL+Oax+l9yNKIHxOsSE3Q/RU
foHGZG8LK6Pl1kJdeloiyHAUVP5ZYeqXh3WoMoQpV0tTtyuxnzaI0NpcrqIujMXB
z47LxU8BbzVqIkZYCJndGlG0j0Eq+mAOkd2T9aEebg/CRu/hsA94sjWYNwARAQAB
tClBZGxlciBNZWRyYWRvIDxhZGxlckBhZGxlcm1lZHJhZG8uY29tLmJyPokCOQQT
AQIAIwUCVHhUHQIbDwcLCQgHAwIBBhUIAgkKCwQWAgMBAh4BAheAAAoJECK8ZIYV
grmfpq4P/iw1gcUxqcj2njAYpg4g63k0nPs6ZuxEgOKWnWou2oNSZQ8Ke0HIXyPw
yhh2LEFOpSZleEImz9Yl9eeRLc9q+utbjYpIC3107tDHWgUF2wofyQynPVnh2S6O
hPOYNkMd8HgjEsf8wKT+sF2YAd2dZLNbQYrPSdpF8wP6dQfG7kkgms06+5g33Adz
bZJkcx8gysDmkDPtw8/iMKeR/fIJ8qBJUM3rAsLpwHOytwF756q/JEX9dHukXbuH
XwGezKz/a7A2RSAhgsqPPYh99Nh6I8jijBJrndy29X0UHht2NO4lGHb0Bv1dcL7K
+XZ8oeHixo+vBB5Z/g/rgrPCQE8bTgtr7VQg7pmaJB3I9DXu7Wj5LPeLJ90InSMv
vwGKrrDTkrqpDR/XaJN77g62Ez+2D4gNAGb/3IWGLP4MMqVxdiJZgf9WJpG7QjtB
4MvbzNS4tUE3ReuNP7qv1y097+iW5E6nDUv4XXkVk+gcs7e8iWBNCh+6GP+2MOkH
+b7IahDQj6KFI//to3xWauPTH7995Tzn4zg8UfQaCnTLSbELJzeynSVr9VIGMg8E
CTyDGT0et9m30bl4LJ0MSK88g76g3bw5d5o8UuxGAriVDwQDjs7X5OjyFsxKalRr
c2ZVC6RL70hqWnuObvJ/wcC+atuRpwBdo2SYLqN7YEXRMtQsWx+x
=/B96
-----END PGP PUBLIC KEY BLOCK-----
</pre>

## Ferramentas de Comunicação aka Instant Messengers

* [Skype][28] &#8211; Se não fosse tão vulnerável e cheio de bugs, seria
perfeito;
* [Pidgin][29] &#8211; Eu não gosto do Google Hangouts, por isso enquanto houver
a possibilidade, eu usarei o Pidgin para me comunicar via Google Talk;
* [HipChat][30] &#8211; Uma das melhores ferramentas de comunicação para equipes
de desenvolvimento já criadas;

## Cloud Drive

* [Dropbox][31];
* [OneDrive][32];

## Bitcoin Wallet

* [Multibit][33] &#8211; Não é a melhor opção, admito, mas eu realmente não
tive *paciência* ainda para usar o app oficial do [Bitcoin][34] devido à
demora para fazer o download do [blockchain][35], como eu não movimento tanto
dinheiro assim, eu prefiro assumir o risco.

## Resumindo &#8230;

Acho que é isso, se eu me lembrar de algo relevante eu atualizarei o post.

E você, tem alguma sugestão de algo interessante que eu não tenha colocado na lista?

[1]: http://rdio.com
[2]: http://www.videolan.org/vlc/
[3]: http://gpodder.org/
[4]: https://chocolatey.org/
[5]: http://blog.adlermedrado.com.br/2014/08/gerenciador-de-pacotes-para-windows/
[6]: http://bliker.github.io/cmder/
[7]: http://postbox-inc.com/
[8]: https://atom.io/
[9]: http://markdownpad.com/
[10]: https://leanpub.com/devphpms
[11]: http://office.microsoft.com/pt-br/
[12]: https://windows.github.com/
[13]: https://www.atlassian.com/software/sourcetree/overview
[14]: http://www.visualstudio.com/en-us/news/vs2013-community-vs.aspx
[15]: http://www.php.net
[16]: https://www.jetbrains.com/phpstorm/
[17]: http://windows.microsoft.com/pt-br/windows-8/internet-information-services-iis-8-0
[18]: http://www.microsoft.com/web/downloads/platform.aspx
[19]: http://www.eclipse.org
[20]: http://elixir-lang.org/
[21]: http://www.virtualbox.org
[22]: https://www.vagrantup.com/
[23]: http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html
[24]: http://winscp.net/eng/index.php
[25]: http://www.gpg4win.org/
[26]: https://www.enigmail.net/home/index.php
[27]: http://www.getsafe.org/
[28]: http://www.skype.com
[29]: https://www.pidgin.im/
[30]: https://www.hipchat.com/
[31]: http://dropbox.com
[32]: https://onedrive.live.com/about/pt-br/
[33]: https://multibit.org/
[34]: https://bitcoin.org
[35]: https://en.bitcoin.it/wiki/Block_chain
