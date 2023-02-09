---
title: Componente principal adaptável do Forms - Botão
description: Uso ou personalização do Componente principal do botão Adaptive Forms.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1491'
ht-degree: 2%

---


# Componente de Botão  {#button-component-adaptive-forms-core-component}

Um botão em um formulário adaptável é um elemento da interface do usuário que permite aos usuários iniciar uma ação quando clicados. O elemento de botão pode ser usado para enviar um formulário, redefinir um formulário ou executar outras ações, como navegar para uma página diferente ou acionar o código personalizado. O botão pode ser criado usando o Componente principal do botão.

O Editor de regras adaptável Forms permite que os usuários definam várias ações para o componente de botão. Essas ações incluem abrir um site, mostrar ou ocultar componentes do formulário, adicionar uma instância de um painel ou componente, enviar ou redefinir um formulário e muito mais.

O Adaptive Forms também fornece componentes de botão separados para enviar ou redefinir um formulário, mas o componente de botão também pode ser configurado para executar essas ações, se necessário.

Os usuários podem acessar a lista completa de ações compatíveis com o componente de botão usando o Editor de regras adaptável do Forms. O Editor de regras permite que os usuários criem regras acionadas por vários eventos, como quando um botão é clicado, quando um formulário é carregado ou quando um valor de campo é alterado. Essas regras podem ser usadas para executar várias ações, como mostrar ou ocultar componentes, definir valores de campo ou enviar o formulário.

## Uso {#reasons-to-use-button}

Há vários motivos pelos quais é benéfico incluir um botão em um formulário adaptável, incluindo:

* **Envio do formulário**: Normalmente, um botão é usado para enviar um formulário, permitindo que os usuários enviem os dados inseridos no servidor para processamento.

* **Redefinição de formulário**: Os botões também podem ser usados para redefinir um formulário, limpando todos os dados inseridos pelo usuário.

* **Navegação**: Os botões podem ser usados para navegar entre diferentes seções de um formulário ou páginas diferentes em um site.

* **Manuseio de evento**: Os botões podem ser usados para acionar eventos diferentes, como abrir um site, mostrar/ocultar componentes, adicionar uma instância de um painel ou componente ao botão.

* **Interatividade**: Os botões podem ser usados para criar formulários interativos. Por exemplo, um botão pode ser usado para abrir uma caixa de diálogo modal ou para alternar uma seção do formulário.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal do botão Adaptive Forms v1 foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta é uma tabela que mostra todas as versões suportadas, a compatibilidade AEM e os links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível  com<br>[versão 2.0.4](/help/versions.md) e posterior | Compatível | Compatível |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do botão adaptável Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de botão para visitantes com a caixa de diálogo Configurar . Você também pode definir propriedades de botão com facilidade para uma experiência do usuário contínua.

### Guia básica {#basic-tab}

![Guia básica](/help/adaptive-forms/assets/button_basictab.png)

* **Nome** - É possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não deve conter espaços ou caracteres especiais.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.

* **Referência de vínculo de documento** - Essa opção permite associar um campo Formulário adaptável ao campo Documento de registro. Quando o usuário insere qualquer valor em um campo vinculado de um Formulário adaptável, esse valor também aparece no campo vinculado do Documento de registro correspondente. Por exemplo, uma referência de vínculo Documento de registro pode ser usada para exibir o nome e o endereço de um cliente em um Documento de registro, com base na ID do cliente inserida no formulário. Dessa forma, o AEM Forms permite gerar o Documento de registro e oferece uma experiência do usuário contínua para coletar e gerenciar dados.

* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente** - Selecione a opção para desativar o componente. O componente desativado não é ativo ou editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Somente leitura** - Selecione a opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Conteúdo da Ajuda {#help-content}

![Guia Conteúdo da Ajuda](/help/adaptive-forms/assets/button_helptab.png)

* **Descrição curta** - Uma breve descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative o **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta** - Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda** - O texto da Ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto da Ajuda fornece informações mais detalhadas do que o rótulo de um campo de formulário ou o texto de espaço reservado, e foi projetado para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/button_accessibilitytab.png)


No **Acessibilidade** , os valores são definidos para [Acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) rótulos do componente. Várias opções estão disponíveis para usar o texto para leitor de tela:

* **Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias assistivas, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.


   * **Texto personalizado**: Selecione essa opção para usar o texto personalizado para rótulos de acessibilidade ARIA. Selecionar essa opção exibe a caixa de diálogo Texto personalizado . Você pode adicionar informações relevantes na caixa de diálogo Texto personalizado.
   * **Descrição**: Selecione essa opção para usar a descrição para rótulos de acessibilidade ARIA.
   * **Título**: Selecione essa opção para usar o título para rótulos de acessibilidade ARIA.
   * **Nome**: Selecione essa opção para usar o nome para rótulos de acessibilidade ARIA.
   * **Nenhum**: Selecione essa opção se não quiser adicionar rótulos de acessibilidade ARIA.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente de botão.

### Guia Estilos {#styles-tab}

O Componente principal do botão adaptável do Forms é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal do botão adaptável do Forms.

**Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

