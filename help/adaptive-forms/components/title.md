---
title: Componente principal adaptável do Forms - Título
description: Uso ou personalização do Componente principal do título adaptável do Forms.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 15%

---


# Título {#title-input-adaptive-forms-core-component}

Em um formulário adaptável, um &quot;título&quot; refere-se ao texto que aparece na parte superior do formulário, normalmente abaixo do cabeçalho. O título é especificado usando o componente Título. Esse componente pode ser adicionado ao layout do formulário e seu texto pode ser editado para corresponder à finalidade ou ao tópico do formulário. O título serve como um rótulo ou uma breve descrição do formulário para o usuário, e ajuda a distinguir o formulário de outros.

**Exemplo**

![](/help/adaptive-forms/assets/title.png)

## Uso {#reasons-to-use-title-in-an-adaptive-form}

Há vários motivos pelos quais é uma boa prática usar um título em um formulário:

* **Clareza**: Um título identifica claramente a finalidade do formulário, o que ajuda os usuários a entender quais informações precisam ser fornecidas.

* **Organização**: Um título pode ajudar a organizar formulários por tópico ou finalidade, o que facilita para os usuários encontrar o formulário necessário.

* **Acessibilidade**: Um título é um elemento essencial para os usuários com necessidades de acessibilidade, pois é lido em voz alta pelos leitores de tela, ajudando os usuários a entender o contexto do formulário.

* **Marca**: Um título também pode ser usado para exibir o nome de uma empresa ou organização, o que ajuda a criar um senso de confiança e familiaridade com o usuário.

* **Navegação**: Um título também pode ser útil para navegar pelo formulário, especialmente se ele for longo ou complexo.

* **Otimização do mecanismo de pesquisa (SEO)**: Ter um título no formulário também ajuda na SEO, já que os mecanismos de pesquisa usam o título para determinar a relevância de uma página da Web para um query de pesquisa.

Em geral, o título de um formulário é um aspecto importante da experiência do usuário e deve ser usado para fornecer um rótulo claro e conciso para o formulário, que ajude os usuários a entender o contexto e a finalidade do formulário.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal do título adaptável do Forms foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta é uma tabela que mostra todas as versões compatíveis, compatibilidade de AEM e links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível  com<br>[versão 2.0.4](/help/versions.md) e posterior | Compatível | Compatível |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do título adaptativo do Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de título para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de título com facilidade para uma experiência do usuário contínua.

![Guia Básica](/help/adaptive-forms/assets/title_properties.png)

A caixa de diálogo de edição permite que o autor de conteúdo defina o texto do título, e selecione o nível do cabeçalho.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.
* **Tipo / Tamanho** - Define o nível de cabeçalho do título.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de Dados.
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente Seletor de data.

### Título

A guia Título permite que os autores de modelo definam elementos de cabeçalho de HTML padrão e permitido para autores de formulários:

![Guia de título da caixa de diálogo Design](/help/assets/accordion-design-properties.png)

* **Elementos de cabeçalho permitidos**: Uma lista com várias opções que permitem ao autor do modelo escolher quais elementos de cabeçalho podem ser usados pelo autor para o Título.

* **Elemento de cabeçalho padrão**: Uma lista suspensa que define o elemento Cabeçalho padrão para o componente Título .


### Guia Estilos {#styles-tab}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para um componente. O Componente principal do seletor de data adaptável do Forms é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal do seletor de data da Forms adaptável.

**Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Guia Formatos {#format-tab}

A guia format permite especificar os formatos de data padrão e personalizados.

