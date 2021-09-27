---
title: Módulo principal do Arquétipo de projeto do AEM
description: Módulo principal do Arquétipo de projeto do AEM
feature: Componentes principais, Arquétipo de projeto do AEM
role: Architect, Developer, Admin
exl-id: 49e80d8c-2b41-4c42-b45e-c2e3b4b16a59
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '187'
ht-degree: 100%

---

# Módulo principal do Arquétipo de projeto do AEM {#core-module}

O módulo Maven principal (`<src-directory>/<project>/core`) inclui todo o código Java necessário para a implementação. O módulo compactará todo o código Java e implantará na instância do AEM como um pacote OSGi.

O Plug-in do pacote Maven definido no `<src-directory>/<project>/core/pom.xml` é responsável pela compilação do código Java em um pacote OSGi que pode ser reconhecido pelo contêiner OSGi do AEM. Observe que é aqui que a localização dos Modelos Sling é definida.

Embora seja raro o pacote principal precisar ser implantado independentemente do módulo ui.apps em ambientes de nível superior, a implantação direta do pacote principal é útil durante o desenvolvimento/teste local. O plug-in Maven Sling permite que o pacote principal seja implantado no AEM, aproveitando diretamente o perfil `autoInstallBundle`, conforme definido no [POM pal](/help/developing/archetype/using.md#parent-pom).

```shell
mvn -PautoInstallBundle clean install
```

Depois de executado com êxito, você deve conseguir ver o Console de pacotes em `http://<host>:<port>/system/console/bundles`.

## Testes de unidade {#unit-tests}

O teste de unidade no módulo principal mostra o teste de unidade clássica do código contido no pacote. Para testar, execute:

```shell
mvn clean test
```
