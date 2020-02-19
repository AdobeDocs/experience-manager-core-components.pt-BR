---
title: Módulo ui.tests do Arquivo de Projeto AEM
description: Como usar os testes JUnit do AEM Project Archetype
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Módulo ui.tests do Arquivo do Projeto AEM {#uitests-module}

Há três níveis de teste contidos no projeto:

## Testes de unidade {#unit-tests}

O teste de unidade no módulo [](core.md) principal mostra o teste de unidade clássica do código contido no pacote. Para testar, execute:

```
mvn clean test
```

## Testes de integração {#integration-tests}

Os testes de integração do servidor permitem que testes semelhantes a unidades sejam executados no ambiente AEM, ou seja, no servidor AEM. Para testar, execute:

```
mvn clean verify -PintegrationTests
```

## Testes no cliente {#client-side-tests}

Os `client-side Hobbes.js` testes são baseados em JavaScript para verificar o comportamento do navegador.

Para testar, ao exibir uma página do AEM que você deseja testar no navegador, abra a página no modo **** Desenvolvedor abrindo o painel esquerdo, alterne para a guia **Testes** e localize os Testes **do** MyName gerados e execute-os.
