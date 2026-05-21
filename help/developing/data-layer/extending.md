---
title: Expansão da Camada de Dados de Clientes Adobe
description: A Camada de Dados de Clientes Adobe pode ser expandida seguindo alguns padrões básicos
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
TQID: https://experienceleague.adobe.com/67YSpRfwNRMDgcBARHKLz51-Er6xb4vp1rXX0r0sbfE
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 289
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
