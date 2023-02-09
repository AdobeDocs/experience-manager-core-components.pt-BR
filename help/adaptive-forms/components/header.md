---
title: Componente principal adaptável do Forms - Cabeçalho
description: Uso ou personalização do Componente principal do cabeçalho adaptável do Forms.
role: Architect, Developer, Admin, User
source-git-commit: 7f680eac1da61b55f9d90db6c0842421d03ac1dc
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 7%

---


# Cabeçalho {#header-adaptive-forms-core-component}

Um componente Cabeçalho em um Formulário adaptável é uma seção localizada na parte superior do formulário, que normalmente inclui o título, o logotipo ou o nome do formulário. O cabeçalho também pode incluir outras informações, como uma breve descrição da finalidade do formulário, o nome da organização que criou o formulário ou informações de contato para obter ajuda com o formulário. O cabeçalho é usado para fornecer aos usuários uma visão geral do formulário e fornecer contexto para as informações que eles estão prestes a preencher. Ele é usado para ajudar os usuários a entender a finalidade do formulário e como preenchê-lo corretamente.

**Exemplo**

![](/help/adaptive-forms/assets/header.png)

## Uso {#reasons-to-use-header}

* **Marca**: Um cabeçalho pode ser usado para exibir o logotipo ou o nome da organização que criou o formulário, ajudando a estabelecer o reconhecimento e a credibilidade da marca.

* **Contexto**: Um cabeçalho pode fornecer uma breve descrição da finalidade do formulário, ajudando os usuários a entender o contexto em que o formulário está sendo usado.

* **Navegação**: Um cabeçalho pode incluir links ou botões que permitem aos usuários navegar para outras partes do site ou aplicativo.

* **Informações**: Um cabeçalho pode incluir informações de contato ou links para recursos de ajuda, tornando mais fácil para os usuários obter assistência se precisarem.

* **Experiência do usuário**: Um cabeçalho pode ser usado para tornar o formulário mais simples, fornecendo uma maneira clara e intuitiva para os usuários acessarem e preencherem campos de formulário.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal do cabeçalho adaptativo do Forms foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta é uma tabela que mostra todas as versões suportadas, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível  com<br>[versão 2.0.4](/help/versions.md) e posterior | Compatível | Compatível |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/versions.md) documento.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do cabeçalho Adaptive Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de cabeçalho para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de cabeçalho com facilidade para uma experiência do usuário contínua.

### Guia Imagem {#image-tab}

Essa parte do cabeçalho contém o título e a imagem do cabeçalho.

![Imagetab](/help/adaptive-forms/assets/header_image.png)

* **Ativo de imagem** - Essa opção permite soltar um ativo como uma imagem com o arrastar e soltar do mouse. Também é possível fazer upload de um arquivo de um sistema de arquivos local usando a variável **Procurar** botão. Após adicionar uma imagem, três botões são exibidos na parte inferior da imagem. Após adicionar uma imagem, três botões são exibidos na parte inferior da imagem:
   * **Editar** - Toque ou clique **Editar** para gerenciar as representações do ativo no Editor de ativos.
   * **Limpar** - Toque ou clique **Limpar** para desmarcar a imagem selecionada no momento.
   * **Selecionar** - Toque ou clique **Selecionar**  para selecionar outra imagem da pasta Ativos.

* **Título** - Essa opção é usada para adicionar o cabeçalho ao cabeçalho. O texto predefinido é incluído na caixa de diálogo e pode ser modificado pelo usuário.
* **Link para** - Você pode vincular o cabeçalho à pasta usando o **Procurar** ícone .
* **Descrição** - Uma descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de uma imagem específica.
* **Tamanho (px)** - Ajuda a ajustar o comprimento e a largura da imagem, aumentando ou diminuindo os pixels.

![guia acessibilidade](/help/adaptive-forms/assets/header_accessibility.png)

* **Texto alternativo** - Essa opção é usada para inserir o texto que fornece uma alternativa em texto curta e descritiva para a imagem, que descreve a imagem para usuários deficientes visuais.

* **A imagem é decorativa** - Verifique se a imagem deve ser ignorada pela tecnologia assistiva e, portanto, não requer um texto alternativo. Isso se aplica somente a imagens decorativas.

### Guia Texto {#text-tab}

Esta seção permite inserir o texto a ser incluído no cabeçalho.

## Caixa de diálogo de design {#design-dialog}


