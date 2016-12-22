Bug estranho na integração do Mac OS X com o Google 
===================================================







------------------------------------------------------------------------







### Bug estranho na integração do Mac OS X com o Google 

Recentemente aconteceu uma coisa esquisita.

Eu tinha 3 contas do Google configuradas em meu [OS X El
Capitan](http://www.apple.com/osx/){.markup--anchor .markup--p-anchor},
a integração é bem legal porque ao integrar uma conta do Google com o OS
X ele já configura o Mail, o iMessage, o Calendar, o Notes e os Contatos
o que facilita bastante a minha vida.

Mas ontem todas as contas do Google que eu tinha configurado aqui, ao
mesmo tempo, passaram a solicitar novamente a senha e sempre que eu
tentava autenticar novamente o *Internet Accounts* travava conforme a
tela abaixo:







![Screenshot do
Bug](https://cdn-images-1.medium.com/max/1600/0*4rhd1lsb6_gaNY9P.png)



Olha que bug bizarro
#### Será que esse bug só aconteceu comigo? 

Depois de pesquisar na internet e não encontrar nada a respeito eu
resolvi chutar o balde, então fui verificar no *Keychain Access* se lá
teria alguma informação perdida sobre essas contas ou algum certificado
digital, enfim, qualquer coisa que pudesse estar causando o problema e
realmente tinham algumas informações:







![Lista de certificados relacionados ao
Google](https://cdn-images-1.medium.com/max/1600/0*aVyh5yulCBrYvOGW.png)



Lista de certificados relacionados ao Google
Como dá para ver, existem várias senhas as quais estão grifadas, então
eu apaguei tudo (não tinha nada a perder mesmo) e depois recadastrei
cada conta.

Problema solucionado.

Infelizmente eu não consegui descobrir ainda o que causou o problema,
mas a solução está aí para quem precisar.













