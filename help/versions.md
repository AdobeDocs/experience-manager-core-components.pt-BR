---
title: Versões dos Componentes principais principais
description: Os Componentes principais são publicados como versões que podem conter mais de uma versão dos mesmos componentes principais. Este documento explica quais versões e versões são e como entender a compatibilidade com os Componentes principais e AEM.
translation-type: tm+mt
source-git-commit: 3c5749d6660af1ad94f4911f261951e0369fa139
workflow-type: tm+mt
source-wordcount: '1971'
ht-degree: 21%

---


# Versões dos Componentes principais principais {#core-components-versions}

A versão atual dos Componentes principais é 2.15.0 e é compatível com [AEM como instalações Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) e [AEM](https://docs.adobe.com/content/help/en/experience-manager-65/user-guide/home.html) no local.

## Histórico e compatibilidade da versão {#release-history-and-compatibility}

Os componentes principais foram projetados para serem flexíveis e compatíveis com todas as versões de AEM suportadas. Por isso, uma versão dos componentes pode conter várias versões do mesmo componente.

As tabelas a seguir ilustram a compatibilidade das versões dos Componentes principais, juntamente com as versões dos componentes nas quais as versões estão contidas.

### Histórico e requisitos da versão {#release-history-requirements}

A tabela a seguir, cujo conteúdo está [disponível no GitHub com detalhes completos da versão](https://github.com/adobe/aem-core-wcm-components/releases), fornece uma visão geral das versões dos Componentes principais e sua compatibilidade com versões AEM e versões Java.

| Versão | Descrição | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | Data de lançamento |
|---|---|---|---|---|---|---|
| [2,15,0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.0) | Esta versão inclui suporte para aplicativos da Web progressivos no [Componente de página](/help/components/page.md) e suporta a versão 2.0.0 da [Camada de Dados de Adobe.](/help/developing/data-layer/overview.md) | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 23 de fevereiro de 2021 |
| [2,14,0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.14.0) | Esta versão inclui novas opções para [Incorporar componente](/help/components/embed.md) e apresenta o espaçador de marca no nível [page](/help/components/page.md), além de abordar muitos problemas. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 9 de fevereiro de 2021 |
| [2,13,2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.2) | Esta foi uma versão de correção que solucionou um problema com o RTE quando usado no AEMaaCS | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 16 de dezembro de 2020 |
| [2,13,0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | Esta versão inclui novos recursos do Dynamic Media para o [Componente de imagem.](/help/components/image.md) | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 4 de dezembro de 2020 |
| [2,12,2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | Esta foi uma versão de correção para 2.12.0, incluindo correções secundárias. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 11 de novembro de 2020 |
| [2,12,1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1) | Esta foi uma versão de correção para 2.12.0 que corrige um erro principal no [Componente de imagem.](/help/components/image.md) | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 5 de novembro de 2020 |
| [2,12,0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0) | Esta versão introduziu [um novo manipulador de formulários POST;](/help/components/forms/form-container.md#post-data) a capacidade de incluir tags personalizadas de CSS, Javascript e metadados [através de configuração sensível ao contexto;](/help/developing/including-clientlibs.md#context-aware-loading) e um utilitário `DataLayerBuilder` para [simplificar a integração da camada de dados em componentes personalizados.](/help/developing/data-layer/integrations.md#enabling-custom-components) | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 29 de outubro de 2020 |
| [2,11,0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Esta versão introduziu o suporte [AMP.](/help/developing/amp.md) | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 20 de julho de 2020 |
| [2,10,0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | Esta versão apresentou o componente [Visualizador de PDF.](/help/components/pdf-viewer.md) | 6.4.8.1+ | 6.5.5.0+ | Contínuo | 8, 11 | 17 de junho de 2020 |
| [2,9,0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | Esta versão habilitou a integração com a [Adobe Client Data Layer](/help/developing/data-layer/overview.md) e introduziu o componente [Progress Bar.](/help/components/progress-bar.md) | 6.4.8.0+ | 6.5.4.0+ | Contínuo | 8, 11 | 29 de maio de 2020 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Esta versão focou em correções com pequenos aprimoramentos. | 6.4.4.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 5 de dezembro de 2019 |
| [2,7,0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Esta versão apresentou o novo componente [Incorporar.](/help/components/embed.md) | 6.4.4.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 25 de setembro de 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Esta versão apresentou o novo componente [Fragmento de experiência.](/help/components/experience-fragment.md) | 6.4.4.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 6 de setembro de 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Esta versão apresentou o novo [Acordeão,](/help/components/accordion.md) [Botão,](/help/components/button.md) [Container,](/help/components/container.md) e [Transferir componentes.](/help/components/download.md) | 6.4.2.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 25 de junho de 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Esta versão apresentou o [Componente de Lista do Fragmento de Conteúdo.](/help/components/content-fragment-list.md) | 6.4.2.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 7 de maio de 2019 |
| [2.3.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Esta versão focou-se em refinamentos para a [Biblioteca de Componentes,](https://aemcomponents.dev) mas também contém algumas melhorias de recursos para o [Componente Separador.](/help/components/separator.md) | 6.4.2.0+ | 6.5.0.0+ | Contínuo | 8 | 14 de março de 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Esta versão focou-se na [Biblioteca de Componentes](https://aemcomponents.dev), bem como na introdução do novo [Componente Separador,](/help/components/separator.md) mas também contém algumas melhorias de recursos para o [Componente de Imagem.](/help/components/image.md) | 6.4.2.0+ | - | - | 8 | 11 de fevereiro de 2019 |
| [2.2.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Esta versão focou principalmente em correções de erros, mas também contém algumas melhorias de recursos para o [Componente carrossel.](/help/components/carousel.md) | 6.4.2.0+ | - | - | 8 | 27 de novembro de 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Esta versão introduziu o [Componente de Guias](/help/components/tabs.md) e o [Componente de Carrossel](/help/components/carousel.md), bem como melhorias no [Componente de Imagem,](/help/components/image.md) [Componente de Página,](/help/components/page.md) e [Componente de Título](/help/components/title.md) e acompanhamento aprimorado. | 6.4.2.0+ | - | - | 8 | 16 de outubro de 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Esta versão introduziu o [Teaser Component](/help/components/teaser.md) juntamente com melhorias no [Componente de imagem](/help/components/image.md) e várias correções de erros. | 6.4.2.0+ | - | - | 8 | 13 de julho de 2018 |
| [2,0,8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Esta foi uma versão de correção. | 6.4.0.0+ | - | - | 8 | 12 de junho de 2018 |
| [2,0,6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Esta versão adicionou melhorias, correções de bugs e pequenos aprimoramentos, incluindo suporte de flip de imagem no [Componente de imagem.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 11 de abril de 2018 |
| [2,0,4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Esta versão concentra-se principalmente em melhorias de sub-capa, correções de erros, além de algumas melhorias secundárias no [Componente de imagem,](/help/components/image.md) [Componente de página,](/help/components/page.md) e [Componente de fragmento de conteúdo.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 7 de março de 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Esta versão introduziu o [Componente de Navegação,](/help/components/navigation.md) [Componente de Navegação de Idioma,](/help/components/language-navigation.md) e o [Componente de Pesquisa Rápida](/help/components/quick-search.md) e implementou o [Sistema de Estilo](/help/get-started/authoring.md#component-styling) para todos os componentes. | 6.4.0.0+ | - | - | 8 | 16 de janeiro de 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Esta versão implementa a exportação JSON em todos os componentes e introduz o [Componente de Fragmento de Conteúdo.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 10 de outubro de 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Esta versão adiciona várias correções para o [Componente de imagem.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 4 de agosto de 2017 |
| [1.0.4.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Esta versão adiciona correções para o [Componente de página,](/help/components/page.md) [Componente de imagem,](/help/components/image.md) e várias correções e melhorias globais. | 6.4.0.0+ | - | - | 8 | 26 de abril de 2017 |
| [1.0.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Esta versão adiciona correções para imagens GIF animadas em [Componente de imagem.](/help/components/image.md) | 6.4.0.0+ | - | - | 7 | 22 de março de 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Versão inicial dos Componentes principais. | 6.4.0.0+ | - | - | 7 | 20 de março de 2017 |

>[!NOTE]
>
>(*) Desde a versão 2.11.0, `org.apache.sling.models.impl` versão 1.4.12 ou superior é necessário (devido a [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Isso será fornecido para AEM 6.4 e 6.5 em um Service Pack futuro. Até então, o pacote Sling Models é incluído no pacote `core.wcm.components.all`.

>[!TIP]
>
>Assim como AEM, a Adobe recomenda que os desenvolvedores usem a versão [mais recente e as versões dos Componentes principais](https://github.com/adobe/aem-core-wcm-components/releases/latest) disponíveis, compatíveis com a versão dos AEM que estão em execução, para se beneficiarem das correções e dos recursos mais atualizados.

### Versões e versões do componente {#component-versions-and-releases}

A tabela a seguir detalha quais versões de quais componentes estão contidos em quais versões dos Componentes principais.

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

Os Componentes principais são distribuídos pelo GitHub. Isso permite que o Adobe adicione funcionalidade aos componentes mais rapidamente e também permita a entrada da comunidade fora do ciclo de lançamento do AEM.

Os Componentes principais são disponibilizados com versões AEM definidas com as quais são compatíveis. Isso significa que uma versão AEM pode suportar várias versões ou versões dos Componentes principais. Isso dá mais flexibilidade do que os antigos Componentes da Fundação, que estavam ligados a uma versão específica do AEM.

### Versões {#versions}

A principal iteração dos Componentes principais são as **versões**. Cada componente tem uma versão. As versões são denotadas com **v** anexadas com um número inteiro positivo diferente de zero, como v1 e v2. As versões são aumentadas somente para alterações que não sejam compatíveis com versões anteriores, o que normalmente acontece com a introdução de novos recursos e funcionalidades.

Os desenvolvedores e administradores podem reconhecer as versões dos componentes principais por um número em seus caminhos de tipo de recurso e nos nomes de classe Java totalmente qualificados de suas implementações. Este número de versão representa uma versão principal, conforme definido por [diretrizes semânticas de controle de versão](https://semver.org/).

Para obter mais detalhes sobre as versões dos componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](developing/guidelines.md).

### Versões {#releases}

Os componentes principais são disponibilizados por meio de **versões** e [representam os artefatos realmente publicados disponíveis no GitHub](https://github.com/adobe/aem-core-wcm-components/releases). As versões são denotadas com um número decimal do formato X.Y.Z e coletam todos os componentes principais como um pacote entregável.

* **As principais** versões podem apresentar novas versões dos componentes existentes, juntamente com componentes totalmente novos e correções de erros padrão. Isso é representado por um incremento no componente X do número da versão.
* **As** versões importantes podem introduzir novas funcionalidades nas versões existentes dos componentes, juntamente com correções de erros. Isso é representado por um incremento no componente Y do número da versão.
* **As** versões secundárias contêm apenas correções de erros. Isso é representado por um incremento no componente Z do número da versão.

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

A ênfase do Adobe mudou para os componentes principais e os novos recursos continuarão a ser adicionados.

[Quase todos os componentes básicos foram descontinuados com AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) e somente correções importantes serão consideradas para os componentes básicos a partir de agora.
