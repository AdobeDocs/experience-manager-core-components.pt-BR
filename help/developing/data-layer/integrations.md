---
title: Integrações e a Camada de dados de clientes Adobe
description: Saiba como a Camada de dados de clientes Adobe pode se integrar aos seus componentes personalizados e como as integrações com o Adobe Analytics e o Adobe Target podem ajudar você a obter insights sobre o seu site
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: 503dd3dc-fe95-4a17-83f5-1f0c1960993d
TQID: https://experienceleague.adobe.com/xncfOtz1FNyeH6CjQjg7cSeIonIg2mkBIPUgZvMI7Ww
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: ae478996-b206-4712-9b0c-dc78a2644453id: d429a63e-ade4-4117-b04e-9b996d1c94ef
subfeature_v2: id: a94e5c13-4138-47ec-b9c8-e804e17aaca2
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 424
ht-degree: 100%

---

# Integrações com a Camada de dados de clientes Adobe {#integrations}

A Camada de dados de clientes Adobe reduz o esforço de instrumentar sites, fornecendo um método padronizado para expor e acessar qualquer tipo de dados para qualquer script.

A Camada de dados de clientes Adobe pode se integrar aos seus componentes personalizados e às integrações com o Adobe Analytics e o Adobe Target pode ajudar você a obter insights sobre o seu site.

## Habilitar a Camada de dados para Componentes personalizados {#enabling-custom-components}

Para adicionar automaticamente um componente personalizado à Camada de dados:

1. Defina as propriedades do modelo de componente personalizado que precisam ser rastreadas.
1. Adicione o atributo `data-cmp-data-layer` ao componente personalizado HTL. Por exemplo: `data-cmp-data-layer="${mycomponent.data.json}"`.

Para fazer com que a Camada de dados acione automaticamente um evento `cmp:click` sempre que um elemento específico do componente personalizado for clicado, adicione o atributo `data-cmp-clickable` ao elemento a ser rastreado no componente personalizado HTL.

O atributo `data-cmp-data-layer-enabled` pode ser consultado no lado do cliente para verificar se a camada de dados está habilitada.

>[!TIP]
>
>Para mais detalhes técnicos sobre a integração da Camada de dados de dados de clientes Adobe com os Componentes principais e como habilitar a Camada de dados em seus componentes personalizados, consulte o arquivo [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) no repositório dos Componentes principais.

## Integração com o Adobe Analytics e o Adobe Target {#analytics-target}

Em conjunto com a Adobe Analytics e a Adobe Target, a Camada de dados de clientes Adobe se torna a base de um conjunto de ferramentas muito eficiente e flexível para obter insights sobre suas experiências digitais. Os seguintes tutoriais o orientam por meio de integrações de amostra.

### Coletar dados de página com o Adobe Analytics {#collect-page-data}

Saiba como usar os recursos integrados da Camada de dados de clientes Adobe com os Componentes principais do AEM para coletar dados sobre uma página no Adobe Experience Manager Sites. O Experience Platform Launch e a extensão do Adobe Analytics serão usados para criar regras para enviar dados de página para o Adobe Analytics.

[Visualize o tutorial aqui.](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/sites/integrations/analytics/collect-data-analytics)

### Rastrear componentes clicados com o Adobe Analytics {#track-clicked-components}

Use a Camada de dados de clientes Adobe orientada por eventos com os Componentes principais do AEM para rastrear cliques de componentes específicos em um site do Adobe Experience Manager. Saiba como usar as regras no Experience Platform Launch para acompanhar eventos de clique, filtrar por componente e enviar os dados ao Adobe Analytics com um aviso de rastreamento de link.

[Visualize o tutorial aqui.](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/sites/integrations/analytics/track-clicked-component)
