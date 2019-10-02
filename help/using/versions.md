---
title: Versões dos componentes principais
seo-title: Versões dos componentes principais
description: Os Componentes principais são publicados como versões que podem conter mais de uma versão dos mesmos componentes principais. Este documento explica quais versões e versões são e como entender a compatibilidade com os Componentes principais e o AEM.
seo-description: Os Componentes principais são publicados como versões que podem conter mais de uma versão dos mesmos componentes principais. Este documento explica quais versões e versões são e como entender a compatibilidade com os Componentes principais e o AEM.
uuid: a916a923-8c5e-456a-84b5-b52228e21434
contentOwner: Usuário
content-type: referência
topic-tags: introdução
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: a3a98b2f-65bf-4493-82ad-01717938fdbc
translation-type: tm+mt
source-git-commit: 97f1461b57079806f9f96d325d9b763538e32127

---


# Versões dos componentes principais{#core-components-versions}

A versão atual dos Componentes principais é 2.7.0 e é compatível com o AEM 6.5. Ela foi lançada em setembro de 2019 como uma atualização importante para a versão 2.0.0. A versão 2.0.0 introduziu novos componentes juntamente com atualizações v2 de componentes existentes.

Consulte a seção Histórico de [versão e Compatibilidade](#versions-and-releases) deste documento para obter mais informações.

Você também pode conferir a Biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library.html)componentes, que mostra a versão atual dos Componentes principais e fornece exemplos de seu uso.

## Versões e versões {#versions-and-releases}

Os Componentes principais são distribuídos pelo GitHub. Isso permite que a Adobe adicione funcionalidade aos componentes mais rapidamente e também permita a entrada da comunidade fora do ciclo de lançamento do AEM.

Os Componentes principais são disponibilizados com as versões definidas do AEM com as quais são compatíveis. Isso significa que uma versão do AEM pode suportar várias versões ou versões dos Componentes principais. Isso proporciona mais flexibilidade do que os componentes básicos anteriores, que estavam vinculados a uma versão específica do AEM.

### Versões {#versions}

As principais iterações dos Componentes principais são as **versões**. Cada componente tem uma versão. As versões são denotadas com **v** anexada com um número inteiro positivo diferente de zero, como v1 e v2. As versões são aumentadas somente para alterações que não sejam compatíveis com versões anteriores, o que normalmente acontece com a introdução de novos recursos e funcionalidades.

Os desenvolvedores e administradores podem reconhecer as versões dos componentes principais por um número em seus caminhos de tipo de recurso e nos nomes de classe Java totalmente qualificados de suas implementações. Esse número de versão representa uma versão principal, conforme definido pelas diretrizes [de controle de versão](https://semver.org/)semântica.

Para obter mais detalhes sobre as versões dos componentes principais, consulte a documentação do [desenvolvedor dos Componentes](guidelines.md)principais.

### Versões {#releases}

Os componentes principais são disponibilizados por meio de **versões** e [representam os artefatos publicados reais disponíveis no GitHub](https://github.com/adobe/aem-core-wcm-components/releases). As versões são denotadas com um número decimal do formato X.Y.Z e coletam todos os componentes principais como um pacote entregável.

* **As versões** principais podem apresentar novas versões dos componentes existentes, juntamente com componentes totalmente novos e correções padrão de erros. This is represented by an increment in the X component of the release number.
* **Important releases** can introduce new functionality to existing versions of components along with bug fixes. This is represented by an increment in the Y component of the release number.
* **Minor releases** contain only bug fixes. This is represented by an increment in the Z component of the release number.

>[!NOTE]
>
>Releases can contain multiple versions of the same component.
>
>A mesma versão de um componente pode aparecer em várias versões.

## Release History and Compatibility {#release-history-and-compatibility}

The Core Components were first released with AEM 6.3 and are designed to be flexible and compatible with all supported AEM versions. Because of this a release of the components can contain multiple versions of the same component.

The following tables illustrate the compatibility of the releases of the Core Components along with which component versions are contained in which releases.

### Release History &amp; Supported AEM Versions {#release-history-supported-aem-versions}

The following table, the contents of which are available on GitHub with full release details, gives an overview of the releases of the Core Components and their compatibility with AEM releases and Java versions.[](https://github.com/adobe/aem-core-wcm-components/releases)

| Release | Descrição | AEM 6.3 | AEM 6.4 | AEM 6.5 | Java | Release Date |
|---|---|---|---|---|---|---|
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | This release introduced the new Embed component | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 8, 11 | 25 de setembro de 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Esta versão apresentou o novo componente Fragmento de experiência | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 8, 11 | 6 de setembro de 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Esta versão apresentou os novos componentes Acordeão, Botão, Contêiner e Download. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | 25 de junho de 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Esta versão apresentou o componente Lista de fragmentos do conteúdo | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | 7 de maio de 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Esta versão focou nos refinamentos da biblioteca de componentes, mas também contém algumas melhorias de recursos para o Componente separador | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8 | 14 de março de 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Esta versão focou na biblioteca de componentes, bem como na introdução do novo componente separador, mas também contém algumas melhorias de recursos para o Componente de imagem | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 11 de fevereiro de 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Esta versão focou principalmente em correções de erros, mas também contém algumas melhorias de recursos para o componente Carousel | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 27 de novembro de 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Componentes de guias e carrossel introduzidos, melhorias nos componentes de imagem, página e título e rastreamento aprimorado | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 16 de outubro de 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Componente Teaser introduzido, melhorias no componente de imagem e inúmeras correções de erros | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 13 de julho de 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Versão do Bugfix | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 12 de junho de 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Aprimoramentos adicionais de sub-capa, correções de erros e pequenos aprimoramentos, incluindo suporte a flip de imagem. | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 11 de abril de 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | A maioria das melhorias sub-capa, correções de erros, além de algumas melhorias secundárias nos componentes de imagem, página e fragmento de conteúdo | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 7 de março de 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Os componentes Navegação, Navegação de idioma e Pesquisa rápida foram introduzidos. Sistema de estilo implementado para todos os componentes. | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 16 de janeiro de 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Implementação da exportação JSON em todos os componentes, introdução do componente Fragmento do conteúdo | 6.3.1.0 | 6.4.0.0+ | - | 8 | 10 de outubro de 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Várias correções para o componente Imagem | 6.3.0.0+ | 6.4.0.0+ | - | 8 | 4 August 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Fixes of Page Component, Image Component, various global fixes and improvements | 6.3.0.0+ | 6.4.0.0+ | - | 8 | 26 April 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Fixes for animated GIF images in Image component | 6.3.0.0+ | 6.4.0.0+ | - | 7 | 22 March 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Initial release of Core Components | 6.3.0.0+ | 6.4.0.0+ | - | 7 | 20 March 2017 |

>[!NOTE]
>
>As with AEM, Adobe recommends that developers use the latest release and versions of the Core Components available that is compatible with the version of AEM that they are running in order to benefit from the most up-to-date fixes and features.[](https://github.com/adobe/aem-core-wcm-components/releases/latest)

### Component Versions &amp; Releases {#component-versions-and-releases}

The following table details which versions of which components are contained in which releases of the Core Components.

|  | Release 1.0.0 - 1.0.6 | Release 1.1.0 | Release 2.0.0 - 2.0.8 | Release 2.1.0 | Release 2.2.0-2.2.0 | Versão 2.3.0-2.3.2 | Versão 2.4.0 | Versão 2.5.0 | Versão 2.6.0 | Versão 2.7.0+ |
|---|---|---|---|---|---|---|---|---|---|---|
| **[Página](page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Título](title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Imagem](image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Lista](list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Trilha](breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Compartilhamento em rede social](sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Contêineres de formulário](form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Texto do formulário](form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Opções de formulário](form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulário oculto](form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Botão de formulário](form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Fragmento do conteúdo](content-fragment-component.md)** |  | Caixa de proteção | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Navegação](navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Navegação de idiomas](language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Pesquisa rápida](quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Teaser](teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Guias](tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Carrossel](carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Separador](separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Lista de fragmento do conteúdo](content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Acordeão](accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Botão](button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Contêiner](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Download](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Fragmento de experiência](separator.md)** |  |  |  |  |  |  |  |  | v1 | v1 |
| **[Incorporar](separator.md)** |  |  |  |  |  |  |  |  |  | v1 |

## Documentação {#documentation}

[Authoring with Core Components describes the usage of the core components and the features that are exposed to content authors and template authors. ](authoring.md) Each component is documented in detail.

[Component Library is a showcase of the current version of most Core Components, illustrating how they can be used.](http://opensource.adobe.com/aem-core-wcm-components/library.html)

[Developing Core Components describes the technical capabilities of the Core Components, how to use them in your projects, how to customize, and best practices.](developing.md)

[A Introdução](introduction.md) aos componentes principais fornece uma visão geral da compatibilidade dos componentes principais entre versões, casos de uso e suporte.

[The WKND Tutorial is a great step-by-step introduction to developing for AEM including using the Core Components.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)
