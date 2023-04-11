---
title: 'Componente principal de Formulários adaptáveis: Cabeçalho'
description: Uso ou personalização do Componente principal de cabeçalho de Formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: aa18def9-0bec-4475-8dde-213860621ef5
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 92%

---

# Cabeçalho {#header-adaptive-forms-core-component}

Um componente de cabeçalho em um Formulário adaptável é uma seção localizada na parte superior do formulário que normalmente inclui o título, o logotipo ou o nome do formulário. O cabeçalho também pode incluir outras informações, como uma breve descrição da finalidade do formulário, o nome da organização que o criou ou informações de contato para obter ajuda com o formulário. O cabeçalho é usado para fornecer aos usuários uma visão geral do formulário e o contexto das informações que eles estão prestes a preencher. Ele é usado para ajudar os usuários a entender a finalidade do formulário e como preenchê-lo corretamente.

**Exemplo**

![](/help/adaptive-forms/assets/header.png)

## Uso {#reasons-to-use-header}

* **Marca**: um cabeçalho pode ser usado para exibir o logotipo ou o nome da organização que criou o formulário, ajudando a estabelecer o reconhecimento e a credibilidade da marca.

* **Contexto**: um cabeçalho pode fornecer uma breve descrição da finalidade do formulário, ajudando os usuários a entender o contexto no qual o formulário está sendo usado.

* **Navegação**: um cabeçalho pode incluir links ou botões que permitem aos usuários navegar para outras partes do site ou do aplicativo.

* **Informações**: um cabeçalho pode incluir informações de contato ou links para recursos de ajuda, tornando mais fácil para os usuários obter assistência se precisarem.

* **Experiência do usuário**: um cabeçalho pode ser usado para tornar o formulário mais simples, fornecendo uma maneira clara e intuitiva para os usuários acessarem e preencherem os campos de formulário.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal Adaptive Forms Accordion foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, AEM compatibilidade e links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com<br>[versão 1.1.12](/help/adaptive-forms/version.md) e posterior, mas inferior a 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de cabeçalho de Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de cabeçalho para visitantes com a caixa de diálogo Configurar. Também é possível definir as opções de cabeçalho com facilidade para uma experiência do usuário perfeita.

### Guia Imagem {#image-tab}

Essa parte do cabeçalho contém o título e a imagem do cabeçalho.

![Imagetab](/help/adaptive-forms/assets/header_image.png)

* **Ativo de imagem**: essa opção permite usar o arrastar e soltar do mouse em um ativo como uma imagem. Também é possível fazer upload de um arquivo do sistema de arquivos local usando o botão **Procurar**. Após adicionar uma imagem, três botões são exibidos em sua parte inferior. Após adicionar uma imagem, três botões são exibidos em sua parte inferior:
   * **Editar**: toque ou clique em **Editar** para gerenciar as representações do ativo no editor de ativos.
   * **Limpar**: toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * **Selecionar**: toque ou clique em **Selecionar** para selecionar outra imagem da pasta Ativos.

* **Título**: essa opção é usada para adicionar o título ao cabeçalho. O texto predefinido é incluído na caixa de diálogo e pode ser modificado pelo usuário.
* **Vincular a**: é possível vincular o cabeçalho à pasta usando o ícone de **Procurar**.
* **Descrição**: uma descrição é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de uma imagem específica.
* **Tamanho (px)**: ajuda a ajustar o comprimento e a largura da imagem, aumentando ou diminuindo os pixels.

![accessibilitytab](/help/adaptive-forms/assets/header_accessibility.png)

* **Texto alternativo**: essa opção é usada para inserir um texto curto e descritivo como uma alternativa para a imagem para usuários com deficiência visual.

* **A imagem é decorativa** - Verifique se a imagem deve ser ignorada pela tecnologia assistiva e, portanto, não requer um texto alternativo. Isso se aplica somente a imagens decorativas.

### Guia Texto {#text-tab}

Esta seção permite inserir o texto a ser incluído no cabeçalho.

