---
title: Acessando o Office 365 via Powershell
author: Adler Medrado
layout: post
permalink: /2014/07/acessando-o-office-365-via-powershell/
dsq_thread_id:
  - 3264376162
categories:
  - Windows
tags:
  - dicas
  - office
  - powershell
  - programming
  - tips
---
É muito fácil acessar sua conta do [Office365][1] usando [Powershell][2],
principalmente se você precisa otimizar a administração de contas corporativas
via script em situações onde é necessário manipular muitos usuários simultaneamente.

Alguns exemplos de tarefas que podem ser executadas são:

* Adicionar novos usuários;
* Remover usuários;
* Mudar permissões;
* etc.;

No texto a seguir eu demonstrarei de uma forma bem simples como se conectar a
uma conta na nuvem do Office365.

O primeiro passo é [instalar os Cmdlets][3] para Office365 ao Powershell,
a partir daí basta se familiarizar com os cmdlets específicos para esta integração.

O passo seguinte é importar o módulo MSOnline para obter acesso aos cmdlets instalados anteriormente:

<pre>
Import-Module MSOnline
</pre>

Em seguida é necessário obter as credenciais de acesso ao serviço:

<pre>$credenciais = Get-Credential</pre>

O comando acima irá mostrar uma tela nativa do Windows solicitando um nome de usuário e senha.

O problema desta abordagem é que se houver a necessidade de colocar este script
no agendador de tarefas ele não irá funcionar, neste caso será necessário
configura-lo para uso em modo não-interativo, conforme o código a seguir:

<pre>
Import-Module MSOnline
$password = "avidaebelaagenteequefodeela"
$securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
$UserName = "username@domain"
$Credentials = New-Object System.Management.Automation.PSCredential -ArgumentList $UserName, $securePassword
Connect-MsolService -Credential $Credentials
</pre>

Desta maneira o script converterá as credenciais de acesso, que estão hardcoded,
e converterá em um objeto Automation.PSCredential.

É importante frisar que nesta abordagem a segurança é menor pois a senha fica
explícita no código, o que significa que ela estará exposta a qualquer um com acesso ao código.

Durante a transação esses dados ficam criptografados no objeto Automation.PSCredential.

Pronto!

Com esses passos seu script powershell estará apto a se autenticar na nuvem do Office365.

Segue agora o código completo:

<pre>Import-Module MSOnline
$password = "huehuebrbr"
$securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
$UserName = "username@domain"
$Credentials = New-Object System.Management.Automation.PSCredential -ArgumentList $UserName, $securePassword
Connect-MsolService -Credential $Credentials
</pre>

Espero ter a oportunidade de em breve poder explorar mais funcionalidades como
criar, excluir e alterar usuários, por exemplo e também espero que este post
tenha sido útil.

[1]: http://office.microsoft.com/en-us/
[2]: http://technet.microsoft.com/pt-br/library/bb978526.aspx
[3]: http://technet.microsoft.com/en-us/library/hh974317.aspx
