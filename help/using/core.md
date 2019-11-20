---
title: Módulo principal do arquivo do projeto AEM
seo-title: Módulo principal do arquivo do projeto AEM
description: Módulo principal do arquivo do projeto AEM
seo-description: Módulo principal do arquivo do projeto AEM
contentOwner: bohnert
content-type: reference
topic-tags: core-components
translation-type: tm+mt
source-git-commit: ca7a47d8ac91516659c115a3f27c09f0ee4b8b33

---


# Módulo principal do arquivo do projeto AEM {#core-module}

O módulo principal de maven (`<src-directory>/<project>/core`) inclui todo o código Java necessário para a implementação. O módulo compactará todo o código Java e implantará na instância do AEM como um pacote OSGi.

O Plug-in Maven Bundle definido no `<src-directory>/<project>/core/pom.xml` é responsável pela compilação do código Java em um pacote OSGi que pode ser reconhecido pelo contêiner OSGi do AEM. Observe que este é o local em que os Modelos Sling são definidos.

Embora seja raro que o pacote principal precise ser implantado independentemente do módulo ui.apps em ambientes de nível superior, a implantação direta do pacote principal é útil durante o desenvolvimento/teste local. O plug-in Maven Sling permite que o pacote principal seja implantado no AEM aproveitando diretamente o `autoInstallBundle` perfil, conforme definido no POM [](overview.md#parent-pom)pai.

```
mvn -PautoInstallBundle clean install
```

Depois de executado com êxito, você deve ser capaz de visualizar o Console de pacotes em `http://<host>:<port>/system/console/bundles`.
