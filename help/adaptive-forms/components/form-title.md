---
title: Componente principal dos Formulários adaptáveis - Título
description: Utilização ou personalização do Componente principal de Título dos Formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 33eac885-8d66-4a5c-9a32-0ba11e6de293
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '864'
ht-degree: 100%

---


# Componente Título de formulário{#title-input-adaptive-forms-core-component}

Em um Formulário adaptável, um “título” refere-se ao texto que aparece na parte superior do formulário, normalmente abaixo do cabeçalho. O título é especificado usando o componente de Título. Esse componente pode ser adicionado ao layout do formulário e seu texto pode ser editado para corresponder à finalidade ou ao tópico do formulário. O título serve como um rótulo ou uma breve descrição do formulário para o usuário, e ajuda a distinguir o formulário de outros.

{{traditional-aem}}

**Exemplo**

![exemplo de título](/help/adaptive-forms/assets/title.png)

## Uso {#reasons-to-use-title-in-an-adaptive-form}

Há vários motivos pelos quais é uma boa prática usar um título em um formulário:

- **Clareza**: um título identifica claramente a finalidade do formulário, o que ajuda os usuários a entender quais informações precisam ser fornecidas.

- **Organização**: um título pode ajudar a organizar formulários por tópico ou finalidade, o que facilita para os usuários encontrar o formulário necessário.

- **Acessibilidade**: um título é um elemento essencial para os usuários com necessidades de acessibilidade, pois é lido em voz alta pelos leitores de tela, ajudando os usuários a entender o contexto do formulário.

- **Marca**: um título também pode ser usado para exibir o nome de uma empresa ou organização, o que ajuda a criar um senso de confiança e familiaridade com o usuário.

- **Navegação**: um título também pode ser útil para navegar pelo formulário, especialmente se ele for longo ou complexo.

- **Otimização de mecanismo de pesquisa (SEO)**: ter um título no formulário também ajuda na SEO, já que os mecanismos de pesquisa usam o título para determinar a relevância de uma página da Web para uma consulta de pesquisa.

Em geral, o título de um formulário é um aspecto importante da experiência do usuário e deve ser usado para fornecer um rótulo claro e conciso para o formulário, que ajude os usuários a entender o contexto e a finalidade do formulário.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal de título de formulários adaptáveis foi lançado em fevereiro de 2023 como parte dos componentes principais 2.0.4 para serviços na nuvem e dos componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM Forms 6.5.16.0 ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_br). -->


## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de Título dos Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de título para visitantes com a caixa de diálogo Configurar. Você também pode definir opções de título com facilidade para proporcionar uma experiência do usuário contínua.

![Guia Básico](/help/adaptive-forms/assets/title_properties.png)

A caixa de diálogo de edição permite que o autor de conteúdo defina o texto do título, e selecione o nível do cabeçalho.

- **Título**: o título permite identificar facilmente um componente em um formulário; por padrão, ele aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.
- **Tipo / Tamanho** - Define o nível de cabeçalho do título.
- **ID**: Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de Dados.
   - Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   - Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   - A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

## Caixa de diálogo Design {#design-dialog}

A guia Design é usada para definir e gerenciar os estilos CSS para o componente de título.

### Título

A guia Título permite que os autores de modelo definam elementos de cabeçalho de HTML padrão e permitido para autores de formulários:

![Guia título da caixa de diálogo de Design](/help/adaptive-forms/assets/title_heading.png)

- **Elementos de cabeçalho permitidos**: uma lista com várias opções que permitem ao autor do modelo escolher quais elementos de cabeçalho podem ser usados pelo autor para o título.

- **Elemento de cabeçalho padrão**: uma lista suspensa que define o elemento Cabeçalho padrão para o componente Título.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal do Seletor de datas de formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Guia Título da caixa de diálogo de design](/help/adaptive-forms/assets/title_styles.png)

- **Classes padrão do CSS**: você pode fornecer uma classe padrão do CSS ao componente principal título para formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Guia Formatos {#format-tab}

A guia Formatos permite especificar os formatos de data padrão e personalizados.

![Guia Formato](/help/adaptive-forms/assets/title_styles.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=pt-BR)

-->

## Artigos relacionados {#related-articles}


{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}