---
title: it.testing Module of AEM Project Archetype
description: Como usar os testes de integração do AEM Project Archetype
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---


# it.testing Módulo do AEM Project Archetype {#ittests-module}

Há três níveis de teste contidos no projeto:

* [Testes de unidade](core.md#unit-tests)
* Testes de integração
* [Testes da interface do usuário](uitests.md)

Este artigo descreve os testes de integração disponíveis como parte do módulo it.testing.

## Execução de testes de integração {#running-tests}

Os testes de integração do lado do servidor permitem que testes semelhantes a unidades sejam executados no ambiente AEM, ou seja, no servidor AEM. Para testar, execute:

```
mvn clean verify -PintegrationTests
```
