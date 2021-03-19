---
title: Módulo it.tests do Arquétipo de Projeto AEM
description: Como usar os Testes de integração do Arquétipo de projeto do AEM
feature: Componentes principais, Arquétipo de projeto AEM
role: Arquiteto, desenvolvedor, administrador
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Módulo it.tests do Arquétipo de Projeto AEM {#ittests-module}

Existem três níveis de testes contidos no projeto:

* [Testes de unidade](core.md#unit-tests)
* Testes de integração
* [Testes da interface do usuário](uitests.md)

Este artigo descreve os testes de integração disponíveis como parte do módulo it.tests .

## Executando testes de integração {#running-tests}

Os testes de integração do lado do servidor permitem que testes semelhantes a unidades sejam executados no ambiente AEM, ou seja, no servidor AEM. Para testar, execute:

```
mvn clean verify -PintegrationTests
```
