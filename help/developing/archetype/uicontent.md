---
title: ui.content Module do AEM Project Archetype
description: ui.content Module do AEM Project Archetype
feature: Componentes principais, Arquétipo de projeto AEM
role: Arquiteto, desenvolvedor, administrador
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Módulo ui.content do Arquétipo de projeto AEM {#uicontent-module}

O módulo ui.content maven (`<src-directory>/<project>/ui.content`) inclui o conteúdo da linha de base e as configurações abaixo de `/content` e `/conf`. ui.content é compilado em um pacote de AEM como ui.apps. A principal diferença é que os nós armazenados em ui.content podem ser modificados diretamente na instância de AEM. Isso inclui páginas, ativos DAM e modelos editáveis. O módulo ui.content pode ser usado para armazenar conteúdo de amostra para uma instância limpa e/ou para criar algumas configurações de linha de base que devem ser gerenciadas no controle do código-fonte.

## filter.xml {#filter}

O arquivo `filter.xml` para o módulo ui.content é encontrado em `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml` e contém os caminhos que serão incluídos e instalados com o pacote ui.content. Observe que um atributo `mode="merge"` é adicionado ao caminho. Isso garante que as configurações implantadas com uma implantação de código não substituam automaticamente o conteúdo ou as configurações que foram criadas diretamente na instância de AEM.

## ui.content/pom.xml

O módulo ui.content, como o módulo ui.apps , usa o plug-in FileVault Package. No entanto, o pom ui.content (`<src>/<project>/ui.content/pom.xml`) inclui uma propriedade de configuração extra chamada `acHandling`, definida como `merge_preserve`. Isso é incluído porque o módulo ui.content inclui Listas de Controle de Acesso (ACLs) que são permissões, que determinam quem pode editar os modelos. Para que essas ACLs sejam importadas para AEM a propriedade `acHandling` é necessária.
