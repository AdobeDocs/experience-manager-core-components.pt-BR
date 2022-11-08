---
title: Módulo ui.apps do Arquétipo de projeto do AEM
description: Módulo ui.apps do Arquétipo de projeto do AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: fc63a19a-3253-44ee-96e2-bb5544c2235b
source-git-commit: 19bceb1d8ba07c70798f2e7203db957d3e8b3d03
workflow-type: ht
source-wordcount: '308'
ht-degree: 100%

---

# Módulo ui.apps do Arquétipo de projeto do AEM {#uiapps-module}

O módulo ui.apps maven (`<src-directory>/<project>/ui.apps`) inclui todo o código de renderização necessário para o site sob `/apps`. Isso inclui CSS/JS que será armazenado em um formato do AEM chamado [clientlibs.](uifrontend.md#clientlibs) Também inclui scripts HTL para renderização de HTML dinâmico. Pense no módulo ui.apps como um mapa para a estrutura no JCR, mas em um formato que pode ser armazenado em um sistema de arquivos e comprometido com o controle de origem.

O plug-in Apache Jackrabbit FileVault Package é usado para compilar os conteúdos do módulo ui.apps em um pacote de AEM que pode ser implantado no AEM. As configurações globais para o plug-in são definidas no pom.xml principal.

## POM principal {#parent-pom}

[O POM principal](/help/developing/archetype/using.md#parent-pom) (`<src>/<project>/pom.xml`) inclui seções `<plugin>` que definem várias configurações para os plug-ins usados no projeto. Isso inclui uma configuração para o `filterSource` para o plug-in Jackrabbit FileVault Package. O `filterSource` aponta para o local do arquivo `filter.xml` usado para definir os caminhos jcr incluídos no pacote.

Além do plug-in Jackrabbit FileVault Package, há uma definição do plug-in Pacote de conteúdo, usado para enviar o pacote para o AEM. Observe que são usadas variáveis para `aem.host`, `aem.port`, `vault.user` e `vault.password` que correspondem às propriedades globais definidas no mesmo POM principal.

## ui.apps/pom.xml {#uiapps-pom}

Observe que os pacotes core.wcm.components.all e core.wcm.components.examples são incluídos como um subpacote. Isso implantará o pacote dos Componentes principais junto com o código WKND toda vez.

Os pacotes core.wcm.components.all e core.wcm.components.examples são incluídos como dependências na lista de dependências. No entanto, como prática recomendada, as versões das dependências são omitidas aqui e gerenciadas no [arquivo pom principal](/help/developing/archetype/using.md#core-components).

## filter.xml {#filter}

O arquivo `filter.xml` para o módulo ui.apps é encontrado em `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` e contém os caminhos que serão incluídos e instalados com o pacote ui.apps.
