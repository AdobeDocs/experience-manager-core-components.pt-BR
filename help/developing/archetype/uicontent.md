---
title: ui.content Module do AEM Project Archetype
description: ui.content Module do AEM Project Archetype
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Módulo ui.content do AEM Project Archetype {#uicontent-module}

O módulo ui.content maven (`<src-directory>/<project>/ui.content`) inclui conteúdo de linha de base e configurações abaixo de `/content` e `/conf`. ui.content é compilado em um pacote AEM, como ui.apps. A principal diferença é que os nós armazenados em ui.content podem ser modificados diretamente na instância AEM. Isso inclui páginas, ativos DAM e modelos editáveis. O módulo ui.content pode ser usado para armazenar conteúdo de amostra para uma instância limpa e/ou para criar algumas configurações de linha de base que devem ser gerenciadas no controle de origem.

## filter.xml {#filter}

O arquivo `filter.xml` do módulo ui.content é encontrado em `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml` e contém os caminhos que serão incluídos e instalados com o pacote ui.content. Observe que um atributo `mode="merge"` é adicionado ao caminho. Isso garante que as configurações implantadas com uma implantação de código não substituam automaticamente o conteúdo ou as configurações que foram criadas diretamente na instância AEM.

## ui.content/pom.xml

O módulo ui.content, como o módulo ui.apps, usa o plug-in FileVault Package. No entanto, o pom ui.content (`<src>/<project>/ui.content/pom.xml`) inclui uma propriedade de configuração extra chamada `acHandling`, definida como `merge_preserve`. Isso é incluído porque o módulo ui.content inclui Controles de acesso (ACLs) que são permissões, que determinam quem pode editar os modelos. Para que essas ACLs sejam importadas AEM a propriedade `acHandling` é necessária.
