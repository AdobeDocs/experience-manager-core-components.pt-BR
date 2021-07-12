---
title: Versões dos Componentes principais principais
description: Os Componentes principais são publicados como versões que podem conter mais de uma versão dos mesmos componentes principais. Este documento explica quais versões e versões são e como entender a compatibilidade com os Componentes principais e AEM.
role: Architect, Developer, Administrator, Business Practitioner
exl-id: 7d4dbe46-4013-4217-b815-cdb1462072c6
source-git-commit: 535e60115d7163b94185113a354c19cb03c402e4
workflow-type: tm+mt
source-wordcount: '2174'
ht-degree: 20%

---

# Versões dos Componentes principais principais {#core-components-versions}

A versão atual dos Componentes principais é 2.17.2 e é compatível com [AEM como um Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) e [instalações no local AEM](https://docs.adobe.com/content/help/en/experience-manager-65/user-guide/home.html).

## Histórico e compatibilidade da versão {#release-history-and-compatibility}

Os Componentes principais foram projetados para serem flexíveis e compatíveis com todas as versões de AEM compatíveis. Por causa disso, uma versão dos componentes pode conter várias versões do mesmo componente.

As tabelas a seguir ilustram a compatibilidade das versões dos Componentes principais, juntamente com as versões dos componentes em que as versões estão contidas.

### Histórico e requisitos da versão {#release-history-requirements}

A tabela a seguir, cujo conteúdo está [disponível no GitHub com detalhes completos da versão](https://github.com/adobe/aem-core-wcm-components/releases), fornece uma visão geral das versões dos Componentes principais e sua compatibilidade com AEM versões e versões do Java.

| Versão | Descrição | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | Data de lançamento |
|---|---|---|---|---|---|---|
| [2.17.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.2) | Esta versão de patch inclui uma correção para a [Camada de dados](/help/developing/data-layer/overview.md) que não está funcionando com o AEMaaCS. | 6.4.8.4+ * | 6.5.6.0+ * | Contínuo | 8, 11 | 8 de julho de 2021 |
| [2.17.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.0) | Esta versão inclui visualizações técnicas de várias versões de componentes novos que oferecem suporte a recursos do manipulador de links, bem como uma visualização técnica de um recurso de imagem em destaque para o [Componente de página.](/help/components/page.md) Várias correções de erros também são incluídas. | 6.4.8.4+ * | 6.5.6.0+ * | Contínuo | 8, 11 | 16 de junho de 2021 |
| [2.16.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.4) | Esta é uma versão de patch para corrigir um problema com o novo Manipulador de links. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 19 de maio de 2021 |
| [2.16.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.2) | Esta foi uma versão de patch corrigindo principalmente um problema com o novo Manipulador de links e adicionando um aprimoramento para suportar aplicativos de várias páginas para [PWA.](/help/components/page.md#pwa-support) | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 15 de maio de 2021 |
| [2.16.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.0) | Essa versão do se concentrava em melhorias de acessibilidade, bem como na introdução de um novo Manipulador de link para os componentes existentes. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 22 de abril de 2021 |
| [2.15.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.2) | Esta foi uma versão de patch corrigindo problemas principalmente de [compatibilidade com versões anteriores da camada de dados](/help/developing/data-layer/overview.md) e falha nos testes de TI em determinadas situações. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 16 de março de 2021 |
| [2.15.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.0) | Esta versão inclui suporte para [aplicativos web progressivos (PWA) no Componente de página](/help/components/page.md#pwa-support) e suporta a versão 2.0.0 da [Camada de dados do Adobe.](/help/developing/data-layer/overview.md) | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 23 de fevereiro de 2021 |
| [2.14.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.14.0) | Esta versão inclui novas opções para o [Componente incorporado](/help/components/embed.md) e introduz o Slug da marca no nível [página](/help/components/page.md), bem como na resolução de muitos problemas. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 9 de fevereiro de 2021 |
| [2.13.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.2) | Essa era uma versão de patch que abordava um problema com o RTE quando usado no AEMaaCS | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 16 de dezembro de 2020 |
| [2.13.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | Esta versão inclui novos recursos do Dynamic Media para o [Componente de imagem.](/help/components/image.md) | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 4 de dezembro de 2020 |
| [2.12.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | Esta foi uma versão de patch para 2.12.0, incluindo pequenas correções. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 11 de novembro de 2020 |
| [2.12.1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1) | Esta foi uma versão de patch para 2.12.0 que corrige um erro principal no [Componente de imagem.](/help/components/image.md) | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 5 de novembro de 2020 |
| [2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0) | Essa versão introduziu [um novo manipulador de formulário POST;](/help/components/forms/form-container.md#post-data) a capacidade de incluir tags CSS, Javascript e metadados [personalizados por meio de configuração sensível ao contexto;](/help/developing/including-clientlibs.md#context-aware-loading) e um utilitário `DataLayerBuilder` para [simplificar a integração da camada de dados em componentes personalizados.](/help/developing/data-layer/integrations.md#enabling-custom-components) | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 29 de outubro de 2020 |
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Esta versão introduziu o [suporte ao AMP.](/help/developing/amp.md) | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 20 de julho de 2020 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | Esta versão apresentou o [Visualizador de PDF.](/help/components/pdf-viewer.md) | 6.4.8.1+ | 6.5.5.0+ | Contínuo | 8, 11 | 17 de junho de 2020 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | Esta versão habilitou a integração com a [Camada de Dados do Cliente Adobe](/help/developing/data-layer/overview.md) e introduziu o componente [Barra de Progresso.](/help/components/progress-bar.md) | 6.4.8.0+ | 6.5.4.0+ | Contínuo | 8, 11 | 29 de maio de 2020 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Essa versão foi focada em correções com pequenos aprimoramentos. | 6.4.4.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 5 de dezembro de 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Esta versão apresentou o novo [componente Incorporado.](/help/components/embed.md) | 6.4.4.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 25 de setembro de 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Esta versão apresentou o novo componente [Fragmento de experiência.](/help/components/experience-fragment.md) | 6.4.4.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 6 de setembro de 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Esta versão apresentou o novo [Acordeão,](/help/components/accordion.md) [Botão,](/help/components/button.md) [Contêiner,](/help/components/container.md) e [Baixar componentes.](/help/components/download.md) | 6.4.2.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 25 de junho de 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Esta versão apresentou o [Componente da lista de fragmentos de conteúdo.](/help/components/content-fragment-list.md) | 6.4.2.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 7 de maio de 2019 |
| [2.3.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Essa versão focou em refinamentos da [Biblioteca de componentes,](https://aemcomponents.dev), mas também contém algumas melhorias de recursos para o [Componente de separação.](/help/components/separator.md) | 6.4.2.0+ | 6.5.0.0+ | Contínuo | 8 | 14 de março de 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Essa versão focou na [Biblioteca de componentes](https://aemcomponents.dev), bem como na introdução do novo [Componente de separação,](/help/components/separator.md), mas também contém algumas melhorias de recursos para o [Componente de imagem.](/help/components/image.md) | 6.4.2.0+ | - | - | 8 | 11 de fevereiro de 2019 |
| [2.2.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Essa versão focada principalmente em correções de erros, mas também contém algumas melhorias de recursos para o [componente carrossel.](/help/components/carousel.md) | 6.4.2.0+ | - | - | 8 | 27 de novembro de 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Esta versão introduziu o [Componente de guias](/help/components/tabs.md) e o [Componente de carrossel](/help/components/carousel.md), bem como melhorias no [Componente de imagem,](/help/components/image.md) [Componente de página,](/help/components/page.md) e [Componente de título](/help/components/title.md) e rastreamento aprimorado. | 6.4.2.0+ | - | - | 8 | 16 de outubro de 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Esta versão introduziu o [Teaser Component](/help/components/teaser.md) juntamente com aprimoramentos no [Image Component](/help/components/image.md) e várias correções de erros. | 6.4.2.0+ | - | - | 8 | 13 de julho de 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Esta foi uma versão de bugfix. | 6.4.0.0+ | - | - | 8 | 12 de junho de 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Esta versão foi adicionada com melhorias de sub-capa, correções de bugs e pequenas melhorias, incluindo suporte de inversão de imagem no [Componente de imagem.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 11 de abril de 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Essa versão foi focada principalmente em melhorias de sub-capuz, correções de erros, além de algumas melhorias secundárias no [Componente de imagem,](/help/components/image.md) [Componente de página,](/help/components/page.md) e [Componente de fragmento de conteúdo.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 7 de março de 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Esta versão introduziu o [Componente de navegação,](/help/components/navigation.md) [Componente de navegação de idioma,](/help/components/language-navigation.md) e o [Componente de pesquisa rápida](/help/components/quick-search.md) e implementou o [Sistema de estilos](/help/get-started/authoring.md#component-styling) para todos os componentes. | 6.4.0.0+ | - | - | 8 | 16 de janeiro de 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Esta versão implementa a exportação JSON em todos os componentes e introduz o [Componente do fragmento de conteúdo.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 10 de outubro de 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Esta versão adiciona várias correções para o [Componente de imagem.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 4 de agosto de 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Esta versão adiciona correções para o [Componente de página,](/help/components/page.md) [Componente de imagem,](/help/components/image.md) e várias correções e melhorias globais. | 6.4.0.0+ | - | - | 8 | 26 de abril de 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Esta versão adiciona correções para imagens GIF animadas em [Componente de imagem.](/help/components/image.md) | 6.4.0.0+ | - | - | 7 | 22 de março de 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Versão inicial dos Componentes principais. | 6.4.0.0+ | - | - | 7 | 20 de março de 2017 |

>[!NOTE]
>
>(*) Desde a versão 2.11.0, `org.apache.sling.models.impl` versão 1.4.12 ou superior é necessário (devido a [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Isso será fornecido para AEM 6.4 e 6.5 em um Service Pack futuro. Até lá, o pacote Sling Models é incluído no pacote `core.wcm.components.all`.

>[!TIP]
>
>Assim como com AEM, o Adobe recomenda que os desenvolvedores usem a [versão mais recente e as versões dos Componentes principais](https://github.com/adobe/aem-core-wcm-components/releases/latest) disponíveis, compatíveis com a versão de AEM que estão sendo executadas para se beneficiarem das correções e recursos mais atualizados.

### Versões e versões do componente {#component-versions-and-releases}

A tabela a seguir detalha quais versões de quais componentes estão contidas em quais versões dos Componentes principais.

|  | Versão 1.0.0 - 1.0.6 | Versão 1.1.0 | Versão 2.0.0 - 2.0.8 | Versão 2.1.0 | Versão 2.2.0-2.2.0 | Versão 2.3.0-2.3.2 | Versão 2.4.0 | Versão 2.5.0 | Versão 2.6.0 | Versão 2.7.0-2.8.0 | Versão 2.9.0+ |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **[Página](components/page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Título](components/title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Imagem](components/image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Lista](components/list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Caminho](components/breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Compartilhamento em mídia social](components/sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Contêineres de formulário](components/forms/form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Texto do formulário](components/forms/form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Opções de formulário](components/forms/form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulário oculto](components/forms/form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Botão de formulário](components/forms/form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Fragmento de conteúdo](components/content-fragment-component.md)** |  | Caixa de proteção | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 |
| **[Navegação](components/navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Navegação de idiomas](components/language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Busca rápida](components/quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Teaser](components/teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Guias](components/tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Carrossel](components/carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Separador](components/separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Lista de fragmentos do conteúdo](components/content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Menu sanfonado](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Botão](components/button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Container](components/container.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Download](components/download.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Fragmento de experiência](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Incorporar](components/embed.md)** |  |  |  |  |  |  |  |  |  | v1 | v1 |
| **[Barra de progresso](components/progress-bar.md)** |  |  |  |  |  |  |  |  |  |  | v1 |
| **[Visualizador de PDF](components/pdf-viewer.md)** |  |  |  |  |  |  |  |  |  |  | v1 |

## Versões e versões {#versions-and-releases}

Os Componentes principais são distribuídos por meio do GitHub. Isso permite que o Adobe adicione funcionalidades aos componentes com mais rapidez e também permita entrada da comunidade fora do ciclo de lançamento do AEM.

Os Componentes principais são disponibilizados com versões AEM definidas com as quais são compatíveis. Isso significa que uma versão AEM pode suportar várias versões ou versões dos Componentes principais. Isso dá mais flexibilidade do que os antigos Componentes da Fundação, que estavam vinculados a uma versão específica do AEM.

### Versões {#versions}

A principal iteração dos Componentes principais são as **versões**. Cada componente tem uma versão. As versões são indicadas com **v** anexadas com um número inteiro positivo diferente de zero, como v1 e v2. As versões são aumentadas apenas para alterações que não são compatíveis com versões anteriores, o que normalmente ocorre para a introdução de novos recursos e funcionalidades.

Desenvolvedores e administradores podem reconhecer versões dos componentes principais por um número em seus caminhos de tipo de recurso e nos nomes de classe Java totalmente qualificados de suas implementações. Este número de versão representa uma versão principal conforme definido por [diretrizes semânticas de controle de versão](https://semver.org/).

Para obter mais detalhes sobre as versões dos componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](developing/guidelines.md).

### Versões {#releases}

Os componentes principais são disponibilizados por meio de **versões** e [representam os artefatos publicados reais disponíveis no GitHub](https://github.com/adobe/aem-core-wcm-components/releases). As versões são indicadas com um número decimal do formato X.Y.Z e coletam todos os componentes principais juntos como um pacote entregável.

* **As** versões principais podem apresentar novas versões dos componentes existentes, juntamente com componentes totalmente novos, bem como correções de erros padrão. Isso é representado por um incremento no componente X do número da versão.
* **As** versões importantes podem introduzir uma nova funcionalidade nas versões existentes dos componentes, juntamente com correções de erros. Isso é representado por um incremento no componente Y do número de lançamento.
* **As** versões secundárias contêm apenas correções de erros. Isso é representado por um incremento no componente Z do número de lançamento.

>[!NOTE]
>
>As versões podem conter várias versões do mesmo componente.
>
>A mesma versão de um componente pode aparecer em várias versões.

## Suporte para componentes principais {#core-components-support}

Os componentes principais são parte integrante do AEM e são suportados como estão, nos mesmos termos e condições como se fossem fornecidos como parte do Início rápido.

Como outros recursos do produto, a regra geral do fim da vida útil é:

* Os componentes são anunciados como obsoletos antes de serem removidos
* Logo que possível, eles serão removidos do lançamento do AEM após o anúncio.

Isso dá aos clientes pelo menos um ciclo de lançamento para migrar para a nova versão do componente, antes que o suporte termine.

A versão de cada componente indica claramente as versões do AEM suportadas. Quando o suporte para uma versão do AEM é interrompido, o mesmo acontece com o suporte dos Componentes principais para essa versão do AEM.

Para obter detalhes sobre o suporte às personalizações de componentes, consulte a página [Personalizando componentes principais](developing/customizing.md) da versão relevante dos componentes principais.

## Suporte aos componentes da fundação {#foundation-component-support}

A ênfase do Adobe será transferida para os Componentes principais e os novos recursos continuarão a ser adicionados.

[Quase todos os componentes de base foram descontinuados com o AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) e somente correções de erros importantes serão consideradas para os componentes de base a partir de agora.
