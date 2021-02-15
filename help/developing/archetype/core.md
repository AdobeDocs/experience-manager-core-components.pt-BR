---
title: Módulo principal do AEM Project Archetype
description: Módulo principal do AEM Project Archetype
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---


# Módulo principal do AEM Project Archetype {#core-module}

O módulo principal de maven (`<src-directory>/<project>/core`) inclui todo o código Java necessário para a implementação. O módulo compactará todo o código Java e implantará na instância AEM como um pacote OSGi.

O Plug-in Maven Bundle definido em `<src-directory>/<project>/core/pom.xml` é responsável por compilar o código Java em um pacote OSGi que pode ser reconhecido por AEM container OSGi. Observe que este é o local em que os Modelos Sling são definidos.

Embora seja raro que o pacote principal precise ser implantado independentemente do módulo ui.apps em ambientes de nível superior, a implantação direta do pacote principal é útil durante o desenvolvimento/teste local. O Plug-in Maven Sling permite que o pacote principal seja implantado para AEM aproveitando diretamente o perfil `autoInstallBundle` conforme definido no [POM pai](/help/developing/archetype/using.md#parent-pom).

```shell
mvn -PautoInstallBundle clean install
```

Depois de executado com êxito, você deve ser capaz de visualizar o Console de Pacotes em `http://<host>:<port>/system/console/bundles`.

##  Testes de Unidade {#unit-tests}

O teste de unidade no módulo principal mostra o teste de unidade clássica do código contido no conjunto. Para testar, execute:

```shell
mvn clean test
```
