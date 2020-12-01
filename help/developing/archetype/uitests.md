---
title: Módulo ui.tests do AEM Project Archetype
description: Como usar os testes JUnit do AEM Project Archetype
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# Módulo ui.testing do AEM Project Archetype {#uitests-module}

Há três níveis de teste contidos no projeto:

## Testes de Unidade {#unit-tests}

O teste de unidade no módulo [núcleo](core.md) mostra o teste de unidade clássica do código contido no conjunto. Para testar, execute:

```
mvn clean test
```

## Testes de integração {#integration-tests}

Os testes de integração do lado do servidor permitem que testes semelhantes a unidades sejam executados no ambiente AEM, ou seja, no servidor AEM. Para testar, execute:

```
mvn clean verify -PintegrationTests
```

## Testes do lado do cliente {#client-side-tests}

Os testes `client-side Hobbes.js` são testes do lado do navegador baseados em JavaScript que verificam o comportamento do lado do navegador.

Para testar, ao visualizar uma página AEM que você deseja testar no navegador, abra a página no **modo Desenvolvedor** abrindo o painel esquerdo e alterne para a guia **Testes** e localize os **Testes do MeuNome** gerados e execute-os.
