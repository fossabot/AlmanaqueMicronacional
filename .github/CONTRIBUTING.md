# Como Contribuir

:heart: Obrigado por seu interesse em contribuir com o *Almanaque Micronacional* :heart:

As contribuições da comunidade são bem-vindas e muito apreciadas. Há algumas formas de envolver-se com este projeto, como relatando issues, opinando sobre o design do aplicativo, e contribuindo com código. Por favor, leia o restante deste documento para garantir um processo de contribuição agradável.

## Introdução ao Git e ao GitHub

Se você é novo nisso,

* [Abra uma conta no GitHub](https://github.com/signup/free).
* Aprenda sobre o Git e o GitHub neste artigo: [Good Resources for Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/).
* Entenda o fluxo de desenvolvimento do [Git Flow](https://danielkummer.github.io/git-flow-cheatsheet/index.pt_BR.html)

## Contribuindo com relatórios de issues

* Entenda nosso [gerenciamento de issues](/docs/gerenciamento-de-issues.md).
* [Verifique se o issue já não relatado antes](https://github.com/lonedevsoftware/AlmanaqueMicronacional/issues).
* Se já não tiver sido reportado, [reporte seu issue](https://github.com/lonedevsoftware/AlmanaqueMicronacional/issues/new/choose) seguindo as instruções da melhor forma possível.

## Contribuindo com design

O aplicativo depende dos controles fornecidos pela [Windows Community Toolkit](https://github.com/windows-toolkit/WindowsCommunityToolkit) para o seu design, que usam certos elementos do Fluent Design System. Obviamente, o design pode não ser agradável e, como qualquer outra peça do software, pode ser melhorado.

Caso encontre irregularidades no design, abra um relatório de issue como descrito acima, descrevendo o que há de errado. Caso saiba como corrigir, crie um pull request com suas alterações

## Contribuindo com código

A IDE usada no desenvolvimento é o [Visual Studio 2017 Community Edition](https://visualstudio.microsoft.com/). O aplicativo é construído com os blocos de construção do [Windows Template Studio](https://blogs.windows.com/buildingapps/2017/05/16/announcing-windows-template-studio/
) e usa controles fornecidos pela Windows Community Toolkit.

### Obter e compilar

A partir de um prompt de comando, e com o Git instalado, clone o repositório para seu computador local com o comando `git clone https://github.com/lonedevsoftware/AlmanaqueMicronacional.git`. Abra o arquivo de solução `AlmanaqueMicronacional.sln`, aperte F5 e espere o Visual Studio baixar os pacotes necessários, compilar o aplicativo, implantá-lo em sua máquina e executá-lo para você.

### Testar

:scream: AJUDA NECESSÁRIA :scream:

Caso você saiba como escrever testes e tenha tempo e disposição para isso, por favor, envie sua contribuição por meio de um pull request :sob:

### Encontrar ou criar relatórios de issues

1. Siga as instruções em Contribuindo com relatórios de issues, acima, para encontrar ou criar um relatório.
2. Mencione no issue que você está trabalhando nele e solicite atribuição a @joaosantana.

### Escrever código

Lembre-se, este projeto usa o Git Flow para seu fluxo de desenvolvimento.

Após clonar o repositório e escolher onde e como contribuir, inicialize seu branch com o comando apropriado:

* Se uma funcionalidade, `git flow feature start SUAFEATURE`
* Se um hotfix, `git flow hotfix start RELEASE` (onde RELEASE é a versão com problema)

Em ambos os casos, desenvolva seu código e, quando ele estiver como esperado, abra um pull request para mesclar seu código à base de código do projeto.

### Pull Requests

Pull requests são a forma, no GitHub, de apresentar seu código para que seja revisado e mesclado à base de código do projeto.

Espera-se que um pull request siga as diretrizes abaixo. Caso contrário, o autor será informado sobre como corrigir seu pull request até que esteja pronto para mesclagem.

#### Ciclo de vida de um pull request

Antes de submeter:

* Mantenha seus commits limpos, com cada um deles representando uma única mudança completa no código. Se você estiver trabalhando em três arquivos diferentes, faça três commits; se esses três arquivos estiverem relacionados, faça um commit.
* [Assine seus commits com sua chave GPG](https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work). Além disso, use a opção `-s` para assegurar que o código que você está enviando é seu mesmo, por meio do [Developer's Certificate of Origin](https://developercertificate.org/). Um ProBot faz a verificação necessária e rejeita o pull request que não está devidamente assinado.
  * Para entender a razão disso, leia [A Git Horror Story](https://mikegerwitz.com/papers/git-horror-story.html), de Mike Gerwitz.

Submetendo:

* Crie o pull request no branch correto - se feature, para o branch `develop`, se hotfix para o branch `master`.
* Crie um título que descreva o que seu pull request resolve, referenciando o issue original. Não use apenas "Resolve issue #5", nem use o título do issue no seu pull request.
* Enquanto seu pull request não estiver pronto para mesclagem, acrescente e mantenha o prefixo `WIP`.
* Inclua um sumário sobre suas mudanças na descrição do pull request. Esses sumários são usados para criar changelogs. Se as mudanças estão relacionadas a um issue relatado, referencie esse issue na descrição do pull request (na forma Resolve #11).
* Por favor, use o presente do indicativo ao descrever suas mudanças; ao invés de "Corrigido padding em SettingsPage", escreva "Corrige padding em SettingsPage".
* Se suas mudanças acrescentam um novo arquivo-fonte, assegure-se de que ele possui o cabeçalho de copyright abaixo:

```csharp
// <copyright file="`NomeDoArquivo.ext`" company="SeuNome">
// Copyright (c) SeuNome. All rights reserved.
// </copyright>
```

Revisão e mesclagem:

* Ao enviar seu pull request, ele será revisado, imediatamente, tanto pelo AppVeyor (o serviço de CI/CD que nos conquistou :heart:) quanto pelo ProBot DCO (que verifica se você usou a opção `-s`, como explicado acima).
* Caso hajam correções a serem feitas, elas serão indicadas nos comentários do pull request.
* Não havendo ajustes a serem feitos, seu pull request será revisado por um humano.
* Não havendo mais nada que impeça, seu pull request então será mesclado, com o seu nome acrescentado à [lista de contribuintes](/docs/CONTRIBUTORS).

## Developer's Certificate of Origin

By making a contribution to this project, I certify that:

1. The contribution was created in whole or in part by me and I have the right to submit it under the open source license indicated in the file; or
2. The contribution is based upon previous work that, to the best of my knowledge, is covered under an appropriate open source license and I have the right under that license to submit that work with modifications, whether created in whole or in part by me, under the same open source license (unless I am permitted to submit under a different license), as indicated in the file; or
3. The contribution was provided directly to me by some other person who certified (a), (b) or (c) and I have not modified it.
4. I understand and agree that this project and the contribution are public and that a record of the contribution (including all personal information I submit with it, including my sign-off) is maintained indefinitely and may be redistributed consistent with this project or the open source license(s) involved.
