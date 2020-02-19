---
title: Módulo ui.apps do Arquivo de Projeto AEM
description: Módulo ui.apps do Arquivo de Projeto AEM
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Módulo ui.apps do Arquivo de Projeto AEM {#uiapps-module}

O módulo ui.apps maven (`<src-directory>/<project>/ui.apps`) inclui todo o código de renderização necessário para o site abaixo `/apps`. Isso inclui CSS/JS que serão armazenados em um formato AEM chamado clientlibs. Isso também inclui scripts HTL para renderização de HTML dinâmico. Você pode considerar o módulo ui.apps como um mapa para a estrutura no JCR, mas em um formato que pode ser armazenado em um sistema de arquivos e confirmado para o controle de origem.

O plug-in Apache Jackrabbit FileVault Package é usado para compilar o conteúdo do módulo ui.apps em um pacote AEM que pode ser implantado no AEM. As configurações globais para o plug-in são definidas no pom.xml pai.

## POM pai {#parent-pom}

[O POM](overview.md#parent-pom) pai (`<src>/<project>/pom.xml`) inclui `<plugin>` seções que definem várias configurações para os plug-ins usados no projeto. Isso inclui uma configuração para o plug-in do pacote Jackrabbit FileVault. `filterSource` O `filterSource` aponta para o local do `filter.xml` arquivo usado para definir os caminhos jcr incluídos no pacote.

Além do Plug-in do pacote Jackrabbit FileVault é uma definição do Plug-in do pacote de conteúdo que é usado para empurrar o pacote para o AEM. Observe que variáveis para `aem.host`, `aem.port`, `vault.user`e `vault.password` são usadas que correspondem às propriedades globais definidas no mesmo POM pai.

## ui.apps/pom.xml {#uiapps-pom}

O pom ui.apps (`<src>/<project>/ui.apps/pom.xml`) fornece as `embedded` tags para o `filevault-package-maven-plugin`. As `embedded` tags incluem o pacote principal compilado como parte do pacote ui.apps e onde ele será instalado.

Observe que os pacotes core.wcm.components.all e core.wcm.components.example são incluídos como um subpacote. Isso implantará o pacote Componentes principais junto com o código WKND sempre.

Os principais.wcm.components.all e core.wcm.components.examples são incluídos como dependências na lista de dependências. No entanto, como prática recomendada, as versões para dependências são omitidas aqui e gerenciadas no arquivo [pom](overview.md#core-components)pai.

## filter.xml {#filter}

O `filter.xml` arquivo do módulo ui.apps é encontrado em `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` e contém os caminhos que serão incluídos e instalados com o pacote ui.apps.
