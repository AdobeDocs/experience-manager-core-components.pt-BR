---
title: Uso do Arquétipo de projeto do AEM
description: Instruções de uso detalhadas para o Arquétipo de projeto do AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
source-git-commit: 017790c5a0e53ba6203a5c3d5ddebcce9c00cb01
workflow-type: tm+mt
source-wordcount: '2193'
ht-degree: 93%

---

# Arquétipo de projeto do AEM {#aem-project-archetype}

O Arquétipo de projeto do AEM cria um projeto mínimo do Adobe Experience Manager com base em práticas recomendadas como ponto de partida para seus próprios projetos AEM. As propriedades que devem ser fornecidas ao usar esse arquétipo permitem especificar os nomes de todas as partes desse projeto, bem como controlar determinados recursos opcionais.

## Por que usar o arquétipo {#why-use-the-archetype}

Usar o Arquétipo de projeto do AEM estabelece o caminho para a criação de um projeto do AEM com base em práticas recomendadas. Basta digitar algumas teclas. Com o uso do arquétipo, todas as partes já estarão em vigor, de modo que, embora o projeto resultante seja mínimo, ele já implementa todos os [recursos principais](#what-you-get) do AEM. Assim, tudo o que você precisa fazer é criar sobre o arquétipo e expandir.

Obviamente, há vários elementos envolvidos para que um projeto do AEM seja satisfatório. Mas o Arquétipo de projeto do AEM oferece uma base sólida e é altamente recomendado para qualquer projeto do AEM.

## Introdução {#getting-started}

Com o arquétipo de projeto fica mais fácil começar a desenvolver no AEM. E há várias maneiras de dar os primeiros passos.

* Tutorial do WKND - Uma ótima introdução para desenvolver no AEM, incluindo como aproveitar o arquétipo. Em [Introdução ao AEM Sites - Tutorial do WKND](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html), há um exemplo prático que o orienta a usar o arquétipo para implementar um projeto simples.
* Tutorial de eventos do WKND - Se você estiver particularmente interessado no desenvolvimento de aplicativos de página única (SPA) no AEM, verifique o [tutorial de eventos dedicados do WKND](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=pt-BR).
* Baixe e comece sozinho! - Você pode baixar facilmente o arquétipo de projeto atual disponível no GitHub e criar seu primeiro projeto [seguindo as etapas simples abaixo](#how-to-use-the-archetype).

## O que você ganha usando o arquétipo {#what-you-get}

O Arquétipo do AEM é composto de módulos:

* **[core](core.md)**: um pacote Java que contém todas as funcionalidades principais, como serviços OSGi, ouvintes e schedulers, e código Java relacionado a componentes, como servlets e filtros de solicitação.
* **[it.tests](ittests.md)**: testes de integração baseados em Java.
* **[ui.apps](uiapps.md)**: contém as partes `/apps` e `/etc` do projeto, ou seja, clientlibs, componentes e modelos de JS e CSS.
* **[ui.content](uicontent.md)**: contém conteúdo de amostra usando os componentes do módulo ui.apps.
* **ui.config**: contém configurações OSGi específicas para runmode para o projeto.
* **[ui.frontend.general](uifrontend.md)**: **(opcional)** contém os artefatos necessários para usar o módulo de build de front-end baseado no Webpack geral.
* **[ui.frontend.react](uifrontend-react.md)**: **(opcional)** contém os artefatos necessários ao usar o arquétipo para criar projetos de SPA com base no React.
* **[ui.frontend.angular](uifrontend-angular.md)**: **(opcional)** contém os artefatos necessários ao usar o arquétipo para criar projetos de SPA com base no Angular.
* **[ui.tests](uitests.md)**: contém testes de UI com base no Selenium.
* **all**: um pacote de conteúdo único que incorpora todos os módulos compilados (pacotes e pacotes de conteúdo) incluindo qualquer dependência de fornecedor.
* **analyse**: executa a análise no projeto, que fornece validação adicional para implantar no AEM as a Cloud Service.

![](/help/assets/archetype-structure.png)

Os módulos do Arquétipo do AEM representados em Maven são implantados no AEM como pacotes de conteúdo que representam o aplicativo, o conteúdo e os pacotes OSGi necessários.

## Como usar o arquétipo {#how-to-use-the-archetype}

Para usar o arquétipo, primeiro é necessário criar um projeto, que gera os módulos em uma estrutura de arquivo local, conforme [descrito anteriormente](#what-you-get). Como parte da geração do projeto, várias propriedades para o seu projeto podem ser definidas: nome do projeto, versão etc.

Desenvolver o projeto com o Maven cria os artefatos (pacotes e pacotes OSGi), que podem ser implantados no AEM. Comandos e perfis Maven adicionais podem ser usados para implantar os artefatos do projeto em uma instância do AEM.

### Criação de um projeto {#create-project}

Para começar, você pode simplesmente usar a [extensão AEM Eclipse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/eclipse.html?lang=pt-BR), seguir o assistente Novo projeto e escolher **Amostra de projeto de vários módulos do AEM** para usar uma versão lançada do arquétipo.

É claro que você também pode invocar o Maven direto.

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

* Defina `XX` para o [número de versão](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) do Arquétipo de projeto do AEM mais recente.
* Defina `aemVersion=cloud` para o [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html).\
   Defina `aemVersion=6.5.0` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), ou no local.
A dependência dos Componentes principais é adicionada apenas para versões do AEM que não estão na nuvem, pois os Componentes principais são fornecidos OOTB para o AEM as a Cloud Service.
* Ajuste `appTitle="My Site"` para definir o título do site e os grupos de componentes.
* Ajuste `appId="mysite"` para definir o Maven artifactId, os nomes do componente, da configuração e da pasta de conteúdo, e os nomes da biblioteca do cliente.
* Ajuste `groupId="com.mysite"` para definir o Maven groupId e o Pacote de origem Java.
* Pesquise a lista de propriedades disponíveis para ver se há mais itens que você deseja ajustar.

>[!NOTE]
>
>A prática recomendada é adicionar o perfil `adobe-public` ao arquivo Maven `settings.xml` para adicionar automaticamente o repo.adobe.com ao processo de build do maven.
>
>Um exemplo de POM [pode ser encontrado aqui](https://helpx.adobe.com/br/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### Propriedades {#properties}

As seguintes propriedades estão disponíveis ao criar um projeto usando o arquétipo.

| Nome | Padrão | Descrição |
|---------------------------|----------------|--------------------|
| `appTitle` |  | O título do aplicativo será usado para o título do site e grupos de componentes (por exemplo, `"My Site"`). |
| `appId` |  | O nome técnico será usado para nomes de componentes, configurações e pastas de conteúdo, e para nomes de bibliotecas de clientes (por exemplo, `"mysite"`). |
| `artifactId` | *`${appId}`* | ID de artefato Maven de base (por exemplo, `"mysite"`). |
| `groupId` |  | ID de grupo Maven de base (por exemplo, `"com.mysite"`). |
| `package` | *`${groupId}`* | Java Source Package (por exemplo, `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Versão do projeto (por exemplo, `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | Versão do AEM de destino (pode ser `cloud` para o [AEM como Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html); ou `6.5.0`, ou `6.4.4` para o [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) ou no local). |
| `sdkVersion` | `latest` | Quando for `aemVersion=cloud`, uma versão [SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) pode ser especificada (por exemplo, `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Inclui uma configuração de dispatcher para nuvem ou para AMS/no local, dependendo do valor de `aemVersion` (pode ser `y` ou `n`). |
| `frontendModule` | `general` | Inclui um módulo de build de front-end do Webpack que gera as bibliotecas de clientes (pode ser `general` ou `none` para sites regulares; pode ser `angular` ou `react` para um Aplicativo de página única que implementa o [Editor de SPA](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)). |
| `language` | `en` | Código de idioma (ISO 639-1) para criar a estrutura de conteúdo de (por exemplo, `en`, `deu`). |
| `country` | `us` | Código do país (ISO 3166-1) para criar a estrutura de conteúdo de (por exemplo, `US`). |
| `singleCountry` | `y` | Inclui uma estrutura de conteúdo principal de idioma (pode ser `y` ou `n`). |
| `includeExamples` | `n` | Inclui um site de exemplo de [Biblioteca de componentes](https://www.aemcomponents.dev/) (pode ser `y` ou `n`). |
| `includeErrorHandler` | `n` | Inclui uma página de resposta 404 personalizada que será global para toda a instância (pode ser `y` ou `n`). |
| `includeCommerce` | `n` | Inclui dependências de [Componentes principais da CIF](https://github.com/adobe/aem-core-cif-components) e gera artefatos correspondentes. |
| `commerceEndpoint` |  | Necessário somente para CIF. Ponto de extremidade opcional do sistema de comércio do serviço GraphQL a ser usado (por exemplo, `https://hostname.com/grapql`). |
| `datalayer` | `y` | Ativa a integração com a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md). |
| `amp` | `n` | Habilita o suporte [AMP](/help/developing/amp.md) para modelos de projeto gerados. |
| `enableDynamicMedia` | `n` | Ativa os componentes básicos do Dynamic Media nas configurações de política do projeto e ativa os recursos do Dynamic Media na política do componente de Imagem principal. |
| `enableSSR` | `n` | Opção para habilitar o SSR para o projeto de front-end. |
| `precompiledScripts` | `n` | Opção para [pré-compilar](/help/developing/archetype/precompiled-bundled-scripts.md) os scripts do lado do servidor de `ui.apps` e anexá-los à compilação como um artefato de pacote secundário no projeto `ui.apps`. `aemVersion` deve ser definido como  `cloud`. |

>[!NOTE]
>
> Se o arquétipo for executado no modo interativo pela primeira vez, as propriedades com valores padrão não poderão ser alteradas (consulte [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obter mais detalhes). O valor pode ser alterado quando a confirmação da propriedade no final for negada e o questionário for repetido, ou passando o parâmetro na linha de comando (por exemplo, `-DoptionIncludeExamples=n`).

>[!NOTE]
>
>Ao executar no Windows e gerar a configuração do dispatcher, você deve estar executando em um prompt de comando elevado ou no Subsistema do Windows para Linux (consulte [problema 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Perfis {#profiles}

O projeto maven gerado oferece suporte a diferentes perfis de implantação ao executar `mvn install`.

| ID do perfil | Descrição |
| --------------------------|------------------------------|
| `autoInstallBundle` | Instale o pacote principal com o maven-sling-plugin no console felix |
| `autoInstallPackage` | Instale o pacote de conteúdo ui.content e ui.apps com o content-package-maven-plugin para o gerenciador de pacotes para a instância padrão do autor no localhost, porta 4502. O nome do host e a porta podem ser alterados com as propriedades `aem.host` e `aem.port` definidas pelo usuário. |
| `autoInstallPackagePublish` | Instale o pacote de conteúdo ui.content e ui.apps com o content-package-maven-plugin no gerenciador de pacotes tornar a instância de publicação padrão no localhost, porta 4503. O nome do host e a porta podem ser alterados com as propriedades `aem.host` e `aem.port` definidas pelo usuário. |
| `autoInstallSinglePackage` | Instale o pacote de conteúdo `all` com o content-package-maven-plugin no gerenciador de pacotes para a instância do autor padrão no localhost, porta 4502. O nome do host e a porta podem ser alterados com as propriedades `aem.host` e `aem.port` definidas pelo usuário. |
| `autoInstallSinglePackagePublish` | Instale o pacote de conteúdo `all` com o content-package-maven-plugin no gerenciador de pacotes para tornar a instância de publicação padrão no localhost, porta 4503. O nome do host e a porta podem ser alterados com as propriedades `aem.host` e `aem.port` definidas pelo usuário. |
| `integrationTests` | Executa os testes de integração fornecidos na instância do AEM (somente para a fase `verify`) |
| `precompiledScripts` | Definido automaticamente quando o projeto foi gerado com a propriedade `precompiledScripts` definida como `y`. O perfil está ativo por padrão e gera um pacote OSGi dentro de `ui.apps` com os scripts pré-compilados, que serão incluídos no pacote de conteúdo `all`. O perfil pode ser desativado com `-DskipScriptPrecompilation=true`. |

### Criação e instalação {#building-and-installing}

Para criar todos os módulos executados no diretório raiz do projeto, use o seguinte comando Maven.

```shell
mvn clean install
```

Se você tiver uma instância do AEM em execução, poderá criar e empacotar todo o projeto e implantar no AEM com o seguinte comando Maven.

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

Ou, para implantar somente o pacote para o autor, execute este comando.

```shell
mvn clean install -PautoInstallBundle
```

## POM principal {#parent-pom}

O `pom.xml` na raiz do projeto (`<src-directory>/<project>/pom.xml`) é conhecido como POM principal e direciona a estrutura do projeto, bem como gerencia dependências e determinadas propriedades globais do projeto.

### Propriedades globais do projeto {#global-properties}

A seção `<properties>` do POM principal define várias propriedades globais são importantes para a implantação do seu projeto em uma instância do AEM, como nome de usuário/senha, nome/porta do host etc.

Essas propriedades são configuradas para implantar em uma instância do AEM local, pois essa é a build mais comum que os desenvolvedores farão. Observe que há propriedades para implantar em uma instância de autor, bem como uma instância de publicação. Também é aqui que as credenciais são definidas para autenticação com a instância do AEM. As credenciais padrão admin:admin são usadas.

Essas propriedades são configuradas para que possam ser substituídas ao implantar em ambientes de nível superior. Dessa forma, os arquivos POM não precisam ser alterados, mas variáveis como `aem.host` e `sling.password` podem ser substituídas por argumentos de linha de comando:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Estrutura do módulo {#module-structure}

A seção `<modules>` do POM principal define os módulos que o projeto criará. Por padrão, o projeto cria [os módulos padrão definidos anteriormente](#what-you-get): core, ui.apps, ui.content, ui.tests e it.launcher. Mais módulos sempre podem ser adicionados à medida que um projeto evolui.

### Dependências {#dependencies}

A seção `<dependencyManagement>` do POM principal todas as dependências e versões das APIs usadas no projeto. As versões devem ser gerenciadas no POM principal. Submódulos como core e ui.apps não devem incluir informações de versão.

#### Uber-Jar {#uber-jar}

Uma das dependências principais é o [AEM Java API Jar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html). Isso incluirá todas as APIs AEM com apenas uma única entrada de dependência para a versão do AEM.

>[!NOTE]
>
>Como prática recomendada, atualize a versão uber-jar para corresponder à versão de destino do AEM. Por exemplo, se você planeja implantar no AEM 6.4, é necessário atualizar a versão do uber-jar para 6.4.0.

#### Componentes principais {#core-components}

Claro que o Arquétipo de projeto do AEM aproveita os Componentes principais.

Os Componentes principais são instalados no AEM automaticamente no modo de execução padrão e usados pelo site da WKND de amostra. Em um [modo de execução de produção](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#runmodes) (`nosamplecontent`), os Componentes principais não estão disponíveis.

Portanto, para aproveitar os Componentes principais em todas as implantações, a prática recomendada é incluí-los como parte do projeto Maven.

>[!NOTE]
>
>Cada versão dos Componentes principais é geralmente seguida por uma versão do Arquétipo de projeto do AEM. Assim, ambos usam sua versão mais recente.
>
>No entanto, uma nova versão do arquétipo pode não seguir diretamente uma nova versão dos Componentes principais, por isso seria bom atualizar a dependência dos Componentes principais para a versão mais recente.

>[!NOTE]
>
>O core.wcm.components.examples é um conjunto de páginas de exemplo que ilustra exemplos dos Componentes principais. Como prática recomendada, ao implantar um projeto para uso de produção, você deve remover essa dependência e a inclusão do subpacote.

## Testes {#testing}

Existem três níveis de testes contidos no projeto e, como são diferentes tipos de testes, são executados de maneiras diferentes ou em lugares diferentes.

* Teste de unidade no núcleo: mostra o teste de unidade clássica do código contido no pacote. Para testar, execute:
   * `mvn clean test`
* Testes de integração do lado do servidor: executam testes semelhantes a unidades no ambiente do AEM, ou seja, no servidor do AEM. Para testar, execute:
   * `mvn clean verify -PintegrationTests`
* Testes Hobbes.js do lado do cliente: são testes do lado do navegador baseados em JavaScript que verificam o comportamento do lado do navegador. Para testar:
   1. Carregue o AEM no navegador da mesma maneira que você faria para criar uma página.
   1. Abra a página no [Modo de desenvolvedor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/developer-mode.html)
   1. Abra o painel esquerdo e alterne para a guia **Testes**.
   1. Localize os **Testes MyName** gerados e execute-os.

## Próximas etapas {#next-steps}

Então você criou e instalou o Arquétipo de projeto do AEM. E agora? O arquétipo é pequeno, mas consiste em vários exemplos de recursos avançados do AEM configurados de acordo com as práticas recomendadas. Use-os para indicar como você pode aproveitar esses recursos no seu projeto. Para qualquer projeto, você provavelmente precisará:

* [Personalizar componentes estendendo os componentes principais existentes](/help/developing/customizing.md)
* [Acrescentar modelos adicionais](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [Adaptar a estrutura de localização](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/preparation.html)
* [Saiba mais sobre o módulo de build de front-end](uifrontend.md)
