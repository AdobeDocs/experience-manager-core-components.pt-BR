---
title: Arquétipo de projeto do AEM
description: Um modelo de projeto para aplicativos baseados no AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 0d004c90e789f23ff9e121fbd8ae11df9c9748b2
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 100%

---

# Arquétipo de projeto do AEM {#aem-project-archetype}

O Arquétipo de projeto do AEM é um modelo Maven que cria um projeto mínimo do Adobe Experience Manager (AEM) com base em práticas recomendadas, como ponto de partida para o seu site.

>[!TIP]
>
>O Arquétipo de projeto do AEM mais recente [pode ser encontrado no GitHub.](https://github.com/adobe/aem-project-archetype)

## Recursos {#resources}

* **Documentação do arquétipo (este documento):** Visão geral da arquitetura do arquétipo e de seus diferentes módulos.
   * **[Uso do Arquétipo:](using.md)** Mais detalhes sobre o uso do arquétipo e dos módulos disponíveis
   * **[Ui.frontend:](uifrontend.md)** Como usar o módulo de build front-end
* **Os seguintes tutoriais são baseados neste arquétipo:**
   * **[Site da WKND:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=pt-BR)** Aprenda a iniciar um novo site.
   * **[Aplicativo de página única da WKND:](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=pt-BR)** Aprenda a criar um aplicativo Web React ou Angular que seja totalmente autorável no AEM.

## Recursos {#features}

* **Prática recomendada:** Inicializa seu site com todas as práticas recomendadas mais recentes da Adobe.
* **Código baixo:** Edita seus modelos, crie conteúdo, implante seu CSS e seu site está pronto para entrar em funcionamento.
* **Pronto para nuvem:** Se desejar, usa o [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=pt-BR) para entrar em funcionamento em alguns dias e facilitar a escalabilidade e a manutenção.
* **Dispatcher:** Um projeto é concluído somente com uma [configuração do Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=pt-BR) que garanta velocidade e segurança.
* **Vários sites:** Se necessário, o arquétipo gera a estrutura de conteúdo para uma [configuração de vários idiomas e de várias regiões](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html?lang=pt-BR).
* **Componentes principais:** Os autores podem criar quase qualquer layout com nosso [conjunto versátil de componentes padronizados](/help/introduction.md).
* **Modelos editáveis:** Monta praticamente qualquer [modelo sem código](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=pt-BR) e define o que os autores têm permissão para editar.
* **Layout responsivo:** Em modelos ou páginas individuais, [define como os elementos fluem](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=pt-BR) para os pontos de interrupção definidos.
* **Cabeçalho e rodapé:** Monta e localiza sem código, usando os [recursos de localização dos componentes](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=pt-BR).
* **Sistema de Estilos:** Evita criar componentes personalizados permitindo que os autores [apliquem estilos diferentes](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html?lang=pt-BR) a eles.
* **Build de front-end:** Desenvolvedores de front-end podem [simular páginas do AEM](uifrontend.md#webpack-dev-server) e [criar bibliotecas de clientes](uifrontend.md) com Webpack, TypeScript e SASS.
* **Pronto para WebApp:** Para sites que usam o [React](uifrontend-react.md) ou o [Angular](uifrontend-angular.md), use o [SDK do SPA](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html?lang=pt-BR) para manter [a criação em contexto do aplicativo](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=pt-BR).
* **Ativado para comércio:** Para projetos que desejam integrar o [AEM Commerce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html?lang=pt-BR) com soluções comerciais, como [Magento](https://magento.com/br) usando os [Componentes principais do Commerce](https://github.com/adobe/aem-core-cif-components).
* **Exemplo de código:** Conheça o componente HelloWorld e modelos de amostra, servlets, filtros e schedulers.
* **Código aberto:** Se algo não está como devia, [contribua](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) para as melhorias!

## Uso {#usage}

Para gerar um projeto, ajuste a seguinte linha de comando de acordo com suas necessidades:

```shell
mvn -B org.apache.maven.plugins:maven-archetype-plugin:3.2.1:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Substitua `XX` pelo [número de versão do arquétipo ](#requirements)mais recente.
* Defina `aemVersion=cloud` para o [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=pt-BR).\
   Defina `aemVersion=6.5.0` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), ou no local.
A dependência dos Componentes principais é adicionada apenas para versões do AEM que não estão na nuvem, pois os Componentes principais são fornecidos OOTB para o AEM as a Cloud Service.
* Ajuste `appTitle="My Site"` para definir o título do site e os grupos de componentes.
* Ajuste `appId="mysite"` para definir o Maven artifactId, os nomes do componente, da configuração e da pasta de conteúdo, e os nomes da biblioteca do cliente.
* Ajuste `groupId="com.mysite"` para definir o Maven groupId e o Pacote de origem Java.
* Pesquise a lista de propriedades disponíveis para ver se há mais itens que você deseja ajustar.

## Propriedades disponíveis {#available-properties}

| Nome | Padrão | Descrição |
|---------------------------|----------------|--------------------|
| `appTitle` |  | O título do aplicativo será usado para o título do site e grupos de componentes (por exemplo, `"My Site"`). |
| `appId` |  | O nome técnico será usado para nomes de componentes, configurações e pastas de conteúdo, e para nomes de bibliotecas de clientes (por exemplo, `"mysite"`). |
| `artifactId` | *`${appId}`* | ID de artefato Maven de base (por exemplo, `"mysite"`). |
| `groupId` |  | ID de grupo Maven de base (por exemplo, `"com.mysite"`). Esse valor deve ser um [nome de pacote Java válido](https://docs.oracle.com/javase/specs/jls/se6/html/packages.html#7.7). |
| `package` | *`${groupId}`* | Java Source Package (por exemplo, `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Versão do projeto (por exemplo, `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | Versão do AEM de destino (pode ser `cloud` para o [AEM como Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=pt-BR); ou `6.5.0`, ou `6.4.4` para o [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) ou no local). |
| `sdkVersion` | `latest` | Quando for `aemVersion=cloud`, uma versão [SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html?lang=pt-BR) pode ser especificada (por exemplo, `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Inclui uma configuração de dispatcher para nuvem ou para AMS/no local, dependendo do valor de `aemVersion` (pode ser `y` ou `n`). |
| `frontendModule` | `general` | Inclui um módulo de build de front-end do Webpack que gera as bibliotecas de clientes (pode ser `general` ou `none` para sites regulares; pode ser `angular` ou `react` para um Aplicativo de página única que implementa o [Editor de SPA](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/editor-overview.html?lang=pt-BR)). |
| `language` | `en` | Código de idioma (ISO 639-1) para criar a estrutura de conteúdo de (por exemplo, `en`, `deu`). |
| `country` | `us` | Código do país (ISO 3166-1) para criar a estrutura de conteúdo de (por exemplo, `US`). |
| `singleCountry` | `y` | Inclui uma estrutura de conteúdo principal de idioma (pode ser `y` ou `n`). |
| `includeExamples` | `n` | Inclui um site de exemplo de [Biblioteca de componentes](https://www.aemcomponents.dev/) (pode ser `y` ou `n`). |
| `includeErrorHandler` | `n` | Inclui uma página de resposta 404 personalizada que será global para toda a instância (pode ser `y` ou `n`). |
| `includeCommerce` | `n` | Inclui dependências de [Componentes principais da CIF](https://github.com/adobe/aem-core-cif-components) e gera artefatos correspondentes. |
| `commerceEndpoint` |  | Necessário somente para CIF. Ponto de extremidade opcional do sistema de comércio do serviço GraphQL a ser usado (por exemplo, `https://hostname.com/grapql`). |
| `includeFormscommunications` | `n` | Inclui dependências de [Componentes principais do Forms](https://github.com/adobe/aem-core-forms-components), templates, modelos de dados de formulário, temas e gera artefatos correspondentes para programas de Comunicações do Forms. |
| `includeFormsenrollment` | `n` | Inclui dependências de [Componentes principais do Forms](https://github.com/adobe/aem-core-forms-components), templates, modelos de dados de formulário, temas e gera artefatos correspondentes para programas de Inscrição do Forms. |
| `sdkFormsVersion` | `latest` | Quando `aemVersion=cloud` e um `includeFormsenrollment=y` ou `includeFormscommunications=y`, uma versão do SDK do Forms pode ser especificada (por exemplo, `2020.12.17.02`). |
| `datalayer` | `y` | Ativa a integração com a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md). |
| `amp` | `n` | Habilita o suporte [AMP](/help/developing/amp.md) para modelos de projeto gerados. |
| `enableDynamicMedia` | `n` | Ativa os componentes básicos do Dynamic Media nas configurações de política do projeto e ativa os recursos do Dynamic Media na política do componente de Imagem principal. |
| `enableSSR` | `n` | Opção para habilitar o SSR para o projeto de front-end. |
| `precompiledScripts` | `n` | Opção para [pré-compilar](/help/developing/archetype/precompiled-bundled-scripts.md) os scripts do lado do servidor de `ui.apps` e anexá-los ao build como um artefato de pacote secundário no projeto `ui.apps`. `aemVersion` deve ser definido como `cloud`. |
| `includeFormsheadless` | `n` | Inclui dependências dos [Componentes principais do Forms](https://github.com/adobe/aem-core-forms-components), `ui.frontend.react.forms.af` e artefatos do headless. |

## Requisitos do sistema {#requirements}

| Arquétipo | AEM as a Cloud Service | AEM 6.5 | Java SE | Maven |
|---------|---------|---------|---------|---------|
| [40](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-40) | Contínuo | 6.5.7.0+ | 8, 11 | 3.3.9+ |

Configure seu ambiente de desenvolvimento local para o [SDK do AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html?lang=pt-BR) ou para [versões mais antigas do AEM](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=pt-BR).

### Problemas conhecidos {#known-issues}

Ao executar no Windows e gerar a configuração do dispatcher, você deve executar um prompt de comando elevado ou o Subsistema do Windows para Linux (consulte [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

Ao executar o arquétipo no modo interativo (sem o parâmetro `-B`), as propriedades com valores padrão não podem ser alteradas, a menos que a confirmação final seja descartada, o que então repete as perguntas incluindo as propriedades com valores padrão nas perguntas (consulte
[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obter detalhes).

Você não pode usar esse arquétipo no Eclipse ao iniciar um novo projeto com `File -> New -> Maven Project`, já que o script de pós-geração `archetype-post-generate.groovy` não será executado devido a um [problema do Eclipse.](https://bugs.eclipse.org/bugs/show_bug.cgi?id=514993) A solução alternativa é usar a linha de comando acima e, em seguida, no Eclipse usar `File -> Import -> Existing Maven Project`.

## Leitura adicional {#further-reading}

Para mais detalhes sobre o uso do arquétipo, incluindo seus benefícios, opções e como seus módulos funcionam, consulte o [documento Uso do Arquétipo](using.md).
