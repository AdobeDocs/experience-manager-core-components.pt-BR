---
title: Módulo ui.apps do AEM Project Archetype
description: Módulo ui.apps do AEM Project Archetype
translation-type: tm+mt
source-git-commit: a427c2ade8cca69de8e2b59fc3afb4405342909c
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---


# Módulo ui.apps do AEM Project Archetype {#uiapps-module}

O módulo ui.apps maven (`<src-directory>/<project>/ui.apps`) inclui todo o código de renderização necessário para o site abaixo de `/apps`. Isso inclui CSS/JS que serão armazenados em um formato AEM chamado [clientlibs.](uifrontend.md#clientlibs) Isso também inclui scripts HTL para renderização de HTML dinâmico. Você pode considerar o módulo ui.apps como um mapa para a estrutura no JCR, mas em um formato que pode ser armazenado em um sistema de arquivos e confirmado para o controle de origem.

O plug-in Apache Jackrabbit FileVault Package é usado para compilar o conteúdo do módulo ui.apps em um pacote AEM que pode ser implantado no AEM. As configurações globais para o plug-in são definidas no pom.xml pai.

## POM pai {#parent-pom}

[O POM](/help/developing/archetype/using.md#parent-pom) (`<src>/<project>/pom.xml`) pai inclui  `<plugin>` seções que definem várias configurações para os plug-ins usados no projeto. Isso inclui uma configuração para o `filterSource` para o plug-in do pacote Jackrabbit FileVault. O `filterSource` aponta para o local do arquivo `filter.xml` usado para definir os caminhos jcr incluídos no pacote.

Além do Plug-in do pacote Jackrabbit FileVault é uma definição do Plug-in do pacote de conteúdo que é usado para empurrar o pacote para AEM. Observe que as variáveis para `aem.host`, `aem.port`, `vault.user` e `vault.password` são usadas que correspondem às propriedades globais definidas no mesmo POM pai.

## ui.apps/pom.xml {#uiapps-pom}

O pom ui.apps (`<src>/<project>/ui.apps/pom.xml`) fornece as tags `embedded` para `filevault-package-maven-plugin`. As tags `embedded` incluem o pacote principal compilado como parte do pacote ui.apps e onde ele será instalado.

Observe que os pacotes core.wcm.components.all e core.wcm.components.example são incluídos como um subpacote. Isso implantará o pacote Componentes principais junto com o código WKND sempre.

Os principais.wcm.components.all e core.wcm.components.examples são incluídos como dependências na lista de dependência. No entanto, como prática recomendada, as versões para dependências são omitidas aqui e gerenciadas no [arquivo pom pai](/help/developing/archetype/using.md#core-components).

## filter.xml {#filter}

O arquivo `filter.xml` do módulo ui.apps é encontrado em `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` e contém os caminhos que serão incluídos e instalados com o pacote ui.apps.
