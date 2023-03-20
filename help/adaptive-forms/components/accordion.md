---
title: Acordo de formulário adaptável
description: Use a opção para organizar e simplificar um formulário longo ou complexo, dividindo-o em seções menores e mais gerenciáveis.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
source-git-commit: 0cfdc56fe5508e156eee2ae818be311748af7247
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 3%

---

# Componente Acordeão {#accordion-component-adaptive-forms-core-component}

O Componente principal acordeão permite que os usuários criem seções expansíveis e que podem ser recolhidas em um Formulário adaptável. Geralmente é usado para organizar e simplificar formulários longos ou complexos, dividindo-os em seções menores e mais gerenciáveis. Cada seção de uma opção é normalmente representada por um cabeçalho, no qual o usuário pode clicar para expandir ou recolher o conteúdo correspondente. O conteúdo pode ser qualquer Componente principal.

## Uso {#usage}

Há vários motivos pelos quais é benéfico incluir uma opção em um formulário adaptável, incluindo:

* **Economia de espaço**: Uma opção permite que os usuários expandam e recolham seções de um formulário, reduzindo a quantidade de espaço necessário para exibir todos os campos de formulário ao mesmo tempo.

* **Navegação**: Uma opção pode ser usada para criar uma estrutura de navegação hierárquica, facilitando para os usuários encontrarem os campos de formulário necessários.

* **Experiência do usuário**: A opção pode ser usada para tornar o formulário mais fácil de usar, fornecendo uma maneira clara e intuitiva para os usuários acessarem e preencherem campos de formulário.

* **Forms Longo**: O acordeão é um componente ideal para lidar com formulários longos, pois permite que os usuários se concentrem em uma seção de cada vez, em vez de tentar processar muitas informações de uma só vez.

Você pode usar:

* O [caixa de diálogo configurar](#configure-dialog) para especificar as propriedades do componente acordeão.

* O [Selecionar o volume do painel](#select-panel-popover)  para definir a ordem dos painéis do acordeão. Isso permite que o autor organize os painéis na ordem em que eles devem aparecer.

* Opções para um autor de formulários para ativar ou desativar determinados recursos na [caixa de diálogo de design](#design-dialog). Por exemplo, um autor pode optar por desativar determinados campos ou seções de um formulário. Essas opções permitem que o autor tenha maior controle sobre o design e a funcionalidade do formulário, facilitando a criação de formulários adaptados às necessidades específicas da organização.

A caixa de diálogo configurar e selecionar o painel e a caixa de diálogo de design fazem parte dos componentes principais que são criados para facilitar a criação dos formulários e fornecer uma maneira eficiente de criar formulários complexos.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal Adaptive Forms Accordion foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, AEM compatibilidade e links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com<br>[versão 2.0.4](/help/adaptive-forms/version.md) e posterior | Compatível com<br>[versão 1.1.12](/help/adaptive-forms/version.md) e posterior, mas inferior a 2.0.0. |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/adaptive-forms/version.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente acordeão na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência em acordeão para visitantes com a caixa de diálogo Configurar . Você também pode definir itens de acordeão, painéis, comportamento e aparência facilmente para obter uma experiência do usuário contínua.

### Guia básica {#basic-tab}

![Guia Básica](/help/adaptive-forms/assets/accordion_basictab.png)

* **Nome** - É possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não deve conter espaços ou caracteres especiais.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Ocultar Título** - Selecione a opção para ocultar o Título do componente.

* **Vincular dados no objeto** - Escolha &quot;Quebrar dados em um objeto&quot; para colocar os dados de campo do Assistente dentro de um objeto JSON. Se não for escolhido, o JSON de envio de dados terá uma estrutura simples para os campos do Assistente.

* **Layout** - Você pode ter um layout fixo (Simples) ou um layout flexível (Grade Responsiva) para o assistente. O layout Simples mantém tudo fixo no lugar, enquanto a Grade Responsiva permite que você ajuste a posição dos componentes para atender às suas necessidades. Por exemplo, use Grade Responsiva para alinhar &quot;Nome&quot;, &quot;Nome do Meio&quot; e &quot;Sobrenome&quot; em um formulário em uma única linha.

* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.
* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente** - Selecione a opção para desativar o componente. O componente desativado não é ativo ou editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Itens {#items-tab}

![Guia Itens](/help/adaptive-forms/assets/accordion_itemstab.png)

O botão Adicionar permite selecionar um componente a ser adicionado como um painel a partir da janela de seleção de componentes. Após adicionar o componente, você pode ver as seguintes opções:

* **Ícone** - O ícone identifica o componente do painel na lista. Você pode passar o mouse sobre o ícone para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição** - A descrição usada como o texto do painel. Por padrão, o nome do componente é selecionado para o painel.
* **Excluir** - Toque ou clique para excluir o painel do componente Acordeão.
* **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem dos painéis.

### Guia Conteúdo da Ajuda {#help-content}

![Guia Conteúdo da Ajuda](/help/adaptive-forms/assets/accordion_helpcontent.png)

* **Descrição curta** - Uma breve descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative o **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta** - Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda** - O texto da Ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto da Ajuda fornece informações mais detalhadas do que o rótulo de um campo de formulário ou o texto de espaço reservado, e foi projetado para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/accordion_accessibility.png)

**Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias assistivas, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design permite que os criadores do modelo controlem como as coisas são exibidas por padrão. Para o componente Adaptive Forms Acordeon, você pode definir o seguinte:

* O tipo de elementos de cabeçalho de HTML que são permitidos e definidos como padrão (como H1, H2, H3, etc.)
* Os componentes principais que um criador de formulário pode adicionar à opção no editor Adaptive Forms
* Nomes simples para estilos (classes CSS) que podem ser aplicados na caixa de diálogo de propriedades do componente acordeão no editor Adaptive Forms.

Isso ajuda a tornar o processo de criação e personalização de formulários mais simples e eficiente.

### Guia Propriedades {#properties-tab-design}

A guia Propriedades permite que os autores de modelo definam elementos de cabeçalho de HTML padrão e permitido para autores de formulários:

![Guia de propriedades da caixa de diálogo de Design](/help/assets/accordion-design-properties.png)

* **Elementos de cabeçalho permitidos**: Uma lista suspensa com várias opções que permitem ao autor do modelo escolher quais elementos de cabeçalho podem ser usados pelo autor da forma de opção.

* **Elemento de cabeçalho padrão**: Uma lista suspensa define o elemento Cabeçalho padrão para o componente acordeão.

### Guia Componentes permitidos {#allowed-components-tab}

O **Componentes permitidos** Essa guia permite que o editor de modelos defina os componentes que podem ser adicionados como itens aos painéis no componente Acordeão no editor Adaptive Forms.

![Guia Componentes permitidos](/help/adaptive-forms/assets/accordion_allowedcomponents.png)

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar estilos de CSS de um componente. O Componente principal Adaptive Forms Acordeon é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Guia Estilo](/help/adaptive-forms/assets/accordion_style.png)

* **Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o componente acordeão.

* **Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

