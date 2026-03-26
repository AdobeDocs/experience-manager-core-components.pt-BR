---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
landing-page-name: experience-manager
landing-page-breadcrumb-title: AEM
type: Documentation
description: Documentação dos Componentes principais do Adobe Experience Manager
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.en
index: true
recommendations: noDisplay
source-git-commit: 1975e060e8db5526518dcf6fc722e3623c47dda6
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---


# Metadados para uso interno

Os metadados no sistema de criação do GitHub são hierárquicos e definidos nos seguintes níveis crescentes de precedentes.

1. metadata.md
1. ToC
1. Artigo

Os metadados definidos no arquivo metadata.md se aplicam a todo o repositório, mas podem ser substituídos nos níveis de índice e artigo. Qualquer substituição dos metadados deve ser feita no nível mais baixo possível.

Os metadados no repositório experience-manager-core-components.en são o mínimo necessário.

metadata.md

* `product`
* `git-repo`
* `index: true`
* `solution-title`
* `solution-hub-url`
* `getting-started-title`
* `getting-started-url`
* `tutorials-title`
* `tutorials-url`

ToCs

* `sub-product`
* `user-guide-title`

Artigo

* `title`
* `description`
* `index: false` (somente para versões anteriores de componentes)

Informações adicionais sobre os metadados podem ser encontradas no [guia de criação interno.](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/authoring/features/metadata.html#solution)
