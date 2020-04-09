---
title: AEM Project Archetype
description: Um modelo de projeto para aplicativos baseados no AEM
translation-type: tm+mt
source-git-commit: 2faa092a075ab0512e9bd5654884534936c0ad53

---


# AEM Project Archetype {#aem-project-archetype}

O AEM Project Archetype é um modelo Maven que cria um projeto Adobe Experience Manager (AEM) mínimo baseado em práticas recomendadas como ponto de partida para seu site.

>[!TIP]
>
>O Arquivo de projeto do AEM mais recente [pode ser encontrado no GitHub](https://github.com/adobe/aem-project-archetype).

## Recursos {#resources}

* **Documentação do Archetype (este documento):** Visão geral da arquitetura de arquétipo e seus diferentes módulos.
   * **[Usando o Archetype:](using.md)**mais detalhes sobre como usar o arquétipo e os módulos disponíveis
   * **[ui.frontenda:](uifrontend.md)**Como usar o módulo de compilação front-end
* Os seguintes tutoriais têm por base este arquétipo:
   * **[Site WKND:](https://docs.adobe.com/content/help/br/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**Saiba como start um novo site.
   * **[Aplicativo de página única WKND:](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)**Saiba como criar um aplicativo da Web React ou Angular totalmente autorável no AEM.

## Recursos {#features}

* **Prática recomendada:** Inicialize seu site com todas as práticas recomendadas mais recentes da Adobe.
* **Código baixo:** Edite seus modelos, crie conteúdo, implante seu CSS e seu site está pronto para ser lançado.
* **Pronto para nuvem:** Se desejar, use o [AEM como um serviço](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) em nuvem para entrar em funcionamento em poucos dias e facilitar a escalabilidade e a manutenção.
* **Dispatcher:** Um projeto é concluído somente com uma configuração [do](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/dispatcher.html) Dispatcher que garante velocidade e segurança.
* **Vários sites:** Se necessário, o arquétipo gera a estrutura de conteúdo para uma configuração [](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html)de vários idiomas e várias regiões.
* **Componentes principais:** Os autores podem criar praticamente qualquer layout com nosso [conjunto versátil de componentes](/help/introduction.md)padronizados.
* **Modelos editáveis:** Montar praticamente qualquer [modelo sem código](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)e definir o que os autores têm permissão para editar.
* **Layout responsivo:** Em modelos ou páginas individuais, [defina como os elementos refluem](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/responsive-layout.html) para os pontos de interrupção definidos.
* **Cabeçalho e rodapé:** Monte e localize-os sem código, usando os recursos de [localização dos componentes](https://docs.adobe.com/content/help/br/experience-manager-core-components/using/get-started/localization.html).
* **Sistema de estilo:** Evite criar componentes personalizados permitindo que os autores [apliquem estilos](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) diferentes a eles.
* **Compilação front-end:** Os dispositivos front-end podem [criar páginas](uifrontend.md#webpack-dev-server) AEM e [criar bibliotecas](uifrontend.md) de clientes com Webpack, TypeScript e SASS.
* **WebApp-Ready:** Para sites que usam [React](uifrontend-react.md) ou [Angular](uifrontend-angular.md), use o SDK [do](https://docs.adobe.com/content/help/en/experience-manager-64/developing/headless/spas/spa-architecture.html) SPA para manter a criação [no contexto do aplicativo](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Exemplo de código:** Verifique o componente HelloWorld e os modelos de amostra, servelets, filtros e scheduleres.
* **Abrir Origem:** Se algo não for como deveria, [contribua](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) para as suas melhorias!

## Uso

Para gerar um projeto, ajuste a seguinte linha de comando de acordo com suas necessidades:

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.granite.archetypes \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=23 \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Defina `aemVersion=6.5.0` para Serviços [gerenciados da](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)Adobe ou no local.
A dependência dos Componentes principais é adicionada somente para versões aem não-nuvem, já que os Componentes principais são fornecidos como OOTB para AEM como CloudService.
* Ajuste `appTitle="My Site"` para definir o título do site e os grupos de componentes.
* Ajuste `appId="mysite"` para definir a Maven artiactualId, os nomes de componentes, configurações e pastas de conteúdo, bem como os nomes da biblioteca do cliente.
* Ajuste `groupId="com.mysite"` para definir Maven groupId e o Pacote de origem Java.
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
| `aemVersion` | `6.5.0` | Versão do AEM do Público alvo (pode ser `cloud` para o [AEM como um serviço](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)em nuvem; ou `6.5.0`, `6.4.4`ou `6.3.3` para Serviços [gerenciados da](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) Adobe ou no local). |
| `sdkVersion` | `latest` | Quando é possível especificar `aemVersion=cloud` uma versão [SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) (por exemplo, `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Inclui uma configuração de despachante para nuvem ou para AMS/no local, dependendo do valor de `aemVersion` (pode ser `y` ou `n`). |
| `frontendModule` | `none` | Inclui um módulo de construção de front-end do Webpack que gera as bibliotecas do cliente (pode ser `general` ou `none` para sites regulares; pode ser `angular` ou `react` para um aplicativo de página única que implemente o Editor [](https://docs.adobe.com/content/help/en/experience-manager-65/developing/headless/spas/spa-overview.html)SPA). |
| `languageCountry` | `en_us` | Código de idioma e país para criar a estrutura de conteúdo (por exemplo, `en_us`). |
| `singleCountry` | `y` | Inclui uma estrutura de conteúdo do idioma mestre (pode ser `y`, ou `n`). |
| `includeExamples` | `y` | Inclui um site de exemplo da Biblioteca [de](https://www.aemcomponents.dev/) componentes (pode ser `y`, ou `n`). |
| `includeErrorHandler` | `n` | Inclui uma página de resposta 404 personalizada que será global para a instância inteira (pode ser `y` ou `n`). |

## Requisitos do sistema

| Arquétipo | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | AEM 6.3 | Java SE | Maven |
---------|---------|---------|---------|---------|---------|---------
| [23](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-23) | Contínuo | 6.5.0.0+ | 6.4.4.0+ | 6.3.3.4+ | 8, 11 | 3.3.9+ |

Configure seu ambiente de desenvolvimento local para o [AEM como um SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) de serviço em nuvem ou para versões [anteriores do AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Problemas conhecidos

Ao executar no Windows e gerar a configuração do dispatcher, você deve estar em execução em um prompt de comando elevado ou no Subsistema do Windows para Linux (consulte [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

Ao executar o arquétipo no modo interativo (sem o `-B` parâmetro), as propriedades com valores padrão não podem ser alteradas, a menos que a confirmação final seja descartada, o que repete as perguntas ao incluir as propriedades com valores padrão nas perguntas (consulte[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obter detalhes).

## Leitura adicional {#further-reading}

Para obter mais detalhes sobre como usar o arquétipo, incluindo seus benefícios, opções e como seus módulos funcionam, consulte [Usando o documento Archetype.](using.md)