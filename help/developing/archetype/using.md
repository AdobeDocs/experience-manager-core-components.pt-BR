---
title: Uso do AEM Project Archetype
description: Instruções de utilização detalhadas para o AEM Project Archetype
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Arquétipo de projeto do AEM{#aem-project-archetype}

O AEM Project Archetype cria um projeto Adobe Experience Manager mínimo baseado em práticas recomendadas como ponto de partida para seus próprios projetos AEM. As propriedades que devem ser fornecidas ao usar esse arquétipo permitem especificar os nomes de todas as partes deste projeto, bem como controlar determinados recursos opcionais.

## Por que usar o Archetype {#why-use-the-archetype}

Usar o AEM Project Archetype o define no caminho para a criação de um projeto AEM baseado em práticas recomendadas com apenas alguns pressionamentos de teclas. Usando o arquétipo, todas as partes já estarão no lugar para que, embora o projeto resultante seja mínimo, ele já implemente todos os recursos [](#what-you-get) principais do AEM para que tudo o que você precisa fazer seja construir sobre cima e estender.

É claro que há muitos elementos que entram em um projeto bem-sucedido AEM, mas usar o AEM Project Archetype é uma base sólida e é altamente recomendável para qualquer projeto AEM.

## Introdução {#getting-started}

O arquétipo de projeto facilita começar a desenvolver em AEM. Você pode dar seus primeiros passos de várias maneiras.

* Tutorial de WKND - Para obter uma excelente introdução ao desenvolvimento AEM incluindo como aproveitar o arquétipo, consulte o Tutorial [de](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) Introdução ao AEM Sites - WKND para obter um exemplo prático que o orienta a usar o arquétipo para implementar um projeto simples.
* Tutorial de Eventos WKND - Se você estiver particularmente interessado no desenvolvimento de aplicativos de página única (SPA) no AEM, verifique o tutorial [de Eventos](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)WKND dedicados.
* Baixe e start por conta própria! - Você pode baixar facilmente o arquétipo de projeto atual disponível no GitHub e criar seu primeiro projeto, [seguindo as etapas simples abaixo](#how-to-use-the-archetype).

## O que você obtém usando o Archetype {#what-you-get}

O AEM Archetype é composto de módulos:

* **[núcleo](core.md)**: é um pacote Java que contém todas as funcionalidades principais, como serviços OSGi, ouvintes e scheduleres, bem como código Java relacionado a componentes, como servlets e filtros de solicitação.
* **[ui.apps](uiapps.md)**: contém as `/apps` e `/etc` partes do projeto, ou seja, clientlibs JS e CSS, componentes, modelos, configurações específicas do modo de execução, bem como testes Hobbes.
* **[ui.content](uicontent.md)**: contém conteúdo de amostra usando os componentes do módulo ui.apps.
* **[ui.testing](uitests.md)**: é um pacote Java que contém testes JUnit executados no lado do servidor. Este pacote não deve ser implantado na produção.
* **ui.launch**: contém o código de cola que implanta o pacote ui.testing (e os pacotes dependentes) para o servidor e aciona a execução remota da JUnit.
* **[ui.frontende.general](uifrontend.md)**: **(opcional)** contém os artefatos necessários para usar o módulo de compilação front-end geral baseado no Webpack.
* **[ui.frontende.response](uifrontend-react.md)**: **(opcional)** contém os artefatos necessários ao usar o arquétipo para criar projetos SPA baseados em Reagir.
* **[ui.frontende.angular](uifrontend-angular.md)**: **(opcional)** contém os artefatos necessários ao usar o arquétipo para criar projetos SPA baseados em Angular.

![](/help/assets/archetype-structure.png)

Os módulos de AEM Archetype representados em Maven são implantados em AEM como pacotes de conteúdo que representam o aplicativo, o conteúdo e os pacotes OSGi necessários.

## Como usar o Archetype {#how-to-use-the-archetype}

Para usar o arquétipo, primeiro é necessário criar um projeto, que gera os módulos em uma estrutura de arquivos local, conforme descrito [](#what-you-get)anteriormente. Como parte da geração do projeto, várias propriedades do projeto podem ser definidas, como nome do projeto, versão etc.

A construção do projeto com Maven cria os artefatos (pacotes e pacotes OSGi), que podem ser implantados no AEM. Comandos e perfis Maven adicionais podem ser usados para implantar os artefatos do projeto em uma instância AEM.

### Criação de um projeto   {#create-project}

Para começar, basta usar a extensão [](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/aem-eclipse.html) AEM Eclipse e seguir o assistente de Novo projeto e escolher **AEM Amostra de projeto** de vários módulos para usar uma versão lançada do arquétipo.

Claro que você também pode chamar Maven diretamente.

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.granite.archetypes \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Defina `XX` para o número [de](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) versão do AEM Project Archetype mais recente.
* Definir `aemVersion=cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Defina `aemVersion=6.5.0` para Serviços [gerenciados da](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)Adobe ou no local.
A dependência dos Componentes principais é adicionada somente para versões aem não-nuvem, já que os Componentes principais são fornecidos como OOTB para AEM como CloudService.
* Ajuste `appTitle="My Site"` para definir o título do site e os grupos de componentes.
* Ajuste `appId="mysite"` para definir a Maven artiactualId, os nomes de componentes, configurações e pastas de conteúdo, bem como os nomes da biblioteca do cliente.
* Ajuste `groupId="com.mysite"` para definir Maven groupId e o Pacote de origem Java.
* Pesquise a lista das propriedades disponíveis para ver se há mais itens que você deseja ajustar.

>[!NOTE]
>
>É prática recomendada adicionar o `adobe-public` perfil ao seu arquivo Maven `settings.xml` para adicionar automaticamente repo.adobe.com ao processo de compilação maven.
>
>Um exemplo de POM [pode ser encontrado aqui](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### Propriedades {#properties}

As seguintes propriedades estão disponíveis ao criar um projeto usando o arquétipo.

| Nome | Padrão | Descrição |
--------------------------|----------------|--------------------
| `appTitle` |  | O título do aplicativo será usado para o título do site e grupos de componentes (por exemplo, `"My Site"`). |
| `appId` |  | O nome técnico será usado para nomes de pastas de componentes, configurações e conteúdo, bem como para nomes de bibliotecas de clientes (por exemplo, `"mysite"`). |
| `artifactId` | *`${appId}`* | ID de artefato de Maven de base (por exemplo, `"mysite"`). |
| `groupId` |  | ID de grupo do Maven de base (por exemplo, `"com.mysite"`). |
| `package` | *`${groupId}`* | Pacote de código-fonte Java (por exemplo, `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Versão do projeto (por exemplo, `1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` | Versão AEM público alvo (pode ser `cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html); ou `6.5.0`, ou `6.4.4` para serviços [gerenciados](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) da Adobe ou no local). |
| `sdkVersion` | `latest` | Quando é possível especificar `aemVersion=cloud` uma versão [SDK](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) (por exemplo, `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Inclui uma configuração de despachante para nuvem ou para AMS/no local, dependendo do valor de `aemVersion` (pode ser `y` ou `n`). |
| `frontendModule` | `none` | Inclui um módulo de construção de front-end do Webpack que gera as bibliotecas do cliente (pode ser `general` ou `none` para sites regulares; pode ser `angular` ou `react` para um aplicativo de página única que implemente o Editor [](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/introduction.html)SPA). |
| `languageCountry` | `en_us` | Código de idioma e país para criar a estrutura de conteúdo (por exemplo, `en_us`). |
| `singleCountry` | `y` | Inclui uma estrutura de conteúdo principal de idioma (pode ser `y`, ou `n`). |
| `includeExamples` | `y` | Inclui um site de exemplo da Biblioteca [de](https://www.aemcomponents.dev/) componentes (pode ser `y`, ou `n`). |
| `includeErrorHandler` | `n` | Inclui uma página de resposta 404 personalizada que será global para a instância inteira (pode ser `y` ou `n`). |

>[!NOTE]
>
> Se o arquétipo for executado no modo interativo pela primeira vez, as propriedades com valores padrão não poderão ser alteradas (consulte [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obter mais detalhes). O valor pode ser alterado quando a confirmação de propriedade no final for negada e o questionário for repetido, ou transmitindo o parâmetro na linha de comando (por exemplo, `-DoptionIncludeExamples=n`).

>[!NOTE]
>
>Ao executar no Windows e gerar a configuração do dispatcher, você deve estar em execução em um prompt de comando elevado ou no Subsistema do Windows para Linux (consulte o [problema 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Perfis {#profiles}

O projeto maven gerado suporta diferentes perfis de implantação durante a execução `mvn install`.

| ID do perfil | Descrição |
--------------------------|------------------------------
| `autoInstallBundle` | Instale o pacote principal com o plug-in maven-sling no console felix |
| `autoInstallPackage` | Instale o pacote de conteúdo ui.content e ui.apps com o content-package-maven-plugin no gerenciador de pacotes para a instância padrão do autor no localhost, porta 4502. O nome do host e a porta podem ser alterados com as propriedades definidas pelo `aem.host` usuário e pelo `aem.port` usuário. |
| `autoInstallPackagePublish` | Instale o pacote de conteúdo ui.content e ui.apps com o content-package-maven-plugin no gerenciador de pacotes para a instância de publicação padrão no localhost, porta 4503. O nome do host e a porta podem ser alterados com as propriedades definidas pelo `aem.host` usuário e pelo `aem.port` usuário. |
| `autoInstallSinglePackage` | Instale o pacote de `all` conteúdo com o plug-in content-package-maven-ao gerenciador de pacote para a instância padrão do autor no localhost, porta 4502. O nome do host e a porta podem ser alterados com as propriedades definidas pelo `aem.host` usuário e pelo `aem.port` usuário. |
| `autoInstallSinglePackagePublish` | Instale o pacote de `all` conteúdo com o plug-in content-package-maven-ao gerenciador de pacote para a instância de publicação padrão no localhost, porta 4503. O nome do host e a porta podem ser alterados com as propriedades definidas pelo `aem.host` usuário e pelo `aem.port` usuário. |
| `integrationTests` | Executa os testes de integração fornecidos na instância AEM (somente para a `verify` fase) |

### Construção e instalação {#building-and-installing}

Para criar todos os módulos executados no diretório raiz do projeto, use o seguinte comando Maven.

```
mvn clean install
```

Se você tiver uma instância AEM em execução, poderá criar e empacotar o projeto inteiro e implantar no AEM com o seguinte comando Maven.

```
mvn clean install -PautoInstallPackage
```

Para implantá-lo em uma instância de publicação, execute este comando.

```
mvn clean install -PautoInstallPackagePublish
```

Como alternativa, para implantar em uma instância de publicação, execute este comando.

```
mvn clean install -PautoInstallPackage -Daem.port=4503
```

Ou para implantar somente o pacote no autor, execute este comando.

```
mvn clean install -PautoInstallBundle
```

## POM pai {#parent-pom}

A raiz `pom.xml` do projeto (`<src-directory>/<project>/pom.xml`) é conhecida como POM pai e direciona a estrutura do projeto, além de gerenciar dependências e determinadas propriedades globais do projeto.

### Propriedades do projeto global {#global-properties}

A `<properties>` seção do POM pai define várias propriedades globais que são importantes para a implantação do seu projeto em uma instância AEM, como nome de usuário/senha, nome/porta do host etc.

Essas propriedades são configuradas para implantar em uma instância AEM local, pois essa é a compilação mais comum que os desenvolvedores farão. Observe que há propriedades para implantar em uma instância do autor, bem como em uma instância de publicação. Também é aqui que as credenciais são definidas para autenticação com a instância AEM. As credenciais padrão admin:admin são usadas.

Essas propriedades são configuradas para que possam ser substituídas ao implantar ambientes de nível superior. Dessa forma, os arquivos POM não precisam ser alterados, mas variáveis como `aem.host` e `sling.password` podem ser substituídas por argumentos de linha de comando:

```
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Estrutura do módulo {#module-structure}

A `<modules>` seção do POM pai define os módulos que o projeto criará. Por padrão, o projeto cria [os módulos padrão previamente definidos](#what-you-get): core, ui.apps, ui.content, ui.testing e it.launch. Mais módulos sempre podem ser adicionados à medida que um projeto evolui.

### Dependências {#dependencies}

A `<dependencyManagement>` seção do POM pai define todas as dependências e versões de APIs usadas no projeto. As versões devem ser gerenciadas no POM pai. Submódulos como core e ui.apps não devem incluir informações sobre a versão.

#### Uber-Jar {#uber-jar}

Uma das principais dependências é o [AEM uber-jar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies). Isso incluirá todas as APIs AEM com apenas uma entrada de dependência para a versão do AEM.

>[!NOTE]
>
>Como prática recomendada, atualize a versão uber-jar para corresponder à versão do público alvo do AEM. Por exemplo, se você planeja implantar no AEM 6.4, atualize a versão do uber-jar para 6.4.0.

#### Componentes principais {#core-components}

O AEM Project Archetype, claro, aproveita os Componentes Principais.

Os Componentes principais são instalados em AEM automaticamente no modo de execução padrão e usados pelo site de amostra do WKND. Em um modo de execução [de produção](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html) (`nosamplecontent`), os Componentes principais não estão disponíveis.

Portanto, para aproveitar os componentes principais em todas as implantações, é uma prática recomendada incluí-los como parte do projeto Maven.

>[!NOTE]
>
>Cada versão dos Componentes principais é geralmente seguida de uma versão do AEM Project Archetype para que o arquétipo mais recente use a versão mais recente dos componentes principais.
>
>Entretanto, uma nova versão do arquétipo pode não seguir diretamente uma nova versão dos Componentes principais, portanto, você pode atualizar a dependência dos Componentes principais para a versão mais recente.

>[!NOTE]
>
>Os principais.wcm.components.examples são um conjunto de páginas de amostra que ilustram exemplos dos Componentes principais. Como prática recomendada, ao implantar um projeto para uso de produção, você deve remover essa dependência e a inclusão do subpacote.

## Testes {#testing}

Há três níveis de testes contidos no projeto e, por serem diferentes tipos de testes, são executados de maneiras diferentes ou em lugares diferentes.

* Teste de unidade no núcleo: Isso mostra o teste de unidade clássica do código contido no pacote. Para testar, execute:
   * `mvn clean test`
* Testes de integração do servidor: Estes executam testes semelhantes a unidades no ambiente AEM, ou seja, no servidor AEM. Para testar, execute:
   * `mvn clean verify -PintegrationTests`
* Testes Hobbes.js do cliente: Esses são testes do lado do navegador baseados em JavaScript que verificam o comportamento do lado do navegador. Para testar:
   1. Carregue AEM em seu navegador como faria para criar uma página.
   1. Abrir a página no modo [Desenvolvedor](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html)
   1. Abra o painel esquerdo e alterne para a guia **Testes** .
   1. Encontre os testes **do** MyName gerados e execute-os.

## Próximas etapas {#next-steps}

Então você construiu e instalou o AEM Project Archetype. E agora? Bem, o arquétipo é pequeno, mas consiste em muitos exemplos de recursos AEM avançados configurados de acordo com as práticas recomendadas. Use-os para indicar como você pode aproveitar esses recursos no seu projeto. Para qualquer projeto, você provavelmente precisa:

* [Personalize componentes estendendo os componentes principais existentes](/help/developing/customizing.md)
* [Adicionar modelos adicionais](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [Adapte a estrutura da localização](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [Saiba mais sobre o módulo de compilação front-end](uifrontend.md)
