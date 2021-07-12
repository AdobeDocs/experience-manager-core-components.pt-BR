---
title: Integrações e a camada de dados do cliente do Adobe
description: Saiba como a Camada de dados do cliente do Adobe pode se integrar aos seus componentes personalizados e como as integrações com o Adobe Analytics e o Adobe Target podem ajudar você a obter insights sobre seu site
feature: Componentes principais, Camada de dados do cliente Adobe
role: Architect, Developer, Admin
exl-id: 503dd3dc-fe95-4a17-83f5-1f0c1960993d
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Integrações com a camada de dados do cliente do Adobe {#integrations}

A Camada de dados do cliente do Adobe reduz o esforço de instrumentar sites, fornecendo um método padronizado para expor e acessar qualquer tipo de dados para qualquer script.

A Camada de dados do cliente do Adobe pode se integrar aos seus componentes personalizados e às integrações com o Adobe Analytics e o Adobe Target pode ajudar você a obter insights sobre seu site.

## Ativar a camada de dados para componentes personalizados {#enabling-custom-components}

Para adicionar automaticamente um componente personalizado à Camada de dados:

1. Defina as propriedades do modelo de componente personalizado que precisam ser rastreadas.
1. Adicione o atributo `data-cmp-data-layer` ao componente personalizado HTL. Por exemplo `data-cmp-data-layer="${mycomponent.data.json}"`.

Para fazer com que a Camada de dados acione automaticamente um evento `cmp:click` sempre que um elemento específico do componente personalizado for clicado, adicione o atributo `data-cmp-clickable` ao elemento a ser rastreado no componente personalizado HTL.

O atributo `data-cmp-data-layer-enabled` pode ser consultado no lado do cliente para verificar se a camada de dados está ativada.

>[!TIP]
>
>Para obter mais detalhes técnicos sobre a integração da Camada de dados do cliente do Adobe com os Componentes principais e como habilitar a Camada de dados em seus componentes personalizados, consulte o arquivo [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) no repositório dos Componentes principais.

## Integração com o Adobe Analytics e o Adobe Target {#analytics-target}

Em conjunto com a Adobe Analytics e a Adobe Target, a Camada de dados do cliente do Adobe se torna a base de um conjunto de ferramentas muito eficiente e flexível para obter insights sobre suas experiências digitais. Os seguintes tutoriais o orientam por meio de integrações de amostra.

### Coletar dados de página com o Adobe Analytics {#collect-page-data}

Saiba como usar os recursos integrados da Camada de dados do cliente do Adobe com AEM Componentes principais para coletar dados sobre uma página no Adobe Experience Manager Sites. O Experience Platform Launch e a extensão Adobe Analytics serão usados para criar regras para enviar dados de página para o Adobe Analytics.

[Visualize o tutorial aqui.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html)

### Rastrear componentes clicados com o Adobe Analytics {#track-clicked-components}

Use a Camada de dados do cliente do Adobe orientada por eventos com AEM Componentes principais para rastrear cliques de componentes específicos em um site do Adobe Experience Manager. Saiba como usar as regras no Experience Platform Launch para acompanhar eventos de clique, filtrar por componente e enviar os dados para uma Adobe Analytics com um beacon de rastreamento de link.

[Visualize o tutorial aqui.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html)
