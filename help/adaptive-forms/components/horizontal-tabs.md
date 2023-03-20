---
title: Componente principal adaptável do Forms - guias horizontais
description: Uso ou personalização do Componente principal de guias horizontais adaptáveis do Forms.
role: Architect, Developer, Admin, User
exl-id: fbdf330b-3b85-4f94-9dab-eea8465fba67
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1609'
ht-degree: 2%

---

# Guias horizontais {#horizontal-tabs-adaptive-forms-core-component}

As guias horizontais em um formulário adaptável referem-se a um padrão de design em que várias seções de um formulário são agrupadas e exibidas como guias separadas, alinhadas horizontalmente. O usuário pode alternar entre as guias para acessar diferentes seções do formulário. Cada guia atua como um acionador para mostrar e ocultar o conteúdo do formulário relacionado. As guias horizontais ajudam a organizar formulários longos em seções gerenciáveis e melhoram a experiência do usuário. Guias podem ajudar a tornar um formulário mais acessível para usuários portadores de deficiência, pois podem alternar entre seções usando a navegação pelo teclado.

Normalmente, as guias são criadas como uma série de links ou botões, com cada link ou botão correspondente a uma seção do formulário. Quando um usuário clica em uma guia, o conteúdo do formulário é atualizado dinamicamente para mostrar a seção correspondente.

## Uso {#reasons-to-use-horizontal-tabs}

Os motivos comuns para usar guias horizontais em um formulário adaptável são:

* **Maior usabilidade**: Guias horizontais facilitam para os usuários navegarem pelo formulário, especialmente se ele tiver várias seções ou um grande número de campos.

* **Gerenciamento do espaço**: As guias horizontais ajudam a preservar o espaço na tela, agrupando seções de formulário relacionadas em guias e exibindo apenas uma seção de cada vez.

* **Melhor organização**: As guias fornecem uma estrutura clara e organizada para um formulário, tornando mais fácil para os usuários compreender e preencher o formulário.

* **Aumento do envolvimento do usuário**: Guias horizontais podem tornar um formulário mais atraente visualmente e atraente para os usuários, o que pode melhorar a taxa de preenchimento do formulário.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal Adaptive Forms Accordion foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, AEM compatibilidade e links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com<br>[versão 2.0.4](/help/adaptive-forms/version.md) e posterior | Compatível com<br>[versão 1.1.12](/help/adaptive-forms/version.md) e posterior, mas inferior a 2.0.0. |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/adaptive-forms/version.md) documento.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal das guias horizontais adaptáveis do Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageHorizontal guias/v1/pageHorizontal ). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de guias horizontais para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de guias Horizontais com facilidade para uma experiência do usuário contínua.

### Guia básica {#basic-tab}

![Guia Básica](/help/adaptive-forms/assets/tabsontop_basictab.png)

* **Nome** - É possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não deve conter espaços ou caracteres especiais.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Ocultar Título** - Selecione a opção para ocultar o Título do componente.

* **Vincular dados no objeto** - Escolha &quot;Quebrar dados em um objeto&quot; para colocar os dados de campo do Assistente dentro de um objeto JSON. Se não for escolhido, o JSON de envio de dados terá uma estrutura simples para os campos do Assistente.

* **Layout** - Você pode ter um layout fixo (Simples) ou um layout flexível (Grade Responsiva) para o assistente. O layout Simples mantém tudo fixo no lugar, enquanto a Grade Responsiva permite que você ajuste a posição dos componentes para atender às suas necessidades. Por exemplo, use Grade Responsiva para alinhar &quot;Nome&quot;, &quot;Nome do Meio&quot; e &quot;Sobrenome&quot; em um formulário em uma única linha.

* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.
* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente** - Selecione a opção para desativar o componente. O componente desativado não é ativo ou editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Itens {#items-tab}

![Guia Itens](/help/adaptive-forms/assets/tabsontop_itemstab.png)

O **Adicionar** permite selecionar um componente para adicionar como um painel na janela de seleção de componentes. Após adicionar o componente, você pode ver as seguintes opções:

* **Ícone** - O ícone identifica o componente do painel na lista. Você pode passar o mouse sobre o ícone para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição** - A descrição usada como o texto do painel. Por padrão, o nome do componente selecionado para o painel.
* **Excluir** - Toque ou clique para excluir o painel do componente de guia horizontal.
* **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem dos painéis.

### Guia Conteúdo da Ajuda {#help-content}

![Guia Conteúdo da Ajuda](/help/adaptive-forms/assets/tabsontop_helptab.png)

* **Descrição curta** - Uma breve descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative o **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta** - Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda** - O texto da Ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto da Ajuda fornece informações mais detalhadas do que o rótulo de um campo de formulário ou o texto de espaço reservado, e foi projetado para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/tabsontop_accessibilitytab.png)

* **Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias assistivas, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

* **Função de HTML para anúncio do leitor de tela** - A função HTML é um atributo usado para especificar a finalidade de um elemento HTML para tecnologias de assistência, como leitores de tela. O atributo de função é usado para fornecer contexto e significado semântico adicionais a um elemento, facilitando a interpretação e o anúncio do conteúdo pelos leitores de tela. Por exemplo, no AEM Forms, o rótulo de um campo de formulário pode ter a função de &quot;rótulo&quot; e seu campo de entrada pode ter a função de &quot;caixa de texto&quot;. Isso ajuda o leitor de tela a entender a relação entre o rótulo e o campo de entrada e anunciá-los corretamente ao usuário.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design permite que os criadores do modelo controlem como as coisas são exibidas por padrão. Para o componente Adaptive Forms, você pode definir o seguinte:

* Os componentes principais que um criador de formulário pode adicionar às guias horizontais no editor adaptável do Forms
* Nomes simples para estilos (classes CSS) que podem ser aplicados na caixa de diálogo de propriedades do componente de guias horizontais no editor Adaptive Forms.

Isso ajuda a tornar o processo de criação e personalização de formulários mais simples e eficiente.

### Guia Componentes permitidos {#allowed-components-tab}

O **Componentes permitidos** A guia permite que o editor de modelo defina os componentes que podem ser adicionados como itens aos painéis no componente de guias Horizontais no editor Adaptive Forms.

![Guias horizontais](/help/adaptive-forms/assets/horizontaltabs_designdilog.png)

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar estilos de CSS de um componente. O Componente principal de guias horizontais adaptáveis do Forms é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Guia Estilo](/help/adaptive-forms/assets/horizontaltabs_designstyletab.png)

* **Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal de guias horizontais do Adaptive Forms.

* **Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.
