---
title: Uso do Arquétipo de projeto do AEM
description: Saiba como usar o Arquétipo de projeto do AEM para criar um projeto mínimo do Adobe Experience Manager baseado em práticas recomendadas como ponto de partida para seus próprios projetos AEM.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 100%

---


# Uso do Arquétipo de projeto do AEM {#using-the-archetype}

Este documento explica como é possível usar o Arquétipo de projeto do AEM para criar um projeto mínimo do Adobe Experience Manager com base em práticas recomendadas como ponto de partida para seus próprios projetos AEM.

Ele se concentra nos padrões de uso geral e no que o arquétipo faz por você. Para obter opções de criação detalhadas e instruções técnicas, consulte a documentação no repositório do GitHub do arquétipo.

>[!TIP]
>
>O Arquétipo de projeto do AEM mais recente e a documentação técnica associada [podem ser encontrados no GitHub.](https://github.com/adobe/aem-project-archetype)

## Introdução {#getting-started}

Com o arquétipo de projeto fica mais fácil começar a desenvolver no AEM. Você pode dar os primeiros passos com o arquétipo de várias maneiras.

* **Tutorial do WKND**: para obter uma excelente introdução ao desenvolvimento no AEM, inclusive como aproveitar o arquétipo, consulte a [Introdução ao AEM Sites – Tutorial do WKND](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=pt-BR) para obter um exemplo prático que orienta através do uso do arquétipo para implementar um projeto simples.
* **Tutorial de eventos do WKND**: se você estiver particularmente interessado no desenvolvimento de aplicativos de página única (SPA) no AEM, confira o [tutorial dedicado de eventos do WKND.](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html?lang=pt-BR)
* **Comece sozinho!**: você pode baixar facilmente o [arquétipo de projeto atual disponível no GitHub](https://github.com/adobe/aem-project-archetype) e criar seu primeiro projeto por conta própria.

## Como usar o arquétipo {#how-to-use-the-archetype}

A primeira etapa para usar o arquétipo é criar um projeto, que gera [os módulos](#what-you-get) em uma estrutura de arquivo local. Como parte da geração do projeto, diversas propriedades do seu projeto podem ser definidas, como nome do projeto, versão, habilitação de diversas opções, etc.

>[!TIP]
>
>Sempre que você criar o arquétipo, ele também gerará uma série de arquivos Leia-me, fornecendo os detalhes técnicos e o uso de cada módulo como [no link abaixo.](#what-you-get)

Desenvolver o projeto com o Maven cria os artefatos (pacotes e pacotes OSGi), que podem ser implantados no AEM. Comandos e perfis Maven adicionais podem ser usados para implantar os artefatos do projeto em uma instância do AEM.

## O que você ganha usando o Arquétipo {#what-you-get}

O arquétipo é composto de módulos, todos criados automaticamente ao usar o arquétipo.

* **[core](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** é um pacote Java que contém todas as funcionalidades principais, como serviços OSGi, ouvintes e schedulers, bem como código Java relacionado a componentes, como servlets e filtros de solicitação.
* **[it.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** são testes de integração baseados em Java.
* **[ui.apps](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.apps)** contém as partes `/apps` e `/etc` do projeto, ou seja, clientlibs CSS e JS, componentes e modelos.
* **[ui.content](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.content)** contém conteúdo de amostra usando os componentes do módulo ui.apps.
* **[ui.config](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.config)** contém configurações OSGi específicas do modo de execução para o projeto.
* **[ui.frontend.general](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.general)** contém os artefatos necessários para usar o módulo geral de criação de front-end baseado em Webpack (opcional).
* **[ui.frontend.react](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.react)** **(opcional)** contém os artefatos necessários ao usar o arquétipo para criar projetos de SPA baseados no React (opcional, depende da criação de parâmetros).
* **[ui.frontend.angular](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.angular)** **(opcional)** contém os artefatos necessários ao usar o arquétipo para criar projetos de SPA baseados no Angular (opcional, depende da criação de parâmetros).
* **[ui.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** contém testes de interface baseados em Selenium.
* **[all](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/all)** é um pacote de conteúdo único que incorpora todos os módulos compilados (pacotes e pacotes de conteúdo), incluindo todas as dependências de fornecedor.
* **[dispatcher.ams](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.ams)** contém as configurações básicas do dispatcher para projetos AMS/no local (opcional, depende dos parâmetros de criação).
* **[dispatcher.cloud](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.cloud)** contém as configurações básicas do dispatcher para projetos AEMaaCS (opcional, depende dos parâmetros de criação).

![Organização do pacote de conteúdo](/help/assets/content-package-organization.png)

Os módulos do arquétipo representado no Maven são implantados no AEM como pacotes de conteúdo que representam o aplicativo, o conteúdo e os pacotes OSGi necessários.

## POM principal {#parent-pom}

O `pom.xml` na raiz do projeto (`<src-directory>/<project>/pom.xml`) é conhecido como POM principal e direciona a estrutura do projeto, bem como gerencia dependências e determinadas propriedades globais do projeto.

### Propriedades globais do projeto {#global-properties}

A seção `<properties>` do POM principal define várias propriedades globais são importantes para a implantação do seu projeto em uma instância do AEM, como nome de usuário/senha, nome/porta do host etc.

Essas propriedades são configuradas para implantar em uma instância do AEM local, pois essa é a build mais comum que os desenvolvedores farão. Observe que há propriedades para implantar em uma instância de autor, bem como uma instância de publicação. Também é aqui que as credenciais são definidas para autenticação com a instância do AEM. As credenciais `admin:admin` padrão são usadas.

Essas propriedades são configuradas para que possam ser substituídas ao implantar em ambientes de nível superior. Dessa forma, os arquivos POM não precisam ser alterados, mas variáveis como `aem.host` e `sling.password` podem ser substituídas por argumentos de linha de comando:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Estrutura do módulo {#module-structure}

A seção `<modules>` do POM principal define os módulos que o projeto criará. Por padrão, o projeto cria [os módulos padrão definidos anteriormente.](#what-you-get)Mais módulos sempre podem ser adicionados à medida que o projeto evolui.

### Dependências {#dependencies}

A seção `<dependencyManagement>` do POM principal todas as dependências e versões das APIs usadas no projeto. As versões devem ser gerenciadas no POM principal. Os submódulos não devem incluir informações de versão.

#### Uber-Jar {#uber-jar}

Uma das dependências principais é o [Jar da API Java do AEM. ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html?lang=pt-BR) Ela incluirá todas as APIs do AEM com apenas uma única entrada de dependência para a versão do AEM.

>[!NOTE]
>
>Como prática recomendada, atualize a versão uber-jar para corresponder à versão de destino do AEM. Por exemplo, se você planeja implantar no AEM 6.5, é necessário atualizar a versão do uber-jar para 6.5.X, em que o `X` é o pacote de serviços mais recente.

#### Componentes principais {#core-components}

Claro que o arquétipo aproveita os [Componentes principais.](/help/introduction.md) Portanto, para aproveitar os Componentes principais em todas as implantações, a prática recomendada é incluí-los como parte do projeto Maven.

O core.wcm.components.examples é um conjunto de páginas de exemplo que ilustra exemplos dos Componentes principais. Como prática recomendada, ao implantar um projeto para uso de produção, você deve remover essa dependência e a inclusão do subpacote.

>[!NOTE]
>
>Os Componentes principais e o arquétipo são mantidos como projetos do GitHub separados e, como tal, suas versões são diferentes.
>
>Cada versão do arquétipo utilizará a versão mais recente dos Componentes principais disponíveis no momento do lançamento. No entanto, talvez seja melhor atualizar a dependência nos Componentes principais manualmente.

## Testes {#testing}

Existem três níveis de testes contidos no projeto e, como são diferentes tipos de testes, são executados de maneiras diferentes ou em lugares diferentes.

* **[Testes de unidade](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)**: teste de unidade clássica do código contido no pacote
* **[Testes de integração](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)**: testes de integração no lado do servidor que executam testes semelhantes a unidades no ambiente do AEM, ou seja, no servidor do AEM
* **[Testes de interface](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)**: testes do lado do navegador baseados em Selenium que verificam o comportamento do lado do navegador
