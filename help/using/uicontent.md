---
title: ui.content Module do AEM Project Archetype
description: ui.content Module do AEM Project Archetype
translation-type: tm+mt
source-git-commit: 945381996db443c227aa31f0aacb963071165681

---


# ui.content Module do AEM Project Archetype {#uicontent-module}

O módulo ui.content maven (`<src-directory>/<project>/ui.content`) inclui conteúdo básico e configurações abaixo `/content` e `/conf`. ui.content é compilado em um pacote AEM como ui.apps. A principal diferença é que os nós armazenados em ui.content podem ser modificados diretamente na instância do AEM. Isso inclui páginas, ativos DAM e modelos editáveis. O módulo ui.content pode ser usado para armazenar conteúdo de amostra para uma instância limpa e/ou para criar algumas configurações de linha de base que devem ser gerenciadas no controle de origem.

## filter.xml {#filter}

O `filter.xml` arquivo do módulo ui.content é encontrado em `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml` e contém os caminhos que serão incluídos e instalados com o pacote ui.content. Observe que um `mode="merge"` atributo é adicionado ao caminho. Isso garante que as configurações implantadas com uma implantação de código não substituam automaticamente o conteúdo ou as configurações que foram criadas diretamente na instância do AEM.

## ui.content/pom.xml

O módulo ui.content, como o módulo ui.apps, usa o plug-in FileVault Package. Entretanto, o pom ui.content (`<src>/<project>/ui.content/pom.xml`) inclui uma propriedade de configuração extra chamada `acHandling`, definida como `merge_preserve`. Isso é incluído porque o módulo ui.content inclui ACLs (Access Control Lists, listas de controle de acesso) que são permissões, que determinam quem pode editar os modelos. Para que essas ACLs sejam importadas para o AEM, a `acHandling` propriedade é necessária.
