---
title: Arquétipo de projeto do AEM
description: Um modelo de projeto para aplicativos baseados em AEM
translation-type: tm+mt
source-git-commit: e32521f35f33897cd72892de393073b01ad963f1
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 10%

---


# Arquétipo de projeto do AEM{#aem-project-archetype}

O AEM Project Archetype é um modelo Maven que cria um projeto Adobe Experience Manager (AEM) mínimo baseado em práticas recomendadas como ponto de partida para seu site.

>[!TIP]
>
>O AEM mais recente do Project Archetype [pode ser encontrado no GitHub](https://github.com/adobe/aem-project-archetype).

## Recursos {#resources}

* **Documentação do Archetype (este documento):** Visão geral da arquitetura do arquétipo e de seus diferentes módulos.
   * **[Usando o Archetype:](using.md)** mais detalhes sobre como usar o arquétipo e os módulos disponíveis
   * **[ui.front-end:](uifrontend.md)** Como usar o módulo de compilação front-end
* Os seguintes tutoriais têm por base este arquétipo:
   * **[Site WKND:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** saiba como start um novo site.
   * **[Aplicativo de página única WKND:](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** saiba como criar um aplicativo Web React ou Angular que seja totalmente autorável no AEM.

## Recursos {#features}

* **Prática recomendada:** Bootstrap do site com todas as práticas recomendadas mais recentes do Adobe.
* **Baixo código:** edite seus modelos, crie conteúdo, implante seu CSS e seu site está pronto para funcionar.
* **Pronto para a nuvem:** se desejar, use  [AEM como um serviço ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) da nuvem para entrar em funcionamento em poucos dias e facilitar a escalabilidade e a manutenção.
* **Dispatcher:** Um projeto é concluído somente com uma  [configuração do Dispatcher que garante ](https://docs.adobe.com/content/help/pt-BR/experience-manager-dispatcher/using/dispatcher.html) velocidade e segurança.
* **Vários sites:** se necessário, o arquétipo gera a estrutura de conteúdo para uma configuração [ ](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html) de vários idiomas e várias regiões.
* **Componentes principais:** os autores podem criar praticamente qualquer layout com nosso  [conjunto versátil de componentes](/help/introduction.md) padronizados.
* **Modelos editáveis:** monta praticamente qualquer  [modelo sem código](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) e define o que os autores têm permissão para editar.
* **Layout responsivo:** em modelos ou páginas individuais,  [defina como os elementos ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html) fluem para os pontos de interrupção definidos.
* **Cabeçalho e rodapé:** monte e localize-os sem código, usando os recursos de  [localização dos componentes](https://docs.adobe.com/content/help/br/experience-manager-core-components/using/get-started/localization.html).
* **Sistema de estilo:** evite criar componentes personalizados permitindo que os autores  [apliquem ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) estilos diferentes a eles.
* **Compilação front-end: os desenvolvedores** front-end podem  [criar páginas AEM ](uifrontend.md#webpack-dev-server) e  [criar ](uifrontend.md) bibliotecas clientes com Webpack, TypeScript e SASS.
* **WebApp-Ready:** Para sites que usam o  [](uifrontend-react.md) Reator  [Angular](uifrontend-angular.md), use o  [SPA ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/developing.html) SDK para manter a criação  [no contexto do aplicativo](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Comércio ativado:** para projetos que desejam integrar  [AEM ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/commerce/home.html) Comércio com soluções de comércio como  [](https://magento.com/) Magentousing the  [Commerce Core Components](https://github.com/adobe/aem-core-cif-components).
* **Exemplo de código:** faça check-out do componente HelloWorld e dos modelos de amostra, servlets, filtros e scheduleres.
* **Open Sourced:** Se algo não for como deveria,  [](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) contribua para as suas melhorias!

## Uso

Para gerar um projeto, ajuste a seguinte linha de comando de acordo com suas necessidades:

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=24 \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Defina `aemVersion=cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Defina `aemVersion=6.5.0` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), ou no local.
A dependência dos Componentes principais só é adicionada para versões aem não nuvem, pois os Componentes principais são fornecidos como OOTB para AEM como Cloud Service.
* Ajuste `appTitle="My Site"` para definir o título do site e os grupos de componentes.
* Ajuste `appId="mysite"` para definir a Maven artiactualId, os nomes de componentes, pastas de configuração e conteúdo, bem como os nomes da biblioteca do cliente.
* Ajuste `groupId="com.mysite"` para definir Maven groupId e Java Source Package.
* Pesquise a lista das propriedades disponíveis para ver se há mais itens que você deseja ajustar.

## Propriedades disponíveis

| Nome | Padrão | Descrição |
--------------------------|----------------|--------------------
| `appTitle` |  | O título do aplicativo será usado para o título do site e grupos de componentes (por exemplo, `"My Site"`). |
| `appId` |  | O nome técnico será usado para nomes de pastas de componentes, configurações e conteúdo, bem como para nomes de bibliotecas de clientes (por exemplo, `"mysite"`). |
| `artifactId` | *`${appId}`* | ID de artefato de Maven de base (por exemplo, `"mysite"`). |
| `groupId` |  | ID de grupo do Maven de base (por exemplo, `"com.mysite"`). |
| `package` | *`${groupId}`* | Pacote de código-fonte Java (por exemplo, `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Versão do projeto (por exemplo, `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | Público alvo AEM versão (pode ser `cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html); ou `6.5.0`, ou `6.4.4` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) ou no local). |
| `sdkVersion` | `latest` | Quando `aemVersion=cloud` uma versão [SDK](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) puder ser especificada (por exemplo, `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Inclui uma configuração de dispatcher para nuvem ou para AMS/no local, dependendo do valor de `aemVersion` (pode ser `y` ou `n`). |
| `frontendModule` | `general` | Inclui um módulo de compilação frontal do Webpack que gera as bibliotecas do cliente (pode ser `general` ou `none` para sites regulares; pode ser `angular` ou `react` para um aplicativo de página única que implemente o [SPA Editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)). |
| `language` | `en` | Código de idioma (ISO 639-1) para criar a estrutura de conteúdo de (por exemplo, `en`, `deu`). |
| `country` | `us` | Código do país (ISO 3166-1) para criar a estrutura de conteúdo de (por exemplo, `US`). |
| `singleCountry` | `y` | Inclui uma estrutura de conteúdo principal de idioma (pode ser `y` ou `n`). |
| `includeExamples` | `n` | Inclui um site de exemplo [Biblioteca de componentes](https://www.aemcomponents.dev/) (pode ser `y` ou `n`). |
| `includeErrorHandler` | `n` | Inclui uma página de resposta 404 personalizada que será global para a instância inteira (pode ser `y` ou `n`). |
| `includeCommerce` | `n` | Inclui [CIF Componentes Principais](https://github.com/adobe/aem-core-cif-components) dependências e gera artefatos correspondentes. |
| `commerceEndpoint` |  | Obrigatório apenas para CIF. Ponto de extremidade opcional do serviço GraphQL do sistema de comércio a ser usado (por exemplo, `https://hostname.com/grapql`). |
| `datalayer` | `y` | Ative a integração com [Camada de Dados do Cliente Adobe](/help/developing/data-layer/overview.md). |
| `amp` | `n` | Ative o suporte [AMP](/help/developing/amp.md) para modelos de projeto gerados. |

## Requisitos do sistema

| Arquétipo | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | Java SE | Maven |
|---------|---------|---------|---------|---------|---------|
| [24](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-24) | Contínuo | 6.5.5.0+ | 6.4.8.1+ | 8, 11 | 3.3.9+ |

Configure seu ambiente de desenvolvimento local para [AEM como um SDK Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) ou para [versões anteriores de AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Problemas conhecidos

Ao executar no Windows e gerar a configuração do dispatcher, você deve estar em execução em um prompt de comando elevado ou no Subsistema do Windows para Linux (consulte [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

Ao executar o arquétipo no modo interativo (sem o parâmetro `-B`), as propriedades com valores padrão não podem ser alteradas, a menos que a confirmação final seja descartada, o que repete as perguntas ao incluir as propriedades com valores padrão nas perguntas (consulte
[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obter detalhes).

## Leitura adicional {#further-reading}

Para obter mais detalhes sobre como usar o arquétipo, incluindo seus benefícios, opções e como seus módulos funcionam, consulte [Usando o documento Archetype.](using.md)
