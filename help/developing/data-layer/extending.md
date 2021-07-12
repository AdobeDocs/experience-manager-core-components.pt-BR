---
title: Extensão da camada de dados do cliente do Adobe
description: A Camada de dados do cliente do Adobe pode ser estendida seguindo alguns padrões básicos
feature: Componentes principais, Camada de dados do cliente Adobe
role: Architect, Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Extensão da camada de dados do cliente do Adobe {#extending-acdl}

É possível estender os Componentes principais com opções de caixa de diálogo personalizadas que permitem que autores de conteúdo insiram informações adicionais relacionadas à Camada de dados.

Para incluir esses campos na Camada de dados fornecida pelos Componentes principais, é necessário estender o modelo do componente que implementa seus próprios métodos específicos de camada de dados.

## Exemplo: Componente de título {#example}

Um Componente principal como [Componente de título](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) estende [Componente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) que tem um método `getData` que por padrão retorna [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serializa campos predefinidos que seu componente pode implementar, como  `getDataLayerLinkUrl` e  `getDataLayerTitle` para o  [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Portanto, seu modelo Sling personalizado pode ter um método `getData` que retorna um objeto que estende `ComponentData` para retornar mais campos.

Ao fazer isso, o adicionará um atributo `data-cmp-data-layer` ao elemento HTML do seu componente com o JSON dos dados que serão preenchidos na camada de dados. Nesse ponto, é possível implementar scripts que ouçam esses dados ou eventos relacionados.

>[!TIP]
>
>Para explorar a flexibilidade da camada de dados, analise as opções de integração, incluindo como ativar a camada de dados para seus componentes personalizados.
