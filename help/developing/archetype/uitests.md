---
title: Módulo ui.tests do Arquétipo de Projeto AEM
description: Como usar os Testes da interface do usuário do Arquétipo de projeto do AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# Módulo ui.tests do Arquétipo de Projeto AEM {#uitests-module}

Existem três níveis de testes contidos no projeto:

* [Testes de unidade](core.md#unit-tests)
* [Testes de integração](ittests.md)
* Testes da interface do usuário

Este artigo descreve os testes de interface disponíveis como parte do módulo ui.tests .

## Executando testes de interface do usuário {#running-tests}

Para testar, execute:

```shell
mvn verify -Pui-tests-local-execution
```

Após a execução, os relatórios e logs ficam disponíveis na pasta `target/reports`.

## Opções adicionais {#additional-options}

Os testes da interface do usuário podem ser executados com várias opções diferentes, incluindo testes sem periféricos em um navegador local e como uma imagem Docker. Consulte o arquivo [README.md do módulo ui.tests](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests) para obter mais informações.
