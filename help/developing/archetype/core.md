---
title: Módulo principal do arquétipo de projeto AEM
description: Módulo principal do arquétipo de projeto AEM
feature: Componentes principais, Arquétipo de projeto AEM
role: Arquiteto, desenvolvedor, administrador
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# Módulo principal do Arquétipo de projeto AEM {#core-module}

O módulo principal de maven (`<src-directory>/<project>/core`) inclui todo o código Java necessário para a implementação. O módulo compactará todo o código Java e implantará na instância AEM como um pacote OSGi.

O Plug-in do pacote Maven definido no `<src-directory>/<project>/core/pom.xml` é responsável pela compilação do código Java em um pacote OSGi que pode ser reconhecido AEM contêiner OSGi. Observe que é aqui que a localização dos Modelos do Sling é definida.

Embora seja raro o pacote principal precisar ser implantado independentemente do módulo ui.apps em ambientes de nível superior, a implantação direta do pacote principal é útil durante o desenvolvimento/teste local. O Maven Sling Plugin permite que o pacote principal seja implantado AEM aproveitar diretamente o perfil `autoInstallBundle`, conforme definido no [POM pai](/help/developing/archetype/using.md#parent-pom).

```shell
mvn -PautoInstallBundle clean install
```

Depois de executado com êxito, você deve conseguir ver o Console de pacotes em `http://<host>:<port>/system/console/bundles`.

##  Testes de Unidade {#unit-tests}

O teste de unidade no módulo principal mostra o teste de unidade clássica do código contido no pacote. Para testar, execute:

```shell
mvn clean test
```
