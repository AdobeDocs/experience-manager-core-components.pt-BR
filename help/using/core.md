---
title: Módulo principal do arquivo do projeto AEM
seo-title: Módulo principal do arquivo do projeto AEM
description: Módulo principal do arquivo do projeto AEM
seo-description: Módulo principal do arquivo do projeto AEM
contentOwner: bohnerd
content-type: referência
topic-tags: componentes principais
translation-type: tm+mt
source-git-commit: 683b4f4705c226275439a408423cbf1b23bea66f

---


# Módulo principal do arquivo do projeto AEM {#core-module}

O módulo principal de maven (`<src-directory>/<project>/core`) inclui todo o código Java necessário para a implementação. O módulo compactará todo o código Java e implantará na instância do AEM como um pacote OSGi.

O Plug-in Maven Bundle definido no `<src-directory>/<project>/core/pom.xml` é responsável pela compilação do código Java em um pacote OSGi que pode ser reconhecido pelo contêiner OSGi do AEM. Observe que este é o local em que os Modelos Sling são definidos.

Embora seja raro que o pacote principal precise ser implantado independentemente do módulo ui.apps em ambientes de nível superior, a implantação direta do pacote principal é útil durante o desenvolvimento/teste local. O plug-in Maven Sling permite que o pacote principal seja implantado no AEM aproveitando diretamente o `autoInstallBundle` perfil, conforme definido no POM [](overview.md#parent-pom)pai.

```
mvn -PautoInstallBundle clean install
```

Depois de executado com êxito, você deve ser capaz de ver o console Bundels em `http://<host>:<port>/system/console/bundles`.
