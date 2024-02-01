---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
type: Documentation
description: Documentação dos Componentes principais do Adobe Experience Manager
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.pt-BR
index: y
recommendations: noDisplay
source-git-commit: 55e5ef9271b07d8fffc7b396c890af1637309ff3
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 100%

---


# Metadados para uso interno

Os metadados no sistema de autoria do GitHub são hierárquicos e definidos nos seguintes níveis crescentes de precedentes.

1. metadata.md
1. Índice
1. Artigo

Os metadados definidos no arquivo metadata.md se aplicam a todo o repositório, mas podem ser substituídos nos níveis de índice e artigo. Qualquer substituição dos metadados deve ser feita no nível mais baixo possível.

Os metadados no repositório experience-manager-core-components.en são o mínimo necessário.

metadata.md

* `product`
* `git-repo`
* `index: y`
* `solution-title`
* `solution-hub-url`
* `getting-started-title`
* `getting-started-url`
* `tutorials-title`
* `tutorials-url`

Índices

* `sub-product`
* `user-guide-title`

Artigo

* `title`
* `description`
* `index: n` (somente para versões anteriores de componentes)

Informações adicionais sobre os metadados podem ser encontradas no [guia de criação interno.](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/authoring/features/metadata.html?lang=pt-BR#solution)
