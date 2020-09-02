---
title: Extensão da camada de dados do cliente Adobe
description: A Camada de Dados do Cliente Adobe pode ser estendida seguindo alguns padrões básicos
translation-type: tm+mt
source-git-commit: 896ed679ed3351cb309a34b38bf97fe81adc2cfe
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# Extensão da camada de dados do cliente Adobe {#extending-acdl}

Você pode estender os Componentes principais com opções de diálogo personalizadas que permitem que os autores de conteúdo insiram informações adicionais relacionadas à Camada de dados.

Para incluir esses campos na Camada de dados fornecida pelos Componentes principais, é necessário estender o modelo do componente que implementa seus próprios métodos específicos de camada de dados.

## Exemplo: Componente Título {#example}

Um Componente principal como o componente [](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) Título estende [Componente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) que tem um `getData` método que por padrão retorna [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serializa campos predefinidos que seu componente pode implementar, como `getDataLayerLinkUrl` e `getDataLayerTitle` para o [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Portanto, seu modelo Sling personalizado pode ter um `getData` método que retorna um objeto que se estende `ComponentData` para retornar mais campos.

Ao fazer isso, adicionará um `data-cmp-data-layer` atributo ao elemento HTML do seu componente com o JSON dos dados que serão preenchidos na camada de dados. Nesse ponto, é possível implementar scripts que ouvem esses dados ou eventos relacionados.
