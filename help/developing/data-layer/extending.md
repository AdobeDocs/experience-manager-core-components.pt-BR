---
title: Expansão da Camada de Dados de Clientes Adobe
description: A Camada de Dados de Clientes Adobe pode ser expandida seguindo alguns padrões básicos
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
TQID: 'https://experienceleague.adobe.com/67YSpRfwNRMDgcBARHKLz51-Er6xb4vp1rXX0r0sbfE'
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: d9d38edd-df1b-480c-8f5e-72b62576f390
    internal-label: Site and page features
  - id: d429a63e-ade4-4117-b04e-9b996d1c94ef
    internal-label: Integrations
subfeature_v2:
  - id: c43ff1f6-5a6d-4e8c-b3cc-6bdb3fa6e092
    internal-label: Core components
  - id: a94e5c13-4138-47ec-b9c8-e804e17aaca2
    internal-label: Adobe Client Data Layer
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 025b8134f7675b4515f4586910a94a2732bfa2ee
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 100%
---
# Expansão da Camada de Dados de Clientes Adobe {#extending-acdl}

É possível expandir os Componentes Principais com opções de caixas de diálogo personalizadas que permitem que autores de conteúdo insiram informações adicionais relacionadas à Camada de Dados.

Para incluir esses campos na Camada de Dados fornecida pelos Componentes Principais, é necessário estender o modelo do componente que implementa seus próprios métodos específicos de camada de dados.

## Exemplo: Componente de Título {#example}

Um Componente Principal como o [componente de Título](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) estende o [Componente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) que tenha um método `getData`, que por padrão retorna [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serializa campos predefinidos que seu componente pode implementar, como `getDataLayerLinkUrl` e `getDataLayerTitle` para o [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Portanto, seu modelo Sling personalizado pode ter um método `getData` que retorna um objeto que estende `ComponentData` para retornar mais campos.

Isso adicionará um atributo `data-cmp-data-layer` ao elemento HTML do seu componente com o JSON dos dados que serão preenchidos na camada de dados. Nesse ponto, é possível implementar scripts que ouçam esses dados ou eventos relacionados.

>[!TIP]
>
>Para explorar ainda mais a flexibilidade da Camada de Dados, analise as opções de integração, incluindo como habilitar a Camada de dados para seus componentes personalizados.
