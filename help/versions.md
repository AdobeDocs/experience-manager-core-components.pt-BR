---
title: Versões dos Componentes principais
description: Os Componentes principais são publicados como versões que podem conter mais de uma versão dos mesmos componentes principais. Este documento explica quais são as versões e como entender a compatibilidade com os Componentes principais e o AEM.
role: Architect, Developer, Admin, User
exl-id: 7d4dbe46-4013-4217-b815-cdb1462072c6
source-git-commit: 12fef6732ba53beeb7b3354335005f459321da96
workflow-type: ht
source-wordcount: '2689'
ht-degree: 100%

---

# Versões dos Componentes principais {#core-components-versions}

A versão atual dos componentes principais é a 2.20.6, e é compatível com o [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=pt-BR) e instalações [locais do AEM](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html?lang=pt-BR).

## Histórico e compatibilidade da versão {#release-history-and-compatibility}

Os Componentes principais foram projetados para serem flexíveis e compatíveis com todas as versões do AEM. Por causa disso, uma versão dos componentes pode conter várias versões do mesmo componente.

As tabelas a seguir ilustram a compatibilidade das versões dos Componentes principais, juntamente com as versões dos componentes em que elas estão contidas.

### Histórico e requisitos da versão {#release-history-requirements}

A tabela a seguir, cujo conteúdo está [disponível no GitHub com detalhes completos da versão](https://github.com/adobe/aem-core-wcm-components/releases), fornece uma visão geral das versões dos Componentes principais e sua compatibilidade com as versões do AEM e do Java.

| Versão | Descrição | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | Data de lançamento |
|---|---|---|---|---|---|---|
| [2.20.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.6) | Esta versão de correção corrige um problema com o novo [Componente de índice.](/help/components/tableofcontents.md) | - | 6.5.13.0+ * | Contínuo | 8, 11 | 7 de julho de 2022 |
| --- | --- | --- | --- | --- | --- | --- |
| [2.20.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.4) | Esta versão de correção corrige um problema com o novo [Componente de índice.](/help/components/tableofcontents.md) | - | 6.5.13.0+ * | Contínuo | 8, 11 | 29 de junho de 2022 |
| --- | --- | --- | --- | --- | --- | --- |
| [2.20.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.2) | Esta é uma versão de correção que corrige um problema no novo [serviço de entrega de ativos otimizados para a Web](/help/developing/web-optimized-image-delivery.md) do AEMaaCS. | - | 6.5.13.0+ * | Contínuo | 8, 11 | 20 de junho de 2022 |
| [2.20.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.0) | Esta versão adiciona um novo [Componente de índice](/help/components/tableofcontents.md), compatibilidade com o [serviço de entrega de ativos otimizados para a Web](/help/developing/web-optimized-image-delivery.md) do AEMaaCS e inclui correções de erros. | - | 6.5.13.0+ * | Contínuo | 8, 11 | 9 de junho de 2022 |
| [2.19.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.19.0) | Este lançamento adiciona uma nova versão ao [Componente de pesquisa](/help/components/quick-search.md) e recursos ao [Componente do botão](/help/components/button.md), assim como muitas melhorias de acessibilidade e correções de erros. | - | 6.5.10.0+ * | Contínuo | 8, 11 | 7 de abril de 2022 |
| [2.18.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.8) | Esta versão corrige um problema no AEMaaCS. | - | 6.5.10.0+ * | Contínuo | 8, 11 | 17 de março de 2022 |
| [2.18.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.6) | Esta é uma versão de correção. | - | 6.5.10.0+ * | Contínuo | 8, 11 | 3 de março de 2022 |
| [2.18.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.0) | Essa versão principal dos componentes principais introduz um novo manipulador de links para novas versões de vários componentes, juntamente com muitas melhorias de acessibilidade e correções de erros. | - | 6.5.10.0+ * | Contínuo | 8, 11 | 16 de fevereiro de 2022 |
| [2.17.14](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | Esta é a versão de correção. | 6.4.8.4+ * | 6.5.6.0+ * | Contínuo | 8, 11 | 13 de dezembro de 2021 |
| [2.17.12](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | Esta é uma versão de correção que corrige uma regressão introduzida na versão anterior. | 6.4.8.4+ * | 6.5.6.0+ * | Contínuo | 8, 11 | 1 de outubro de 2021 |
| [2.17.10](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.10) | Esse patch melhora os componentes [Lista](/help/components/list.md) e [Navegação](/help/components/navigation.md) para exibir o URL externo para destinos de redirecionamento, habilita a herança de imagens da página para a próxima v2 do componente [Teaser](/help/components/teaser.md) e contém outras correções de erros. | 6.4.8.4+ * | 6.5.6.0+ * | Contínuo | 8, 11 | 31 de agosto de 2021 |
| [2.17.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.8) | Esta é uma versão de patch para corrigir uma alteração incompatível com versões anteriores que foi introduzida anteriormente. | 6.4.8.4+ * | 6.5.6.0+ * | Contínuo | 8, 11 | 2 de agosto de 2021 |
| [2.17.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.6) | Esta versão de patch adiciona suporte para mapas de site para Páginas e inclui várias melhorias de acessibilidade. | 6.4.8.4+ * | 6.5.6.0+ * | Contínuo | 8, 11 | 29 de julho de 2021 |
| [2.17.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.2) | Esta versão de patch inclui uma correção para a [Camada de dados](/help/developing/data-layer/overview.md) que não está funcionando com o AEMaaCS. | 6.4.8.4+ * | 6.5.6.0+ * | Contínuo | 8, 11 | 8 de julho de 2021 |
| [2.17.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.0) | Esta versão inclui visualizações técnicas de várias versões de novos componentes que oferecem suporte a recursos do manipulador de links, bem como uma visualização técnica de um recurso de imagem em destaque para o [componente de Página.](/help/components/page.md) Várias correções de bugs também estão incluídas. | 6.4.8.4+ * | 6.5.6.0+ * | Contínuo | 8, 11 | 16 de junho de 2021 |
| [2.16.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.4) | Esta é uma versão de patch para corrigir um problema com o novo Manipulador de links. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 19 de maio de 2021 |
| [2.16.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.2) | Esta foi uma versão de patch corrigindo principalmente um problema com o novo Manipulador de links e adicionando um aprimoramento para suportar aplicativos de várias páginas para [PWA](/help/components/page.md#pwa-support). | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 15 de maio de 2021 |
| [2.16.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.0) | Essa versão se concentrou em melhorias de acessibilidade, bem como na introdução de um novo Manipulador de links para os componentes existentes. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 22 de abril de 2021 |
| [2.15.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.2) | Essa foi uma versão de patch corrigindo problemas principalmente de compatibilidade com versões anteriores da [Camada de dados](/help/developing/data-layer/overview.md) e falha nos testes de TI em determinadas situações. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 16 de março de 2021 |
| [2.15.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.0) | Essa versão inclui suporte para [aplicativos web progressivos (PWA) no componente de Página](/help/components/page.md#pwa-support) e é compatível com a versão 2.0.0 da [Camada de dados da Adobe](/help/developing/data-layer/overview.md). | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 23 de fevereiro de 2021 |
| [2.14.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.14.0) | Essa versão inclui novas opções para o [Componente de Incorporação](/help/components/embed.md) e introduz o Brand Slug no nível da [página](/help/components/page.md), bem como a resolução de muitos problemas. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 9 de fevereiro de 2021 |
| [2.13.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.2) | Essa foi uma versão de patch que abordou um problema com o RTE quando usado no AEMaaCS | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 16 de dezembro de 2020 |
| [2.13.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | Essa versão inclui novos recursos do Dynamic Media para o [componente de Imagem](/help/components/image.md). | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 4 de dezembro de 2020 |
| [2.12.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | Essa foi uma versão de patch para 2.12.0, incluindo pequenas correções. | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 11 de novembro de 2020 |
| [2.12.1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1) | Essa foi uma versão de patch para 2.12.0 que corrige um erro principal no [componente de Imagem](/help/components/image.md). | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 5 de novembro de 2020 |
| [2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0) | Essa versão apresentou [um novo manipulador de formulário POST](/help/components/forms/form-container.md#post-data); a capacidade de incluir CSS personalizado, JavaScript e [tags de metadados pela configuração com reconhecimento de contexto](/help/developing/including-clientlibs.md#context-aware-loading); e um utilitário `DataLayerBuilder` para [simplificar a integração da camada de dados em componentes personalizados](/help/developing/data-layer/integrations.md#enabling-custom-components). | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 29 de outubro de 2020 |
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Essa versão introduziu o [suporte ao AMP](/help/developing/amp.md). | 6.4.8.1+ * | 6.5.5.0+ * | Contínuo | 8, 11 | 20 de julho de 2020 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | Essa versão apresentou o [componente de Visualizador de PDF](/help/components/pdf-viewer.md). | 6.4.8.1+ | 6.5.5.0+ | Contínuo | 8, 11 | 17 de junho de 2020 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | Essa versão habilitou a integração com a [Camada de Dados de clientes Adobe](/help/developing/data-layer/overview.md) e introduziu o [componente de Barra de progresso](/help/components/progress-bar.md). | 6.4.8.0+ | 6.5.4.0+ | Contínuo | 8, 11 | 29 de maio de 2020 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Essa versão enfocou correções com pequenos aprimoramentos. | 6.4.4.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 5 de dezembro de 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Essa versão apresentou o novo [componente de Incorporação](/help/components/embed.md). | 6.4.4.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 25 de setembro de 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Essa versão apresentou o novo [componente de Fragmento de experiência](/help/components/experience-fragment.md). | 6.4.4.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 6 de setembro de 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Essa versão apresentou os novos [componentes Acordeão](/help/components/accordion.md), [Botão](/help/components/button.md), [Container](/help/components/container.md) e [Download](/help/components/download.md). | 6.4.2.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 25 de junho de 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Essa versão apresentou o [componente de Lista de fragmentos de conteúdo](/help/components/content-fragment-list.md). | 6.4.2.0+ | 6.5.0.0+ | Contínuo | 8, 11 | 7 de maio de 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Essa versão enfocou refinamentos da [Biblioteca de componentes](https://aemcomponents.dev), mas também contém algumas melhorias de recursos para o [componente Separador](/help/components/separator.md). | 6.4.2.0+ | 6.5.0.0+ | Contínuo | 8 | 14 de março de 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Essa versão focou a [Biblioteca de componentes](https://aemcomponents.dev) e introduziu o novo [Componente de Separador](/help/components/separator.md), mas também contém algumas melhorias de recursos para o [Componente de Imagem](/help/components/image.md). | 6.4.2.0+ | - | - | 8 | 11 de fevereiro de 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Essa versão focou principalmente correções de bugs, mas também contém algumas melhorias de recursos para o [componente Carrossel](/help/components/carousel.md). | 6.4.2.0+ | - | - | 8 | 27 de novembro de 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Essa versão introduziu o [componente de Guias](/help/components/tabs.md) e o [componente Carrossel](/help/components/carousel.md), melhorias no [componente de Imagem](/help/components/image.md), [componente de Página](/help/components/page.md) e [componente de Título](/help/components/title.md), e rastreamento aprimorado. | 6.4.2.0+ | - | - | 8 | 16 de outubro de 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Esta versão introduziu o [componente de Teaser](/help/components/teaser.md) juntamente com aprimoramentos no [componente de Imagem](/help/components/image.md) e várias correções de erros. | 6.4.2.0+ | - | - | 8 | 13 de julho de 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Essa foi uma versão de correção de bug. | 6.4.0.0+ | - | - | 8 | 12 de junho de 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Essa versão foi adicionada com melhorias internas, correções de bugs e pequenos aprimoramentos, incluindo suporte de inversão de imagem no [componente de Imagem](/help/components/image.md). | 6.4.0.0+ | - | - | 8 | 11 de abril de 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Essa versão focou principalmente melhorias internas, correções de erros, além de alguns aprimoramentos secundários no [componente de Imagem](/help/components/image.md), [componente de Página](/help/components/page.md) e [componente de Fragmento de conteúdo](/help/components/content-fragment-component.md). | 6.4.0.0+ | - | - | 8 | 7 de março de 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Essa versão introduziu o [componente de Navegação](/help/components/navigation.md), [componente de Navegação por idiomas](/help/components/language-navigation.md) e o [componente de Pesquisa rápida](/help/components/quick-search.md), e implementou o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) para todos os componentes. | 6.4.0.0+ | - | - | 8 | 16 de janeiro de 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Essa versão implementa a exportação JSON em todos os componentes e introduz o [componente de Fragmento de conteúdo](/help/components/content-fragment-component.md). | 6.4.0.0+ | - | - | 8 | 10 de outubro de 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Essa versão adiciona várias correções para o [componente de Imagem](/help/components/image.md). | 6.4.0.0+ | - | - | 8 | 4 de agosto de 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Essa versão adiciona correções para o [componente de Página](/help/components/page.md), [componente de Imagem](/help/components/image.md) e várias correções e melhorias gerais. | 6.4.0.0+ | - | - | 8 | 26 de abril de 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Essa versão adiciona correções para imagens GIF animadas no [componente de Imagem](/help/components/image.md). | 6.4.0.0+ | - | - | 7 | 22 de março de 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Versão inicial dos Componentes principais. | 6.4.0.0+ | - | - | 7 | 20 de março de 2017 |

>[!NOTE]
>
>(*) Desde a versão 2.11.0, a versão `org.apache.sling.models.impl` 1.4.12 ou superior é necessária (devido a [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Isso será fornecido futuramente para o AEM 6.4 e 6.5 em um Service Pack. Até lá, o pacote Sling Models estará incluído no pacote `core.wcm.components.all`.

>[!TIP]
>
>Assim como o AEM, a Adobe recomenda que os desenvolvedores usem a [versão mais recente dos Componentes principais](https://github.com/adobe/aem-core-wcm-components/releases/latest) disponíveis, que sejam compatíveis com a versão do AEM que está sendo executada para que se beneficiem das correções e recursos mais atualizados.

### Versões dos componentes {#component-versions-and-releases}

A tabela a seguir detalha que versões de quais componentes estão contidas em quais versões dos Componentes principais.

|  | Versão 1.0.0 - 1.0.6 | Versão 1.1.0 | Versão 2.0.0 - 2.0.8 | Versão 2.1.0 | Versão 2.2.0 - 2.2.0 | Versão 2.3.0 - 2.3.2 | Versão 2.4.0 | Versão 2.5.0 | Versão 2.6.0 | Versão 2.7.0 - 2.8.0 | Versão 2.9.0 - 2.17.14 | Versão 2.18.0 | Versão 2.19.0 | Versão 2.20.0+ |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **[Página](components/page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Título](components/title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Imagem](components/image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Lista](components/list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Navegação estrutural](components/breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Compartilhamento em redes sociais](components/sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, descontinuado | v1, descontinuado | v1, descontinuado |
| **[Container de formulário](components/forms/form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Texto de formulário](components/forms/form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Opções de formulário](components/forms/form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulário oculto](components/forms/form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Botão de formulário](components/forms/form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Fragmento de conteúdo](components/content-fragment-component.md)** |  | Sandbox | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Navegação](components/navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Navegação de idiomas](components/language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Pesquisa rápida](components/quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 |
| **[Teaser](components/teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Guias](components/tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Carrossel](components/carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Separador](components/separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Lista de fragmentos de conteúdo](components/content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Acordeão](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Botão](components/button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Container](components/container.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Download](components/download.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Fragmento de experiência](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Incorporação](components/embed.md)** |  |  |  |  |  |  |  |  |  | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Barra de progresso](components/progress-bar.md)** |  |  |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Visualizador de PDF](components/pdf-viewer.md)** |  |  |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Índice](components/tableofcontents.md)** |  |  |  |  |  |  |  |  |  |  |  |  |  | v1 |

## Versões e lançamentos {#versions-and-releases}

Os Componentes principais são distribuídos pelo GitHub. Isso permite que a Adobe adicione funcionalidades aos componentes com mais rapidez e permita contribuições da comunidade fora do ciclo de lançamento do AEM.

Os Componentes principais são disponibilizados com versões AEM definidas com as quais são compatíveis. Isso significa que uma versão do AEM pode ser compatível com várias versões dos componentes principais.

### Versões {#versions}

A principal iteração dos Componentes principais são as **versões**. Cada componente tem uma versão. As versões são indicadas com **v** anexadas com um número inteiro positivo diferente de zero, como v1 e v2. As versões são aumentadas apenas para alterações que não são compatíveis com versões anteriores, o que normalmente ocorre para a introdução de novos recursos e funcionalidades.

Desenvolvedores e administradores podem reconhecer versões dos componentes principais por um número em seus caminhos de tipo de recurso e nos nomes de classe Java totalmente qualificados de suas implementações. Esse número de versão representa uma versão principal conforme definido pelas [diretrizes de controle de versão semântico](https://semver.org/).

Para mais detalhes sobre as versões dos componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](developing/guidelines.md).

### Versões {#releases}

Os Componentes principais são disponibilizados por meio de **versões** e [representam os artefatos publicados reais disponíveis no GitHub](https://github.com/adobe/aem-core-wcm-components/releases). As versões são indicadas com um número decimal do formato `X.Y.Z` e coletam todos os componentes principais juntos como um pacote de entrega.

* **Versões principais** introduzem componentes totalmente novos, melhorias às versões existentes de componentes, bem como correções de erros padrão. Isso é representado por um incremento no componente `X` do número da versão.
* **Versões secundárias** introduzem novos componentes, novas funcionalidades às versões existentes de componentes, bem como correções de erros. Isso é representado por um incremento no componente `Y` do número da versão.
* **As versões de correção** contêm apenas correções de erros. Isso é representado por um incremento no componente `Z` do número da versão.

>[!NOTE]
>
>As versões podem conter várias versões do mesmo componente.
>
>A mesma versão de um componente pode aparecer em várias versões.

## Suporte para componentes principais {#core-components-support}

Por serem uma parte integrante do AEM, os componentes principais são compatíveis nos mesmos termos e condições, como se fossem fornecidos como parte do Quickstart.

Como outros recursos do produto, a regra geral do fim da vida útil é:

* Os componentes são anunciados como obsoletos antes de serem removidos
* Logo que possível, eles serão removidos do lançamento do AEM após o anúncio.

Isso dá aos clientes pelo menos um ciclo de lançamento para migrar para a nova versão do componente, antes que o suporte termine.

A versão de cada componente indica claramente as versões do AEM suportadas. Quando o suporte para uma versão do AEM é interrompido, o mesmo acontece com o suporte dos Componentes principais para essa versão do AEM.

Para obter detalhes sobre o suporte às personalizações de componentes, consulte a página [Personalizando componentes principais](developing/customizing.md) da versão relevante dos componentes principais.

## Suporte aos Componentes de base {#foundation-component-support}

A ênfase no desenvolvimento da Adobe foi transferida para os Componentes principais e os novos recursos continuarão a ser adicionados.

[Quase todos os Componentes de base foram descontinuados com o AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html?lang=pt-BR) e somente correções de bugs importantes serão consideradas para os componentes de base a partir de agora.
