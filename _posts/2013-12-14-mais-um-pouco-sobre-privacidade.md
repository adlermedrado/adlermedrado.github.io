---
title: Mais um pouco sobre privacidade
author: Adler Medrado
layout: post
permalink: /2013/12/mais-um-pouco-sobre-privacidade/
categories:
  - General
---
Eu resolvi escrever este post depois de ficar pensando neste assunto por um
tempo, então se você não se importa muito com a proteção da privacidade e/ou
acha que quem se preocupa com isso é teórico da conspiração, pirado, louco ou
qualquer coisa do gênero, fique com essa foto desse gatinho com uma cara
engraçada, assim a vinda até este post não foi em vão.

<img src="/media/funny-cat.jpg?w=660" alt="funny cat" />

## Mas se você quiser ler um resumo sobre o que penso a respeito deste assunto, é só continuar a leitura.

Nós estamos vivendo na era da informação, sendo assim quem possui o domínio
sobre a informação possui o poder. Não é a toa que os governos estão tentando
de uma forma ou de outra tomar o controle de tudo que trafega na internet para
censurar e vigiar seus cidadãos.

Um exemplo disso é a China que, se precisar,
[simplesmente desliga a internet e deixa todo mundo off][2],
além disso é o governo quem determina o que pode e o que não pode ser
acessado pela população daquele país.

<img src="/media/golden-shield-project.jpg" alt="Golden Shield Project" />

Outro exemplo de vigilância da internet pelo estado é o [Prism][2],
gerido pela NSA, um órgão dos EUA.

<img src="/media/220px-PRISM_logo_PNG.png" alt="Prism Logo" />

No caso do Prism, o governo conta com o apoio de empresas gigantes da internet
como Microsoft, Google e Facebook, existem até informações de que as conversas
em ambientes de jogos como o World of Warcraft [eram monitoradas pelos agentes da NSA][3].

## O que podemos fazer contra a invasão de privacidade?

É esta pergunta que estou me fazendo neste exato momento, no entanto eu estou
com algumas idéias, tendo em vista que muitas das informações coletadas por
estes programas de vigilância se baseiam em informações que deixamos em redes
sociais, acho que são pequenos costumes que podemos adotar afim de diminuir a
invasão em nossa privacidade.

Primeiramente, precisamos definir bem as características que as informações que
são postadas em redes como Google ou Facebook devem ter para serem consideradas:

* Públicas -> Informações que qualquer pessoa na internet pode ver;
* Somente Amigos -> Informações públicas mas que inicialmente você só deseja que seus amigos vejam;
* Somente você -> É aquela informação que você posta na rede social mas não quer que ninguém veja;

Normalmente nós temos estes 3 níveis de privacidade, então, se você deseja
que algo nunca se torne público, nunca publique esta informação em local algum
na internet, até porque, mesmo que ocultado para alguns, estas informações
estão nos servidores destas empresas e é certo que nunca serão excluídas.

## Mas apenas isso não é suficiente

Conforme eu mencionei em [outro post][4], existem diversas ferramentas que
podem ajudar a incrementar a segurança de nossa privacidade na internet.

Quando o assunto é privacidade na internet, nem tudo se resume a posts em redes
sociais, [como está bem explicado aqui][5]. Por exemplo, recentemente eu entrei
no mercado livre e pesquisei por uma máquina de calcular *Facit C1-13* para
ter uma noção de quanto custa uma máquina dessas e depois disso, sempre que
acesso qualquer local com propagandas, eu vejo anúncios desse tipo de máquina.

Além das ferramentas citadas no post mencionado anteriormente, existem
ferramentas que podem nos ajudar a obter um nível maior de anonimização,
o que por sua vez nos garante uma privacidade maior, as que eu uso ou já usei,
todas são relacionadas ao [TOR][7] e cada uma de sua maneira são bem eficazes
naquilo que se propõem.

A primeira opção, que eu gosto de usar pela simplicidade é o [Whonix][8],
que consiste em duas máquinas virtuais [Virtualbox][9] sendo uma um gateway
baseado em TOR e a outra, chamada de workstation que é usada para navegar na internet.
Segundo o site oficial:

> Whonix is an operating system focused on anonymity, privacy and security.
It’s based on the Tor anonymity network, Debian GNU/Linux and security by
isolation. DNS leaks are impossible, and not even malware with root
privileges can find out the user’s real IP.
>
> Whonix consists of two parts: One solely runs Tor and acts as a gateway,
which we call Whonix-Gateway. The other, which we call Whonix-Workstation,
is on a completely isolated network. Only connections through Tor are possible.

<img src="/media/whonix.jpg" alt="whonix" />

Usando o whonix é garantido que a conexão passa somente pelo TOR o que garante
um nível maior de privacidade, claro que se uma pessoa usar este aparato e
acessar o Facebook e postar algo comprometedor, não adiantará nada, afinal de
contas, não existe patch para a estupidez humana.

Outra opção é usar o [Tails][10], que é uma distribuição Linux, que igualmente
ao Whonix é baseada em Debian e só permite tráfego de internet por meio da rede
TOR, a diferença é que o Tails foi criado para ser usado como LiveCD, ou seja,
é necessário instalar ele num CD, DVD, USB, SD Card, enfim, e dar boot usando
este dispositivo com um sistema operacional independente do instalado no computador.

<img src="/media/tails-tor.png" alt="tails-tor" />

Estas duas ferramentas permitem a navegação com um nível de anonimização maior
do que a internet aberta que usamos normalmente e assim acabamos por proteger
nossa privacidade, mas como eu disse anteriormente, tem que saber usar a
ferramenta, senão não adianta nada.

## E a respeito do Cloud? É seguro?

<img src="/media/screen-shot-2013-06-11-at-4.24.18-pm.png" alt="Cloud Computing" />

Se analisarmos friamente, tudo que colocamos em ambiente cloud não é mais nosso.
Mesmo que as informações armazenadas em Cloud sejam explicitamente excluídas,
quem garante que não existe um backup guardado em algum lugar a disposição do
governo ou de empresas privadas?

O que eu costumo tentar fazer é criptografar tudo que eu julgo importante antes
de colocar em um ambiente que eu não possua total controle, neste caso eu me
refiro a armazenamento de arquivos usando um serviço como o Dropbox por exemplo,
então eu uso o [GPG][12] para guardar qualquer informação que eu julgue restrita
e que por algum motivo eu tenha que deixar num ambiente como esse.

Recentemente eu recebi um SMS de uma operadora de celular me oferecendo
5GB gratuitos para armazenar meus arquivos na nuvem. Já não basta as
operadoras de telefonia terem acesso a todas as nossas informações,
ligações, etc., ainda querem mais informações? No way.

## Para finalizar

Nós estamos tão habituados a este bombardeamento de informações que nem nos
damos conta de que os governos e grandes corporações estão nos vigiando o tempo
todo, não é necessário nem mesmo aparatos como o Prism para obterem informações,
porque se pensarmos bem nossas informações estão nas mãos deles e nós as
entregamos de mão beijada.

Microsoft, Google e Yahoo!, entre outras, tem acesso aos nossos e-mails,
operadoras de telefonia tem acesso a nossas informações, empresas de TV a cabo,
provedores de internet, Foursquare, Facebook e quantos mais outros, tudo de mão
beijada, porque nós damos a eles todas as informações que eles querem.

Um fato engraçado e que creio que não tenha ocorrido só comigo, mas após minha
esposa contratar os serviços de uma operadora de telefonia fixa e internet,
quase instantâneamente começamos a receber uma enxurrada de ligações de empresas
oferecendo serviços diversos, ou seja, além de ter nossos dados eles ainda
disponibilizam a terceiros, incluindo aí dados bancários, pois uma dessas
empresas que passaram a nos ligar, começou a agendar débito em nossa conta
corrente mesmo sem nós termos contratado serviço algum dela.

Eu não quero que este post fique parecendo algo sensacionalista, mas ultimamente
eu tenho pensado nessas coisas e por isso resolvi escrever aqui os
meus pensamentos a respeito.

Se você tiver alguma dica de como melhorar a segurança de nossos dados e
nossa privacidade, sinta-se a vontade para expressa-la nos comentários.
Eu realmente quero muito saber.

[1]: http://i1.wp.com/adlermedrado.com.br/images/2013-12-14-mais-um-pouco-sobre-privacidade/funny-cat.jpg
[2]: http://en.wikipedia.org/wiki/Golden_Shield_Project
[3]: http://idgnow.uol.com.br/internet/2013/12/10/nsa-espionou-gamers-de-world-of-warcraft-xbox-live-e-second-life/
[4]: http://adlermedrado.com.br/blog/tools-for-increase-your-privacy/
[5]: http://donttrack.us/
[7]: https://www.torproject.org/
[8]: https://www.whonix.org/wiki/Main_Page
[9]: http://www.virtualbox.org
[10]: https://tails.boum.org/
[12]: http://www.gnupg.org/
