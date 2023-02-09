---
title: Componente principal adaptável do Forms - Contêiner do painel
description: Uso ou personalização do Componente principal do contêiner do painel adaptável do Forms.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 1%

---


# Contêiner do painel {#panel-container-adaptive-forms-core-component}

Em um Formulário adaptável, um painel é um elemento de contêiner que pode ser usado para agrupar elementos de formulário relacionados. Ele permite agrupar e organizar diferentes elementos de formulário de forma lógica e significativa. Isso pode ajudar a melhorar a estrutura geral e a legibilidade do formulário, facilitando a compreensão e a navegação pelos usuários.

Painéis também podem ser usados para criar seções recolhidas, o que pode ser útil para ocultar campos de formulário complexos ou usados com menos frequência, mantendo o formulário simples e fácil de usar. Também permite incluir outros componentes, como texto, caixa de seleção, botão, etc.

Também pode ser usado para definir diferentes ações baseadas em regras, como enviar formulário, abrir um site, mostrar/ocultar componentes ou adicionar uma instância de um painel.

**Exemplo**

![](/help/adaptive-forms/assets/panel-container.png)

## Uso {#reasons-to-use-panel-container}

Há vários motivos para usar um painel em um formulário, incluindo:

* **Organizar elementos de formulário**: Um painel pode ser usado para agrupar elementos de formulário relacionados, facilitando a compreensão e a navegação dos usuários.

* **Melhoria da estrutura dos formulários**: Ao agrupar elementos de formulário em painéis, é possível melhorar a estrutura geral e a legibilidade do formulário, facilitando sua compreensão.

* **Criação de seções recolhidas**: Painéis podem ser usados para criar seções recolhidas, o que pode ser útil para ocultar campos de formulário complexos ou usados com menos frequência, mantendo o formulário simples e fácil de usar.

* **Aprimoramento da usabilidade**: Ao usar painéis para organizar elementos de formulário, ele pode tornar o formulário mais fácil de usar e fácil de usá-lo, o que pode resultar em taxas de conclusão mais altas.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal do contêiner do painel adaptável do Forms foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta é uma tabela que mostra todas as versões suportadas, a compatibilidade AEM e os links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível  com<br>[versão 2.0.4](/help/versions.md) e posterior | Compatível | Compatível |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do contêiner do painel adaptável Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do contêiner do painel para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de contêiner de painel com facilidade para uma experiência do usuário contínua.

### Guia básica {#basic-tab}

![Guia Básica](/help/adaptive-forms/assets/panelcontainer_basictab.png)

* **Nome** - É possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não deve conter espaços ou caracteres especiais.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Ocultar Título** - Selecione a opção para ocultar o Título do componente.

* **Vincular dados no objeto** - Escolha &quot;Quebrar dados em um objeto&quot; para colocar os dados de campo do Assistente dentro de um objeto JSON. Se não for escolhido, o JSON de envio de dados terá uma estrutura simples para os campos do Assistente.

* **Layout** - Você pode ter um layout fixo (Simples) ou um layout flexível (Grade Responsiva) para o assistente. O layout Simples mantém tudo fixo no lugar, enquanto a Grade Responsiva permite que você ajuste a posição dos componentes para atender às suas necessidades. Por exemplo, use Grade Responsiva para alinhar &quot;Nome&quot;, &quot;Nome do Meio&quot; e &quot;Sobrenome&quot; em um formulário em uma única linha.

* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.
* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente** - Selecione a opção para desativar o componente. O componente desativado não é ativo ou editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Conteúdo da Ajuda {#help-content}

![Guia Conteúdo da Ajuda](/help/adaptive-forms/assets/panelcontainer_helptab.png)

* **Descrição curta** - Uma breve descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative o **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta** - Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda** - O texto da Ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto da Ajuda fornece informações mais detalhadas do que o rótulo de um campo de formulário ou o texto de espaço reservado, e foi projetado para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/panelcontainer_accessibilitytab.png)

* **Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias assistivas, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

* **Função de HTML para anúncio do leitor de tela** - A função HTML é um atributo usado para especificar a finalidade de um elemento HTML para tecnologias de assistência, como leitores de tela. O atributo de função é usado para fornecer contexto e significado semântico adicionais a um elemento, facilitando a interpretação e o anúncio do conteúdo pelos leitores de tela. Por exemplo, no AEM Forms, o rótulo de um campo de formulário pode ter a função de &quot;rótulo&quot; e seu campo de entrada pode ter a função de &quot;caixa de texto&quot;. Isso ajuda o leitor de tela a entender a relação entre o rótulo e o campo de entrada e anunciá-los corretamente ao usuário.




