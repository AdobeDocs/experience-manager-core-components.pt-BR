---
title: Módulo it.tests do Arquétipo de projeto do AEM
description: Como usar os Testes de integração do Arquétipo de projeto do AEM
feature: Componentes principais, Arquétipo de projeto do AEM
role: Architect, Developer, Admin
exl-id: 0abc0265-3a3f-4323-97e6-3af0c62299ef
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '80'
ht-degree: 100%

---

# Módulo it.tests do Arquétipo de projeto do AEM {#ittests-module}

Existem três níveis de testes contidos no projeto:

* [Testes de unidade](core.md#unit-tests)
* Testes de integração
* [Testes de IU](uitests.md)

Este artigo descreve os testes de integração disponíveis como parte do módulo it.tests.

## Execução de testes de integração {#running-tests}

Os testes de integração do lado do servidor permitem que testes semelhantes a unidades sejam executados no ambiente AEM, ou seja, no servidor AEM. Para testar, execute:

```
mvn clean verify -PintegrationTests
```
