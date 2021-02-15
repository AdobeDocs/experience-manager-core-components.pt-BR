---
title: Módulo ui.tests do AEM Project Archetype
description: Como usar os Testes da interface do AEM Project Archetype
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Módulo ui.testing do AEM Project Archetype {#uitests-module}

Há três níveis de teste contidos no projeto:

* [Testes de unidade](core.md#unit-tests)
* [Testes de integração](ittests.md)
* Testes da interface do usuário

Este artigo descreve os testes de interface disponíveis como parte do módulo ui.testing.

## Execução de testes de interface de usuário {#running-tests}

Para testar, execute:

```shell
mvn verify -Pui-tests-local-execution
```

Após a execução, os relatórios e registros ficam disponíveis na pasta `target/reports`.

## Opções adicionais {#additional-options}

Os testes da interface do usuário podem ser executados com muitas opções diferentes, incluindo testes sem cabeça em um navegador local e como uma imagem Docker. Consulte o arquivo [README.md do módulo ui.testing](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests) para obter mais informações.
