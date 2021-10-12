---
title: Módulo ui.content do Arquétipo de projeto do AEM
description: Módulo ui.content do Arquétipo de projeto do AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: af019cd8-c733-4b53-bb57-321dd9451178
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '218'
ht-degree: 100%

---

# Módulo ui.content do Arquétipo de projeto do AEM {#uicontent-module}

O módulo maven ui.content (`<src-directory>/<project>/ui.content`) inclui conteúdo de linha de base e configurações abaixo de `/content` e `/conf`. O ui.content é compilado em um pacote do AEM como ui.apps. A principal diferença é que os nós armazenados no ui.content podem ser modificados diretamente na instância do AEM. Isso inclui páginas, ativos DAM e modelos editáveis. O módulo ui.content pode ser usado para armazenar conteúdo de amostra para uma instância limpa e/ou para criar algumas configurações de linha de base que devem ser gerenciadas no controle do código-fonte.

## filter.xml {#filter}

O arquivo `filter.xml` para o módulo ui.content é encontrado em `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml` e contém os caminhos que serão incluídos e instalados com o pacote ui.content. Observe que um atributo `mode="merge"` é adicionado ao caminho. Isso garante que as configurações implantadas com uma implantação de código não substituam automaticamente o conteúdo ou as configurações que foram criadas diretamente na instância do AEM.

## ui.content/pom.xml

O módulo ui.content, como o módulo ui.apps, usa o plug-in FileVault Package. No entanto, o pom ui.content (`<src>/<project>/ui.content/pom.xml`) inclui uma propriedade de configuração extra chamada `acHandling`, definida como `merge_preserve`. Isso é incluído porque o módulo ui.content inclui Listas de Controle de Acesso (ACLs, na sigla em inglês), que são permissões que determinam quem pode editar os modelos. Para que essas ACLs sejam importadas para o AEM, a propriedade `acHandling` é necessária.
