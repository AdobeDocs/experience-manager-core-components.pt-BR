---
title: Versões principais dos componentes
seo-title: Versões principais dos componentes
description: Os Componentes principais são publicados como lançamentos que podem conter mais de uma versão dos mesmos componentes principais. Este documento explica quais versões são versões e como entender a compatibilidade com os componentes principais e o AEM.
seo-description: Os Componentes principais são publicados como lançamentos que podem conter mais de uma versão dos mesmos componentes principais. Este documento explica quais versões são versões e como entender a compatibilidade com os componentes principais e o AEM.
uuid: a 916 a 923-8 c 5 e -456 a -84 b 5-b 52228 e 21434
contentOwner: Usuário
content-type: referência
topic-tags: introdução
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: a 3 a 98 b 2 f -65 bf -4493-82 ad -01717938 fdbc
translation-type: tm+mt
source-git-commit: 144494c03ffed068b403d80f62fdfddc73a53748

---


# Core Components Versions{#core-components-versions}

A versão atual dos Componentes principais é 2.4.0 e é compatível com o AEM 6.5. Foi lançado em maio de 2019 como uma pequena atualização da versão 2.0.0. A versão 2.0.0 introduziu novos componentes junto com atualizações v 2 de componentes existentes.

See the section [Release History and Compatibility](#versions-and-releases) of this document for more information.

You can also check out the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library.html), which showcases the current release of the Core Components and gives examples of their usage.

## Versions and Releases {#versions-and-releases}

Os Componentes principais são distribuídos via github. Isso permite que a Adobe adicione funcionalidade mais rapidamente aos componentes e também permita a entrada da comunidade fora do ciclo de lançamento do AEM.

Os Componentes principais são disponibilizados com versões AEM definidas com as quais são compatíveis. Isso significa que uma versão do AEM pode oferecer suporte a várias versões ou versões dos Componentes principais. Isso proporciona mais flexibilidade do que os antigos Componentes fundamentais, que estavam ligados a uma versão específica do AEM.

### Versões {#versions}

The major iteration of the Core Components are the **versions**. Cada componente tem uma versão. Versions are denoted with **v** appended with a nonzero, positive integer such as v1 and v2. As versões são aumentadas apenas para alterações que não são compatíveis com versões anteriores, o que é normalmente o caso da introdução dos novos recursos e funcionalidades.

Os desenvolvedores e administradores podem reconhecer versões dos componentes principais por um número em seus caminhos de tipo de recurso e nos nomes de classe Java totalmente qualificados de suas implementações. This version number represents a major version as defined by [semantic versioning guidelines](https://semver.org/).

For more details about core component versions, see the [developer documentation of the Core Components](guidelines.md).

### Releases {#releases}

The core components are made available through **releases** and [represent the actual published artifacts available on GitHub](https://github.com/adobe/aem-core-wcm-components/releases). As versões são indicadas com um número decimal do formato X.Y.Z e coletam todos os componentes principais juntos como um pacote executável.

* **As versões principais** podem apresentar novas versões de componentes existentes juntamente com componentes totalmente novos, bem como correções padrão. Isso é representado por um incremento no componente X do número da versão.

* **Versões importantes** podem apresentar uma nova funcionalidade para versões existentes de componentes juntamente com correções de erros. Isso é representado por um incremento no componente Y do número da versão.

* **As versões secundárias** contêm apenas correções de erros. Isso é representado por um incremento no componente Z do número da versão.

>[!NOTE]
>
>As versões podem conter várias versões do mesmo componente.
>
>A mesma versão de um componente pode aparecer em várias versões.

## Release History and Compatibility {#release-history-and-compatibility}

Os Componentes principais foram lançados pela primeira vez com o AEM 6.3 e foram projetados para serem flexíveis e compatíveis com todas as versões do AEM suportadas. Por isso, uma versão dos componentes pode conter várias versões do mesmo componente.

As tabelas a seguir ilustram a compatibilidade das versões dos Componentes principais juntamente com as versões de componentes contidas nas versões.

### Release History &amp; Supported AEM Versions {#release-history-supported-aem-versions}

The following table, the contents of which are [available on GitHub with full release details](https://github.com/adobe/aem-core-wcm-components/releases), gives an overview of the releases of the Core Components and their compatibility with AEM releases and Java versions.

| Versão | Descrição | AEM 6.3 | AEM 6.4 | AEM 6.5 | Java |
|---|---|---|---|---|---|
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Esta versão introduziu o componente Lista de fragmentos do conteúdo | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Esta versão foi focada em refinamentos à biblioteca de componentes, mas também contém alguns aprimoramentos de recursos para o componente Separador | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Esta versão foi focada na biblioteca de componentes, além de apresentar o novo componente de separador, mas também contém alguns aprimoramentos de recursos para o componente de imagem | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Esta versão se concentrava principalmente em correções de erros, mas também contém alguns aprimoramentos de recursos para o componente carrossel | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Componentes de tabulações e carrossel introduzidos, melhorias na imagem, página e componentes de título e rastreamento aprimorado | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Componente de Teaser introduzido, Melhorias do componente de imagem e várias correções de erros | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Versão de bugfix | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Aprimoramentos adicionais na praticidade, correções de bugs e pequenas melhorias, incluindo suporte à imagem do virar. | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Mais aprimoramentos na mola, correções de erros, mais algumas pequenas melhorias na imagem, página e componentes do fragmento do conteúdo | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Componentes de navegação, navegação de idioma e pesquisa rápida foram introduzidos. Sistema de estilo implementado para todos os componentes. | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Implementação de exportação JSON em todos os componentes, introdução ao componente Fragmento do conteúdo | 6.3.1.0 | 6.4.0.0+ | - | 8 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Várias correções para o componente Imagem | 6.3.0.0+ | 6.4.0.0+ | - | 8 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Correções do componente de página, Componente de imagem, várias correções globais e melhorias | 6.3.0.0+ | 6.4.0.0+ | - | 8 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Correções para imagens GIF animadas no componente Imagem | 6.3.0.0+ | 6.4.0.0+ | - | 7 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Lançamento inicial dos componentes principais | 6.3.0.0+ | 6.4.0.0+ | - | 7 |

>[!NOTE]
>
>As with AEM, Adobe recommends that developers use the [latest release and versions of the Core Components](https://github.com/adobe/aem-core-wcm-components/releases/latest) available that is compatible with the version of AEM that they are running in order to benefit from the most up-to-date fixes and features.

### Component Versions &amp; Releases {#component-versions-and-releases}

A tabela a seguir detalha as versões de quais componentes estão contidos nas versões dos Componentes principais.

|  | Versão 1.0.0 - 1.0.6 | Versão 1.1.0 | Versão 2.0.0 - 2.0.8 | Versão 2.1.0 | Versão 2.2.-2.2.0 | 2.3.0 |
|---|---|---|---|---|---|---|
| **[Página](page.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Título](title.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Imagem](image.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Lista](list.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Trilha de navegação](breadcrumb.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Compartilhamento em rede social](sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Contêineres de formulário](form-container.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Texto do formulário](form-text.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Opções de formulário](form-options.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Formulário oculto](form-hidden.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Botão de formulário](form-button.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Fragmento do conteúdo](content-fragment-component.md)** |  | Caixa de proteção | v1 | v1 | v1 | v1 |
| **[Navegação](navigation.md)** |  |  | v1 | v1 | v1 | v1 |
| **[Navegação de idiomas](language-navigation.md)** |  |  | v1 | v1 | v1 | v1 |
| **[Pesquisa rápida](quick-search.md)** |  |  | v1 | v1 | v1 | v1 |
| **[Teaser](teaser.md)** |  |  |  | v1 | v1 | v1 |
| **[Guias](tabs.md)** |  |  |  |  | v1 | v1 |
| **[Carrossel](carousel.md)** |  |  |  |  | v1 | v1 |
| **[Separador](separator.md)** |  |  |  |  |  | v1 |

## Documentação {#documentation}

[A criação com componentes](authoring.md) principais descreve o uso dos componentes principais e os recursos expostos aos autores de conteúdo e autores de modelos. Cada componente está documentado em detalhes.

[A Biblioteca de componentes](http://opensource.adobe.com/aem-core-wcm-components/library.html) é uma exibição da versão atual da maioria dos Componentes principais, ilustrando como eles podem ser usados.

[O Desenvolvimento dos componentes](developing.md) principais descreve os recursos técnicos dos Componentes principais, como usá-los em seus projetos, como personalizar e práticas recomendadas.

[Introdução aos componentes principais](introduction.md) fornece uma visão geral da compatibilidade dos Componentes principais em versões, casos de uso e suporte.
