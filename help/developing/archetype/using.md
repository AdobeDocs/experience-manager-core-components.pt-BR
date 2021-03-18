---
title: Uso do Arquétipo de projeto AEM
description: Instruções de uso detalhadas para o Arquétipo de projeto AEM
feature: Componentes principais, Arquétipo de projeto AEM
role: Arquiteto, desenvolvedor, administrador
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '2072'
ht-degree: 1%

---


# Arquétipo de projeto do AEM{#aem-project-archetype}

O Arquétipo de projeto AEM cria um projeto Adobe Experience Manager mínimo, baseado em práticas recomendadas, como ponto de partida para seus próprios projetos AEM. As propriedades que devem ser fornecidas ao usar esse arquétipo permitem especificar os nomes de todas as partes desse projeto, bem como controlar determinados recursos opcionais.

## Por que usar o arquétipo {#why-use-the-archetype}

Usar o Arquétipo de projeto do AEM define você no caminho para a criação de um projeto de AEM baseado em práticas recomendadas com apenas alguns pressionamentos de tecla. Com o uso do arquétipo, todas as partes já estarão em vigor, de modo que, embora o projeto resultante seja mínimo, ele já implemente todos os [recursos-chave](#what-you-get) do AEM para que tudo o que você precisa fazer seja desenvolver e estender.

É claro que há muitos elementos que entram em um projeto de AEM bem-sucedido, mas usar o Arquétipo de projeto AEM é uma base sólida e é altamente recomendado para qualquer projeto AEM.

## Introdução {#getting-started}

O arquétipo de projeto facilita começar a desenvolver em AEM. Você pode dar seus primeiros passos de várias maneiras.

* Tutorial WKND - Para obter uma ótima introdução ao desenvolvimento sobre AEM incluindo como aproveitar o arquétipo, consulte o [Tutorial WKND](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) para obter um exemplo prático que o orienta a usar o arquétipo para implementar um projeto simples.
* Tutorial de eventos WKND - Se você estiver particularmente interessado no desenvolvimento de aplicativos de página única (SPA) em AEM, verifique o [tutorial de eventos WKND dedicado](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html).
* Baixe e comece sozinho! - É possível baixar facilmente o arquétipo de projeto atual disponível no GitHub e criar seu primeiro projeto [seguindo as etapas simples abaixo](#how-to-use-the-archetype).

## O que você obtém usando o arquétipo {#what-you-get}

O Arquétipo de AEM é composto de módulos:

* **[núcleo](core.md)**: é um pacote Java que contém todas as funcionalidades principais, como serviços OSGi, ouvintes e schedulers, bem como código Java relacionado a componentes, como servlets e filtros de solicitação.
* **[it.testing](ittests.md)**: são testes de integração baseados em Java.
* **[ui.apps](uiapps.md)**: contém as  `/apps` e  `/etc` partes do projeto, ou seja, clientlibs, componentes e modelos de JS e CSS.
* **[ui.content](uicontent.md)**: contém conteúdo de amostra usando os componentes do módulo ui.apps .
* **ui.config**: contém configurações OSGi específicas para runmode para o projeto.
* **[ui.frontend.general](uifrontend.md)**:  **(opcional)** contém os artefatos necessários para usar o módulo de compilação front-end baseado em Webpack geral.
* **[ui.frontend.response](uifrontend-react.md)**:  **(opcional)** contém os artefatos necessários ao usar o arquétipo para criar projetos de SPA com base no React.
* **[ui.frontend.angular](uifrontend-angular.md)**:  **(opcional)** contém os artefatos necessários ao usar o arquétipo para criar projetos de SPA com base no Angular.
* **[ui.tests](uitests.md)**: contém testes de interface do usuário com base em Selenium.
* **todos**: é um pacote de conteúdo único que incorpora todos os módulos compilados (pacotes e pacotes de conteúdo) incluindo qualquer dependência de fornecedor.
* **analisar**: executa a análise no projeto, que fornece validação adicional para implantar no AEM como um Cloud Service.

![](/help/assets/archetype-structure.png)

Os módulos de AEM Archetype representados em Maven são implantados em AEM como pacotes de conteúdo que representam o aplicativo, o conteúdo e os pacotes OSGi necessários.

## Como usar o arquétipo {#how-to-use-the-archetype}

Para usar o arquétipo, primeiro é necessário criar um projeto, que gera os módulos em uma estrutura de arquivo local como [descrito anteriormente](#what-you-get). Como parte da geração do projeto, várias propriedades do projeto podem ser definidas, como nome do projeto, versão etc.

A construção do projeto com Maven cria os artefatos (pacotes e pacotes OSGi), que podem ser implantados no AEM. Comandos e perfis Maven adicionais podem ser usados para implantar os artefatos do projeto em uma instância do AEM.

### Criação de um projeto   {#create-project}

Para começar, você pode simplesmente usar a [AEM extensão do Eclipse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/eclipse.html) e seguir o assistente Novo projeto e escolher **AEM Amostra de projeto de vários módulos** para usar uma versão lançada do arquétipo.

É claro que você também pode chamar Maven diretamente.

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Defina `XX` para o [número de versão](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) do Arquétipo de Projeto AEM mais recente.
* Defina `aemVersion=cloud` para [AEM como um Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Defina `aemVersion=6.5.0` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), ou no local.
A dependência dos Componentes principais é adicionada apenas para versões do aem que não estão na nuvem, pois os Componentes principais são fornecidos OTB para o AEM as a Cloud
Serviço.
* Ajuste `appTitle="My Site"` para definir o título do site e os grupos de componentes.
* Ajuste `appId="mysite"` para definir o Maven artifactId, os nomes do componente, da configuração e da pasta de conteúdo, bem como os nomes da biblioteca do cliente.
* Ajuste `groupId="com.mysite"` para definir o Maven groupId e o Pacote de Origem Java.
* Pesquise a lista de propriedades disponíveis para ver se há mais itens que você deseja ajustar.

>[!NOTE]
>
>É uma prática recomendada adicionar o perfil `adobe-public` ao arquivo Maven `settings.xml` para adicionar automaticamente o repo.adobe.com ao processo de compilação maven.
>
>Um exemplo de POM [pode ser encontrado aqui](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### Propriedades {#properties}

As seguintes propriedades estão disponíveis ao criar um projeto usando o arquétipo.

| Nome | Padrão | Descrição |
--------------------------|----------------|--------------------
| `appTitle` |  | O título do aplicativo será usado para o título do site e grupos de componentes (por exemplo, `"My Site"`). |
| `appId` |  | O nome técnico será usado para nomes de componentes, configurações e pastas de conteúdo, bem como para nomes de bibliotecas de clientes (por exemplo, `"mysite"`). |
| `artifactId` | *`${appId}`* | ID de artefato Maven de base (por exemplo, `"mysite"`). |
| `groupId` |  | ID de grupo Maven de base (por exemplo, `"com.mysite"`). |
| `package` | *`${groupId}`* | Pacote de origem Java (por exemplo, `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Versão do projeto (por exemplo, `1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` | Versão de AEM de destino (pode ser `cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html); ou `6.5.0`, ou `6.4.4` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) ou no local). |
| `sdkVersion` | `latest` | Quando `aemVersion=cloud` uma versão [SDK](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) pode ser especificada (por exemplo, `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Inclui uma configuração de dispatcher para nuvem ou para AMS/no local, dependendo do valor de `aemVersion` (pode ser `y` ou `n`). |
| `frontendModule` | `none` | Inclui um módulo de compilação de frontend do Webpack que gera as bibliotecas de clientes (pode ser `general` ou `none` para sites regulares; pode ser `angular` ou `react` para um Aplicativo de página única que implementa o [Editor de SPA](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/introduction.html)). |
| `languageCountry` | `en_us` | Idioma e código do país para criar a estrutura de conteúdo (por exemplo, `en_us`). |
| `singleCountry` | `y` | Inclui uma estrutura de conteúdo principal de idioma (pode ser `y` ou `n`). |
| `includeExamples` | `y` | Inclui um site de exemplo [Biblioteca de componentes](https://www.aemcomponents.dev/) (pode ser `y` ou `n`). |
| `includeErrorHandler` | `n` | Inclui uma página de resposta 404 personalizada que será global para toda a instância (pode ser `y` ou `n`). |

>[!NOTE]
>
> Se o arquétipo for executado no modo interativo pela primeira vez, as propriedades com valores padrão não poderão ser alteradas (consulte [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obter mais detalhes). O valor pode ser alterado quando a confirmação da propriedade no final é negada e o questionário é repetido, ou passando o parâmetro na linha de comando (por exemplo, `-DoptionIncludeExamples=n`).

>[!NOTE]
>
>Ao executar no Windows e gerar a configuração do dispatcher, você deve estar executando em um prompt de comando elevado ou no Subsistema do Windows para Linux (consulte [issue 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Perfis {#profiles}

O projeto maven gerado oferece suporte a diferentes perfis de implantação ao executar `mvn install`.

| ID do perfil | Descrição |
--------------------------|------------------------------
| `autoInstallBundle` | Instale o pacote principal com o maven-sling-plugin no console felix |
| `autoInstallPackage` | Instale o pacote de conteúdo ui.content e ui.apps com o content-package-maven-plugin para o gerenciador de pacotes para a instância padrão do autor no localhost, porta 4502. O nome do host e a porta podem ser alterados com as propriedades `aem.host` e `aem.port` definidas pelo usuário. |
| `autoInstallPackagePublish` | Instale o pacote de conteúdo ui.content e ui.apps com o content-package-maven-plugin para o gerenciador de pacotes para tornar a instância de publicação padrão no localhost, porta 4503. O nome do host e a porta podem ser alterados com as propriedades `aem.host` e `aem.port` definidas pelo usuário. |
| `autoInstallSinglePackage` | Instale o pacote de conteúdo `all` com o content-package-maven-plugin no gerenciador de pacotes para a instância do autor padrão no localhost, porta 4502. O nome do host e a porta podem ser alterados com as propriedades `aem.host` e `aem.port` definidas pelo usuário. |
| `autoInstallSinglePackagePublish` | Instale o pacote de conteúdo `all` com o content-package-maven-plugin para o gerenciador de pacotes para tornar a instância de publicação padrão no localhost, porta 4503. O nome do host e a porta podem ser alterados com as propriedades `aem.host` e `aem.port` definidas pelo usuário. |
| `integrationTests` | Executa os testes de integração fornecidos na instância do AEM (somente para a fase `verify`) |

### Criação e instalação de {#building-and-installing}

Para criar todos os módulos executados no diretório raiz do projeto, use o seguinte comando Maven.

```shell
mvn clean install
```

Se você tiver uma instância AEM em execução, poderá criar e empacotar todo o projeto e implantar em AEM com o seguinte comando Maven.

```shell
mvn clean install -PautoInstallPackage
```

Para implantá-lo em uma instância de publicação, execute este comando.

```shell
mvn clean install -PautoInstallPackagePublish
```

Como alternativa, para implantar em uma instância de publicação, execute este comando.

```shell
mvn clean install -PautoInstallPackage -Daem.port=4503
```

Ou para implantar somente o pacote no autor, execute este comando.

```shell
mvn clean install -PautoInstallBundle
```

## POM pai {#parent-pom}

O `pom.xml` na raiz do projeto (`<src-directory>/<project>/pom.xml`) é conhecido como POM principal e direciona a estrutura do projeto, bem como gerencia dependências e determinadas propriedades globais do projeto.

### Propriedades do projeto global {#global-properties}

A seção `<properties>` do POM pai define várias propriedades globais que são importantes para a implantação do seu projeto em uma instância do AEM, como nome de usuário/senha, nome/porta do host etc.

Essas propriedades são configuradas para implantar em uma instância de AEM local, pois essa é a build mais comum que os desenvolvedores farão. Observe que há propriedades para implantar em uma instância de autor, bem como uma instância de publicação. Também é aqui que as credenciais são definidas para autenticação com a instância do AEM. As credenciais padrão admin:admin são usadas.

Essas propriedades são configuradas para que possam ser substituídas ao implantar em ambientes de nível superior. Dessa forma, os arquivos POM não precisam ser alterados, mas variáveis como `aem.host` e `sling.password` podem ser substituídas por argumentos de linha de comando:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Estrutura do módulo {#module-structure}

A seção `<modules>` do POM pai define os módulos que o projeto criará. Por padrão, o projeto cria [os módulos padrão definidos anteriormente](#what-you-get): core, ui.apps, ui.content, ui.tests e it.launcher. Mais módulos sempre podem ser adicionados à medida que um projeto evolui.

### Dependências {#dependencies}

A seção `<dependencyManagement>` do POM pai define todas as dependências e versões das APIs usadas no projeto. As versões devem ser gerenciadas no POM pai. Submódulos como core e ui.apps não devem incluir informações de versão.

#### Uber-Jar {#uber-jar}

Uma das dependências principais é o [AEM uber-jar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies). Isso incluirá todas as APIs AEM com apenas uma única entrada de dependência para a versão do AEM.

>[!NOTE]
>
>Como prática recomendada, atualize a versão uber-jar para corresponder à versão de destino do AEM. Por exemplo, se você planeja implantar no AEM 6.4, é necessário atualizar a versão do uber-jar para 6.4.0.

#### Componentes principais {#core-components}

O Arquétipo de projeto AEM, claro, aproveita os Componentes principais.

Os Componentes principais são instalados no AEM automaticamente no modo de execução padrão e usados pelo site WKND de amostra. Em um [modo de execução de produção](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html) (`nosamplecontent`) os Componentes principais não estão disponíveis.

Portanto, para aproveitar os Componentes principais em todas as implantações, é uma prática recomendada incluí-los como parte do projeto Maven.

>[!NOTE]
>
>Cada versão dos Componentes principais é geralmente seguida por uma versão do Arquétipo de projeto AEM, para que o arquétipo mais recente use a versão mais recente dos componentes principais.
>
>No entanto, uma nova versão do arquétipo pode não seguir diretamente uma nova versão dos Componentes principais, por isso você pode querer atualizar a dependência dos Componentes principais para a versão mais recente.

>[!NOTE]
>
>Os core.wcm.components.example são um conjunto de páginas de exemplo que ilustram exemplos dos Componentes principais. Como prática recomendada, ao implantar um projeto para uso de produção, você deve remover essa dependência e a inclusão do subpacote.

## Testes {#testing}

Existem três níveis de testes contidos no projeto e, como são diferentes tipos de testes, eles são executados de maneiras diferentes ou em lugares diferentes.

* Teste de unidade no núcleo: Isso mostra o teste de unidade clássica do código contido no pacote. Para testar, execute:
   * `mvn clean test`
* Testes de integração do lado do servidor: Esses executam testes semelhantes a unidades no ambiente AEM, ou seja, no servidor AEM. Para testar, execute:
   * `mvn clean verify -PintegrationTests`
* Testes do Hobbes.js do lado do cliente: Esses são testes do lado do navegador baseados em JavaScript que verificam o comportamento do lado do navegador. Para testar:
   1. Carregue o AEM no navegador da mesma maneira que você faria para criar uma página.
   1. Abra a página no [Modo de desenvolvedor](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html)
   1. Abra o painel esquerdo e alterne para a guia **Tests** .
   1. Localize os **Testes do MyName** gerados e execute-os.

## Próximas etapas {#next-steps}

Então você construiu e instalou o Arquétipo de Projeto AEM. E agora? Bem, o arquétipo é pequeno, mas consiste em vários exemplos de recursos avançados de AEM configurados de acordo com as práticas recomendadas. Use-os para indicar como você pode aproveitar esses recursos no seu projeto. Para qualquer projeto, você provavelmente precisará:

* [Personalizar componentes estendendo os componentes principais existentes](/help/developing/customizing.md)
* [Adicionar modelos adicionais](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [Adaptar a estrutura de localização](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [Saiba mais sobre o módulo de build de front-end](uifrontend.md)
