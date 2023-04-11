---
title: Acordeão de formulário adaptável
description: Use o acordeão para organizar e simplificar um formulário longo ou complexo, dividindo-o em seções menores e mais fáceis de se controlar.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
source-git-commit: 0cfdc56fe5508e156eee2ae818be311748af7247
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 95%

---

# Componente de acordeão {#accordion-component-adaptive-forms-core-component}

O componente principal de acordeão permite que os usuários criem seções que podem ser expandidas ou recolhidas em um formulário adaptável. Ele geralmente é usado para organizar e simplificar formulários longos ou complexos, dividindo-os em seções menores e mais fáceis de se controlar. Cada seção de um acordeão é normalmente representada por um cabeçalho, no qual o usuário pode clicar para expandir ou recolher o conteúdo correspondente. O conteúdo pode ser qualquer componente principal.

## Uso {#usage}

Há várias vantagens de se usar um acordeão em um formulário adaptável, incluindo:

* **Economia de espaço**: um acordeão permite que os usuários expandam e recolham as seções de um formulário, reduzindo a quantidade de espaço necessária para exibir todos os campos do formulário ao mesmo tempo.

* **Navegação**: um acordeão pode ser usado para criar uma estrutura de navegação hierárquica, facilitando para os usuários encontrarem os campos de formulário necessários.

* **Experiência do usuário**: o acordeão pode ser usado para tornar o formulário mais fácil de usar, fornecendo uma maneira clara e intuitiva para os usuários acessarem e preencherem campos de formulário.

* **Formulários longos**: o acordeão é um componente ideal para lidar com formulários longos, pois permite que os usuários se concentrem em uma seção de cada vez, ao invés de tentar processar informações demais de uma só vez.

Você pode usar:

* A [caixa de diálogo de configuração](#configure-dialog) para definir as propriedades do componente de acordeão.

* O [popover Selecionar painel](#select-panel-popover) para definir a ordem dos painéis do acordeão. Isso permite que o autor organize os painéis na ordem em que eles devam aparecer.

* Opções para um autor de formulários ativar ou desativar determinados recursos na [caixa de diálogo de design](#design-dialog). Por exemplo, um autor pode optar por desativar determinados campos ou seções de um formulário. Essas opções permitem que o autor tenha um maior controle sobre o design e as funcionalidades do formulário, facilitando a criação de formulários personalizados para necessidades específicas da organização.

As caixas de diálogo de configuração e de design, bem como o popover Selecionar painel, fazem parte dos componentes principais que foram desenvolvidos para facilitar a criação de formulários e fornecem uma maneira eficiente de criar formulários complexos.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal Adaptive Forms Accordion foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, AEM compatibilidade e links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com<br>[versão 1.1.12](/help/adaptive-forms/version.md) e posterior, mas inferior a 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente de acordeão na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência de acordeão para visitantes com a caixa de diálogo de configuração. Você também pode facilmente definir itens, painéis, comportamentos e a aparência do acordeão para obter uma experiência de usuário perfeita.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/accordion_basictab.png)

* **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

* **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

* **Ocultar título**: selecione essa opção para ocultar o título do componente.

* **Agrupar dados em um objeto**: escolha “Agrupar dados em um objeto” para colocar os dados de campo do assistente dentro de um objeto JSON. Se isto não for definido, o JSON de envio de dados terá uma estrutura simples para os campos do assistente.

* **Layout**: o assistente pode ter um layout fixo (simples) ou um layout flexível (grade responsiva). O layout simples mantém tudo fixo no lugar, enquanto a grade responsiva permite que você ajuste a posição dos componentes para atender às suas necessidades. Por exemplo, use a grade responsiva para alinhar “Nome”, “Nome do meio” e “Sobrenome” em uma única linha do formulário.

* **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.
* **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Itens {#items-tab}

![Guia Itens](/help/adaptive-forms/assets/accordion_itemstab.png)

O botão Adicionar permite selecionar um componente da janela de seleção de componentes para adicionar como um painel. Após adicionar o componente, você verá as seguintes opções:

* **Ícone**: o ícone identifica o componente do painel na lista. Você pode passar o mouse sobre o ícone para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição**: a descrição usada como o texto do painel. Por padrão, o nome do componente é selecionado para o painel.
* **Excluir** - Toque ou clique para excluir o painel do componente Acordeão.
* **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem dos painéis.

### Guia Conteúdo de ajuda {#help-content}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/accordion_helpcontent.png)

* **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

* **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/accordion_accessibility.png)

**Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que os criadores de modelos controlem a exibição padrão dos elementos. Para o componente de acordeão de formulários adaptáveis, você pode definir o seguinte:

* Os tipos de elementos de cabeçalho HTML que são permitidos e definidos como padrão (como H1, H2, H3 etc.)
* Os componentes principais que um criador de formulário pode adicionar a um acordeão no editor de formulários adaptáveis
* Nomes simples para estilos (classes CSS) que podem ser aplicados na caixa de diálogo de propriedades do componente de acordeão no editor de formulários adaptáveis.

Isso ajuda a tornar o processo de criação e personalização de formulários mais simples e eficiente.

### Guia Propriedades {#properties-tab-design}

A guia Propriedades permite que os autores de modelo definam os elementos de cabeçalho HTML padrão e permitidos para autores de formulários:

![Guia de propriedades da caixa de diálogo de design](/help/assets/accordion-design-properties.png)

* **Elementos de cabeçalho permitidos**: uma lista suspensa com várias opções que permitem ao autor do modelo escolher quais elementos de cabeçalho podem ser usados pelo autor do formulário no acordeão.

* **Elemento de cabeçalho padrão**: uma lista suspensa que define os elementos de cabeçalho padrão para o componente de acordeão.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** permite que o editor de modelos defina os componentes que podem ser adicionados como itens aos painéis do componente de acordeão no editor de formulários adaptáveis.

![Guia Componentes permitidos](/help/adaptive-forms/assets/accordion_allowedcomponents.png)

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar estilos de CSS de um componente. O componente principal de acordeão de formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Guia Estilo](/help/adaptive-forms/assets/accordion_style.png)

* **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o componente de acordeão.

* **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

