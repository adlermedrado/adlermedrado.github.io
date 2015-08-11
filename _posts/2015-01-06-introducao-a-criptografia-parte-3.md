---
title: 'Introdução a Criptografia &#8211; Parte 3'
author: Adler Medrado
layout: post
permalink: /2015/01/introducao-a-criptografia-parte-3/
categories:
  - Criptografia
  - Tutorial
tags:
  - criptografia
  - dicas
---
Continuando com a série de artigos introdutórios à criptografia, vou agora
mostrar como instalar o GnuPG na plataforma Windows, Gnu/Linux e Darwin (Mac OS X).

Apesar de cada plataforma possuir ferramentas gráficas para a gestão das chaves,
não é fácil manter uma uniformidade neste processo, então eu mostrarei como fazer
esta gestão utilizando o cliente de e-mail pois assim haverá uniformidade
independente da plataforma utilizada por você, leitor.
É possível também gerenciar estas chaves através da linha de comando, no entanto
meu objetivo aqui é facilitar e não complicar e eu presumo também que se você,
caro leitor, possui as habilidades necessárias para usar a linha de comando em
seu dia-a-dia, você não sentirá dificuldades em buscar essas informações nas
*man pages* ou similares.

# Importante

Se você chegou primeiro nesta parte da série, eu recomendo que leia a
[primeira][1] e a [segunda][2] antes.

# Instalação do [GnuPG][3].

## Gnu/Linux

Normalmente o GnuPG já vem instalado, mas certifique-se disso executando o
comando em seu shell:

```adler @ adler : ~ $ gpg -- version```

Se o resultado não for semelhante ao exemplo abaixo, provavelmente você precisará
fazer a instalação, neste caso, por não existir uniformidade entre os gerenciadores
de pacotes das distribuições, aconselho você a procurar a documentação de sua distribuição:

```gpg ( GnuPG ) 1.4.16
Copyright ( C ) 2013 Free Software Foundation , Inc .
License GPLv3 + : GNU GPL version 3 or later < http : / / gnu .org / licenses / gpl .html >
This is free software : you are free to change and redistribute it .
There is NO WARRANTY , to the extent permitted by law .```

## Darwin / Mac OS X

Quando eu usava Mac eu instalava o [GPGTools][4] e a instalação também é bem
tranquila.

## Windows

No Windows é necessário fazer o download do [GPG4Win][5], eu sempre faço o
download do pacote completo.

A instalação em ambiente Windows é aquela de sempre: *next, next, next, finish*,
então não entrarei em detalhes neste ponto.

# Cliente de e-mail

O cliente de e-mail que eu uso em meu dia-a-dia é o [Postbox][6] e como ele é
derivado do [Thunderbird][7], o passo-a-passo mostrado aqui em tese
funcionará nele também.

É importante lembrar que existem outros clientes de e-mail que suportam o GnuPG,
mas o único multiplataforma e open-source que conheço que seja fácil de usar é o
Thunderbird.

## Instalação do Thunderbird

Eu não mostrarei os passos para fazer a instalação do Thunderbird aqui, ao invés
disso siga as instruções da documentação oficial do Thunderbird para cada
plataforma através dos links abaixo, é bem simples:

* [Instalação do Mozilla Thunderbird no Linux][8]
* [Instalação do Mozilla Thunderbird no Mac][9]
* [Instalação do Mozilla Thunderbird no Windows][10]

> **Importante**: É bem provável que o [Thunderbird irá configur facilmente o
seu e-mail para uso nele][11], se não for o caso, a empresa que te presta
serviço de e-mail poderá auxiliá-lo na configuração.

## Instalação do Enigmail

O [Enigmail][12] é um complemento para o thunderbird que permite fazer a
integração entre ele e o GnuPG. Com ele é possível enviar e-mails criptografados
diretamente pelo cliente de e-mail sem precisar fazer dois procedimentos distintos
(criptografar um arquivo e posteriormente anexá-lo a um e-mail).

Através do menu, selecione a opção **Complementos**. O menu é localizado no
final da barra de menus, do lado direito, veja a imagem abaixo:

<img src="/media/uploads/2015/01/thunderbird-e1420588859348.png" alt="thunderbird" />

Em **Adicionar**, no campo de busca, digite: **Enigmail** e serão mostrados
diversos complementos, no ato em que este tutorial foi escrito ele estava na
primeira posição dos resultados com o nome: **Enigmail 1.7.2**, selecione-o
clicando no botão **Instalar**.

Quando a instalação terminar, reinicie o Thunderbird e ao reinicia-lo, quando
for solicitado informe que você não quer usar o *wizard*.

## Criando seu primeiro par de chaves

Agora que o ambiente está configurado, está na hora de criar seu primeiro par
de chaves.

Selecione o menu (o mesmo do screenshot acima) e em seguida a opção Enigmail,
depois selecione a opção **Gerenciamento de Chaves OpenPGP**.

Se abriu uma tela parecida com a da imagem abaixo, parabéns, se não abriu,
siga todos os passos novamente pois deve ter ocorrido algum erro.

<img src="/wp-content/uploads/2015/01/gerenciamento-de-chaves.png" alt="Criando par de chaves" />

Selecione a opção **Gerar** e depois **Novo par de Chaves**.

Bom, como dizia Jack o Estripador, vamos por partes:

* Essa nova chave será associada ao e-mail que você configurou no Thunderbird,
se você configurou mais do que uma conta, você deve selecionar a conta desejada
no primeiro campo (um combobox) no início da tela. Dá pra criar uma chave sem
associar, mas creio que para o escopo deste tutorial assim é melhor, mas se você
quiser desmarcar o *checkbox* **Usar chave gerada para a identidade selecionada**,
fica a seu critério;
* Para prover uma segurança maior para a sua chave, crie uma senha usando os
campos *Senha* e *Senha (repita)*, não utilize senhas óbvias como datas de
nascimento, placas de carro, nome da esposa/namorada, nome do cachorro, etc.
Quanto mais longa for a sua senha, melhor;
* Vamos criar uma chave de 4096 bits, pense nos bits da seguinte forma:
Quanto mais, mais difícil quebrar a criptografia, porém alguns computadores
podem ter problemas para processar isso, então caso ocorram travamentos selecione
a opção **Avançado** e diminua o tamanho da chave;
* A data de expiração da chave fica a seu critério também, eu configurei
aqui para não expirar;
* Clique em Gerar e aguarde;
* Quando este processo for finalizado, será solicitado a você que crie um
certificado de revogação, você deve estar se perguntando: **Mas o que que é isso?**
Vamos lá...

Imagine uma situação onde você utiliza suas chaves constantemente mas que por
algum motivo você acredita que ela esteja comprometida ou até mesmo você a
tenha perdido. Todas as pessoas que possuem a sua chave pública continuarão
pensando que está tudo OK com suas chaves, no entanto você não quer mais receber
nada que tenha sido cifrado usando sua chave pública, para isso você usa o
certificado de revogação, para invalidar a sua chave e avisar a todos que aquela
chave não é mais segura.

Eu mostrarei daqui a pouco que as chaves públicas podem ser enviadas para um
*servidor de chaves*, neste caso quando é feita a revogação os servidores de
chave são atualizados e esta informação é propagada para todos.

Vamos continuar, confirme a criação do certificado de revogação e depois
guarde-o em um local seguro.

## Enviando as chaves para um servidor

Como eu falei anteriormente, as chaves podem ser enviadas para servidores de
chaves. Existem diversos desses servidores espalhados pela internet e
normalmente eles fazem uma sincronização entre si, portanto basicamente se você
enviar sua chave para um servidor, em breve ela estará replicada nos demais
(pelo menos nos principais, mais famosos).

**Somente sua chave pública vai para o servidor, a sua chave privada é
responsabilidade sua protegê-la.**

### Mas por que enviar a chave pública para um servidor?

A resposta é simples: Para ficar mais fácil de você ser encontrado.

Como normalmente a chave está associada a um endereço de e-mail, se alguém
quiser te enviar algo criptografado mas não sabe qual é sua chave pública,
basta essa pessoa pesquisar pelo seu e-mail em um servidor de chaves para
poder encontrá-la.

**Agora vamos enviar nossa nova chave para um servidor.**

Na tela de gerenciamento de chaves, clique com o botão direito em cima do seu
endereço de e-mail, em seguida clique em **Enviar chaves públicas para servidor
de chaves**.

Pronto. 😉

## Que tal enviar um e-mail criptografado para testar?

**Primeiramente, importe a minha chave pública.**

Abra a tela de gerenciamento de chaves e selecione a opção **Servidor de
Chaves** no menu, em seguida selecione a opção **Procurar por chaves**,
daí coloque meu e-mail: adler *arroba* adlermedrado *ponto* com *ponto* br,
serão mostradas muitas chaves, a maioria delas estão inválidas e eu esqueci de
criar o certificado de revogação (daí a importância deles), ignore todas as
chaves com exceção daquela que tem o ID **158299F**, selecione-a e faça a
importação clicando em OK.

Você verá que após esse procedimento o meu e-mail e as chaves associadas a ele
estarão na lista de chaves, junto com a sua.

### Enviando o e-mail criptografado

Agora que as chaves estão criadas e você já importou a minha para poder me
enviar um e-mail, vamos testar se tudo está OK.

* Clique em Nova Mensagem;
* Informe o meu endereço de e-mail;
* Informe um título para o e-mail;
* Escreva o conteúdo do seu e-mail;
* Clique no menu Enigmail;
* Clique em **A mensagem será criptografada**;
* Clique em **Force Encryption**;
* Clique em Enviar agora;

Se for mostrada uma mensagem falando sobre o formato HTML, etc., ignore-a pois é
apenas um aviso que o conteúdo pode perder formatação após a encriptação.

**Se tudo correr bem**, eu receberei um e-mail seu e o responderei avisando que recebi OK.

## Considerações finais

Na próxima parte eu mostrarei como criptografar arquivos e também como usar um plugin para Firefox e Google Chrome que permite realizar estes mesmos passos diretamente no Gmail e outros webmails.

Eu espero ter sido claro, eu tentei ser o menos técnico possível mas caso tenha ficado alguma dúvida, envie um comentário que eu tentarei ajuda-lo.

 [1]: http://blog.adlermedrado.com.br/2014/12/introducao-a-criptografia-parte-1/
 [2]: http://blog.adlermedrado.com.br/2014/12/introducao-a-criptografia-parte-2/
 [3]: https://www.gnupg.org/
 [4]: https://gpgtools.org/
 [5]: http://www.gpg4win.org/
 [6]: http://postbox-inc.com/
 [7]: https://www.mozilla.org/pt-BR/thunderbird/
 [8]: https://support.mozilla.org/pt-BR/kb/instalando-thunderbir-linux
 [9]: https://support.mozilla.org/pt-BR/kb/instalando-o-thunderbird-no-mac
 [10]: https://support.mozilla.org/pt-BR/kb/instalando-thunderbird-no-windows
 [11]: https://support.mozilla.org/pt-BR/kb/configuracao-automatica-de-conta
 [12]: https://www.enigmail.net/home/index.php
