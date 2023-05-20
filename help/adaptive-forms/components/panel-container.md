---
title: Componente principal dos Formulários adaptáveis - Container do painel
description: Utilização ou personalização do Componente principal de container do painel dos Formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 104836fe-8325-47de-978d-1ff2d6a9dd15
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1696'
ht-degree: 100%

---

# Container do painel {#panel-container-adaptive-forms-core-component}

Em um formulário adaptável, um painel é um elemento de container que pode ser usado para agrupar elementos de formulário relacionados. Ele permite agrupar e organizar diferentes elementos de formulário de forma lógica e significativa. Isso pode ajudar a melhorar a estrutura geral e a legibilidade do formulário, facilitando a compreensão e a navegação pelos usuários.

Painéis podem ser usados para criar seções que podem ser recolhidas, o que é útil para ocultar campos de formulário complexos ou usados com menos frequência, mantendo o formulário simples e fácil de usar. Também é possível incluir outros componentes, como texto, caixa de seleção e botão.

Além disso, eles podem ser usados para definir diferentes ações baseadas em regras, como enviar formulário, abrir um site, mostrar/ocultar componentes ou adicionar uma instância de um painel.

**Exemplo**

![](/help/adaptive-forms/assets/panel-container.png)

## Uso {#reasons-to-use-panel-container}

Há vários motivos para usar um painel em um formulário, incluindo:

* **Organizar elementos de formulário**: um painel pode ser usado para agrupar elementos de formulário relacionados, facilitando a compreensão e a navegação dos usuários.

* **Melhoria da estrutura dos formulários**: ao agrupar elementos de formulário em painéis, é possível melhorar a estrutura geral e a legibilidade do formulário, facilitando sua compreensão.

* **Criação de seções recolhidas**: painéis podem ser usados para criar seções recolhidas, o que pode ser útil para ocultar campos de formulário complexos ou usados com menos frequência, mantendo o formulário simples e fácil de usar.

* **Aprimoramento da usabilidade**: ao usar painéis para organizar elementos de formulário, ele pode tornar o formulário mais fácil de usar e intuitivo, o que pode resultar em taxas de conclusão mais altas.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de Container do painel dos Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Para mais informações sobre o desenvolvimento dos Componentes principais, consulte a [Documentação do desenvolvedor dos componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do container do painel para visitantes com a caixa de diálogo Configurar. Você também pode definir opções de container de painel com facilidade para proporcionar uma experiência do usuário contínua.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/panelcontainer_basictab.png)

* **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

* **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

* **Ocultar título**: selecione essa opção para ocultar o título do componente.

* **Agrupar dados em um objeto**: escolha “Agrupar dados em um objeto” para colocar os dados de campo do assistente dentro de um objeto JSON. Se isto não for definido, o JSON de envio de dados terá uma estrutura simples para os campos do assistente.

* **Layout**: o assistente pode ter um layout fixo (simples) ou um layout flexível (grade responsiva). O layout simples mantém tudo fixo no lugar, enquanto a grade responsiva permite que você ajuste a posição dos componentes para atender às suas necessidades. Por exemplo, use a grade responsiva para alinhar “Nome”, “Nome do meio” e “Sobrenome” em uma única linha do formulário.

* **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.
* **Ocultar componente** - selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Conteúdo de ajuda {#help-content}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/panelcontainer_helptab.png)

* **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

* **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/panelcontainer_accessibilitytab.png)

* **Texto para leitores de tela**: isso se refere ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

* **Função de HTML para anúncio do leitor de tela** - A função HTML é um atributo usado para especificar a finalidade de um elemento HTML para tecnologias assistivas, como leitores de tela. O atributo de função é usado para fornecer contexto e significado semântico adicionais a um elemento, facilitando a interpretação e o anúncio do conteúdo pelos leitores de tela. Por exemplo, no AEM Forms, o rótulo de um campo de formulário pode ter a função de “rótulo” e seu campo de entrada pode ter a função de “caixa de texto”. Isso ajuda o leitor de tela a entender a relação entre o rótulo e o campo de entrada e anunciá-los corretamente ao usuário.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar os estilos CSS do componente de container do painel.

### Guia Componentes permitidos {#allowed-components-tab}

![Guias Componentes permitidos](/help/adaptive-forms/assets/panel_allowedcomponent.png)

A guia **Componentes permitidos** permite que o editor de modelos defina os componentes que podem ser adicionados como itens aos painéis do componente de container do painel no editor de formulários adaptáveis.

### Guia Componentes padrão {#default-component-tab}

Esta guia permite que o editor de modelos mapeie os componentes que podem ser adicionados como itens aos painéis do componente de container do painel no editor de formulários adaptáveis.

![Componente padrão do painel](/help/adaptive-forms/assets/panel_defaultcomponent.png)

### Configurações responsivas {#responsive-settings}

Essa guia permite que o editor de modelos defina o número de colunas a serem exibidas na grade responsiva.

![Grade responsiva](/help/adaptive-forms/assets/panel_responsivesettings.png)

### Guia Configurações do container {#container-setting-tab}

A guia de configurações do container permite definir a posição dos componentes no editor de formulários adaptáveis.

![Configurações do container](/help/adaptive-forms/assets/panel_settings.png)

* **Layout**: o layout simples mantém tudo fixo no lugar, enquanto a grade responsiva permite que você altere a posição dos componentes para atender às suas necessidades.
* **Desabilitar layout**: também é possível desabilitar a seleção de layout na caixa de diálogo de edição marcando a caixa **Desabilitar layout**.
* **Habilitar imagem de fundo**: essa guia permite definir a cor e a imagem do fundo no editor de modelos.
* **Habilitar cor de fundo**: essa guia permite definir a cor do fundo no editor de modelos.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de Container de painel dos formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Guia Estilo](/help/adaptive-forms/assets/panel_style.png)

* **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o componente principal de formulários adaptáveis.

* **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um dos formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo de design, atualize-os na guia Estilos e salve as alterações.

* **Função de HTML para anúncio do leitor de tela** - A função HTML é um atributo usado para especificar a finalidade de um elemento HTML para tecnologias assistivas, como leitores de tela. O atributo de função é usado para fornecer contexto e significado semântico adicionais a um elemento, facilitando a interpretação e o anúncio do conteúdo pelos leitores de tela. Por exemplo, no AEM Forms, o rótulo de um campo de formulário pode ter a função de “rótulo” e seu campo de entrada pode ter a função de “caixa de texto”. Isso ajuda o leitor de tela a entender a relação entre o rótulo e o campo de entrada e anunciá-los corretamente ao usuário.

