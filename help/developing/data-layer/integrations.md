---
title: Integrações e a camada de dados do cliente Adobe
description: Saiba como a Camada de dados do cliente Adobe pode se integrar aos seus componentes personalizados e como as integrações com a Adobe Analytics e a Adobe Target podem ajudá-lo a obter insights sobre seu site
translation-type: tm+mt
source-git-commit: ea7a0e08ea1b769b400fce275c8ce7e0db6f9407
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Integrações com a camada de dados do cliente Adobe {#integrations}

A Camada de dados do cliente Adobe reduz o esforço de instrumentar sites, fornecendo um método padronizado para expor e acessar qualquer tipo de dados para qualquer script.

A Camada de dados do cliente Adobe pode se integrar aos seus componentes personalizados e às integrações com a Adobe Analytics e a Adobe Target para ajudá-lo a obter insights em seu site.

## Ativação da camada de dados para componentes personalizados {#enabling-custom-components}

Para adicionar automaticamente um componente personalizado à Camada de dados:

1. Defina as propriedades do modelo de componente personalizado que precisam ser rastreadas.
1. Adicione o `data-cmp-data-layer` atributo ao componente personalizado HTL. Por exemplo: `data-cmp-data-layer="${mycomponent.data.json}"`.

Para fazer com que a Camada de dados dispare um `cmp:click` evento automaticamente sempre que um elemento específico do componente personalizado for clicado, adicione o `data-cmp-clickable` atributo ao elemento a ser rastreado no componente personalizado HTL.

O `data-cmp-data-layer-enabled` atributo pode ser consultado no cliente para verificar se a camada de dados está ativada.

>[!TIP]
>
>Para obter mais detalhes técnicos sobre a integração da Camada de dados do cliente Adobe com os componentes principais e como habilitar a Camada de dados em seus componentes personalizados, consulte o [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) arquivo no repositório dos componentes principais.

## Integração com Adobe Analytics e Adobe Target {#analytics-target}

Em conjunto com a Adobe Analytics e a Adobe Target, a Adobe Client Data Layer torna-se a base de um conjunto de ferramentas muito poderoso e flexível para obter insights sobre suas experiências digitais. Os seguintes tutoriais o orientam por meio de integrações de amostra.

### Coletar dados da página com o Adobe Analytics {#collect-page-data}

Saiba como usar os recursos integrados da Camada de dados do cliente Adobe com AEM componentes principais para coletar dados sobre uma página no Adobe Experience Manager Sites. O Experience Platform Launch e a extensão do Adobe Analytics serão usados para criar regras para enviar dados de página para a Adobe Analytics.

[Visualização o tutorial aqui.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html)

### Acompanhar componentes clicados com o Adobe Analytics {#track-clicked-components}

Use a Camada de dados do cliente Adobe orientada pelo evento com AEM componentes principais para rastrear cliques de componentes específicos em um site da Adobe Experience Manager. Saiba como usar regras no Experience Platform Launch para ouvir eventos de clique, filtrar por componente e enviar os dados para um Adobe Analytics com um beacon de rastreamento de link.

[Visualização o tutorial aqui.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html)
