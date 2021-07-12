---
title: Arquétipo de projeto do AEM
description: Um modelo de projeto para aplicativos baseados em AEM
feature: Componentes principais, Arquétipo de projeto AEM
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 9%

---

# Arquétipo de projeto do AEM {#aem-project-archetype}

O AEM Project Archetype é um modelo Maven que cria um projeto Adobe Experience Manager (AEM) mínimo, baseado em práticas recomendadas, como ponto de partida para seu site.

>[!TIP]
>
>O Arquétipo de Projeto do AEM mais recente [pode ser encontrado no GitHub.](https://github.com/adobe/aem-project-archetype)

## Recursos {#resources}

* **Documentação do arquétipo (este documento):** visão geral da arquitetura do arquétipo e de seus diferentes módulos.
   * **[Usando o Arquétipo:](using.md)** mais detalhes sobre o uso do arquétipo e dos módulos disponíveis
   * **[ui.frontend:](uifrontend.md)** como usar o módulo de build front-end
* Os seguintes tutoriais são baseados nesse arquétipo:
   * **[Site WKND: ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** saiba como iniciar um novo site.
   * **[Aplicativo de página única WKND: ](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** saiba como criar um aplicativo Web React ou Angular que seja totalmente autorável no AEM.

## Recursos {#features}

* **Prática recomendada:** Bootstrap seu site com todas as práticas recomendadas mais recentes do Adobe.
* **Código baixo:** edite seus modelos, crie conteúdo, implante seu CSS e seu site está pronto para entrar em funcionamento.
* **Pronto para nuvem:** se desejar, use o  [AEM as a Cloud ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) Service para entrar em funcionamento em alguns dias e facilitar a escalabilidade e a manutenção.
* **Dispatcher:** um projeto é concluído somente com uma configuração  [ ](https://docs.adobe.com/content/help/pt-BR/experience-manager-dispatcher/using/dispatcher.html) do Dispatcher que garante a velocidade e a segurança.
* **Vários sites:** se necessário, o arquétipo gera a estrutura de conteúdo para uma configuração de  [vários idiomas e de várias regiões](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html).
* **Componentes principais:** os autores podem criar quase qualquer layout com nosso  [conjunto versátil de componentes padronizados](/help/introduction.md).
* **Modelos editáveis:** monte praticamente qualquer  [modelo sem código](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) e defina o que os autores têm permissão para editar.
* **Layout responsivo:** em modelos ou páginas individuais,  [defina como os elementos ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html) fluem para os pontos de interrupção definidos.
* **Cabeçalho e rodapé:** monta-os e os localiza sem código, usando os recursos de  [localização dos componentes](https://docs.adobe.com/content/help/br/experience-manager-core-components/using/get-started/localization.html).
* **Sistema de estilos:** evite criar componentes personalizados permitindo que os autores  [apliquem ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) estilos diferentes a eles.
* **Build de front-end:** os desenvolvedores de front-end podem  [modelar ](uifrontend.md#webpack-dev-server) páginas de AEM e  [criar ](uifrontend.md) bibliotecas de clientes com Webpack, TypeScript e SASS.
* **Pronto para WebApp-Ready:** para sites que usam o  [](uifrontend-react.md) Reator  [Angular](uifrontend-angular.md), use o  [SPA ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/developing.html) SDKpara manter a criação  [em contexto do aplicativo](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Ativado para comércio:** para projetos que desejam integrar  [AEM ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/commerce/home.html) Commerce com soluções comerciais, como  [](https://magento.com/) Magentousing the  [Commerce Core Components](https://github.com/adobe/aem-core-cif-components).
* **Exemplo de código:** faça o check-out do componente HelloWorld e dos modelos de amostra, servlets, filtros e agendadores.
* **Fonte aberta:** se algo não é como deveria,  [](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) contribua para as melhorias!

## Uso {#usage}

Para gerar um projeto, ajuste a seguinte linha de comando de acordo com suas necessidades:

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Substitua `XX` pelo número de versão mais recente [do arquétipo.](#requirements)
* Defina `aemVersion=cloud` para [AEM como um Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Defina `aemVersion=6.5.0` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), ou no local.
A dependência dos Componentes principais é adicionada apenas para versões do aem que não estão na nuvem, pois os Componentes principais são fornecidos OTB para AEM como Cloud Service.
* Ajuste `appTitle="My Site"` para definir o título do site e os grupos de componentes.
* Ajuste `appId="mysite"` para definir o Maven artifactId, os nomes do componente, da configuração e da pasta de conteúdo, bem como os nomes da biblioteca do cliente.
* Ajuste `groupId="com.mysite"` para definir o Maven groupId e o Pacote de Origem Java.
* Pesquise a lista de propriedades disponíveis para ver se há mais itens que você deseja ajustar.

## Propriedades disponíveis {#available-properties}

| Nome | Padrão | Descrição |
|---------------------------|----------------|--------------------|
| `appTitle` |  | O título do aplicativo será usado para o título do site e grupos de componentes (por exemplo, `"My Site"`). |
| `appId` |  | O nome técnico será usado para nomes de componentes, configurações e pastas de conteúdo, bem como para nomes de bibliotecas de clientes (por exemplo, `"mysite"`). |
| `artifactId` | *`${appId}`* | ID de artefato Maven de base (por exemplo, `"mysite"`). |
| `groupId` |  | ID de grupo Maven de base (por exemplo, `"com.mysite"`). |
| `package` | *`${groupId}`* | Pacote de origem Java (por exemplo, `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Versão do projeto (por exemplo, `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | Versão de AEM de destino (pode ser `cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html); ou `6.5.0`, ou `6.4.4` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) ou no local). |
| `sdkVersion` | `latest` | Quando `aemVersion=cloud` uma versão [SDK](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) pode ser especificada (por exemplo, `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Inclui uma configuração de dispatcher para nuvem ou para AMS/no local, dependendo do valor de `aemVersion` (pode ser `y` ou `n`). |
| `frontendModule` | `general` | Inclui um módulo de compilação de frontend do Webpack que gera as bibliotecas de clientes (pode ser `general` ou `none` para sites regulares; pode ser `angular` ou `react` para um Aplicativo de página única que implementa o [Editor de SPA](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)). |
| `language` | `en` | Código de idioma (ISO 639-1) para criar a estrutura de conteúdo de (por exemplo, `en`, `deu`). |
| `country` | `us` | Código do país (ISO 3166-1) para criar a estrutura de conteúdo de (por exemplo, `US`). |
| `singleCountry` | `y` | Inclui uma estrutura de conteúdo principal de idioma (pode ser `y` ou `n`). |
| `includeExamples` | `n` | Inclui um site de exemplo [Biblioteca de componentes](https://www.aemcomponents.dev/) (pode ser `y` ou `n`). |
| `includeErrorHandler` | `n` | Inclui uma página de resposta 404 personalizada que será global para toda a instância (pode ser `y` ou `n`). |
| `includeCommerce` | `n` | Inclui [Componentes principais da CIF](https://github.com/adobe/aem-core-cif-components) dependências e gera artefatos correspondentes. |
| `commerceEndpoint` |  | Necessário somente para CIF. Ponto de extremidade opcional do sistema de comércio do serviço GraphQL a ser usado (por exemplo, `https://hostname.com/grapql`). |
| `datalayer` | `y` | Ative a integração com [Adobe Client Data Layer](/help/developing/data-layer/overview.md). |
| `amp` | `n` | Habilite o suporte [AMP](/help/developing/amp.md) para modelos de projeto gerados. |
| `enableDynamicMedia` | `n` | Ativa os componentes básicos do Dynamic Media nas configurações de política do projeto e ativa os recursos do Dynamic Media na política do componente de Imagem principal. |
| `enableSSR` | `n` | Opção para habilitar o SSR para o projeto front-end |

## Requisitos do sistema {#requirements}

| Arquétipo | AEM as a Cloud Service | AEM 6.5 | Java SE | Maven |
|---------|---------|---------|---------|---------|
| [28º](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-28) | Contínuo | 6.5.7.0+ | 8, 11 | 3.3.9+ |

Configure seu ambiente de desenvolvimento local para [AEM como um SDK do Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) ou para [versões mais antigas do AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Problemas conhecidos {#known-issues}

Ao executar no Windows e gerar a configuração do dispatcher, você deve estar executando um prompt de comando elevado ou o Subsistema do Windows para Linux (consulte [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

Ao executar o arquétipo no modo interativo (sem o parâmetro `-B` ), as propriedades com valores padrão não podem ser alteradas, a menos que a confirmação final seja descartada, o que então repete as perguntas incluindo as propriedades com valores padrão nas perguntas (consulte
[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obter detalhes).

Você não pode usar esse arquétipo no Eclipse ao iniciar um novo projeto com `File -> New -> Maven Project` já que o script de pós-geração `archetype-post-generate.groovy` não será executado devido a um problema [Eclipse.](https://bugs.eclipse.org/bugs/show_bug.cgi?id=514993) A solução alternativa é usar a linha de comando acima e, em seguida, no Eclipse use  `File -> Import -> Existing Maven Project`.

## Leitura adicional {#further-reading}

Para obter mais detalhes sobre o uso do arquétipo, incluindo seus benefícios, opções e como seus módulos funcionam, consulte o documento [Usando o Arquétipo.](using.md)
