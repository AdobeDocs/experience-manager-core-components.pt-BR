---
title: Módulo ui.tests do Arquétipo de projeto do AEM
description: Como usar os Testes da IU do Arquétipo de projeto do AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: eb3c9b34-f10e-410f-bcf3-34f94f124c7c
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '112'
ht-degree: 100%

---

# Módulo ui.tests do Arquétipo de projeto do AEM {#uitests-module}

Existem três níveis de testes contidos no projeto:

* [Testes de unidade](core.md#unit-tests)
* [Testes de integração](ittests.md)
* Testes de interface do usuário

Este artigo descreve os testes de IU disponíveis como parte do módulo ui.tests.

## Execução de testes de IU {#running-tests}

Para testar, execute:

```shell
mvn verify -Pui-tests-local-execution
```

Após a execução, os relatórios e logs ficam disponíveis na pasta `target/reports`.

## Opções adicionais {#additional-options}

Os testes de IU podem ser executados com várias opções diferentes, incluindo testes sem periféricos em um navegador local e como uma imagem de Docker. Consulte o arquivo [README.md do módulo ui.tests](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests) para mais informações.
