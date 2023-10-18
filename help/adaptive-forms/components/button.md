---
title: 'Componente principal de Formulários adaptáveis: Botão'
description: Uso ou personalização do Componente principal de Botão de Formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: cb75929b-8c86-49d1-b51a-368f5b80b1a9
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '1479'
ht-degree: 100%

---

# Componente de Botão  {#button-component-adaptive-forms-core-component}

Um botão em um Formulário adaptável é um elemento de interface que permite aos usuários iniciar uma ação quando clicados. O elemento de botão pode ser usado para enviar um formulário, redefinir um formulário ou executar outras ações, como navegar para uma página diferente ou acionar um código personalizado. O botão pode ser criado usando o Componente principal de Botão.

O Editor de regras de Formulários adaptáveis permite que os usuários definam várias ações para o componente de Botão. Essas ações incluem abrir um site, mostrar ou ocultar componentes do formulário, adicionar uma instância de um painel ou de um componente, enviar ou redefinir um formulário e muito mais.

Componentes separados do recurso Formulários adaptáveis para o [Botão Enviar](/help/adaptive-forms/components/submit-button.md) e o [Botão Redefinir](/help/adaptive-forms/components/reset-button.md), permitindo que os usuários enviem ou redefinam um formulário de maneira conveniente. O componente Botão pode ser configurado de forma flexível para executar essas ações com base em necessidades específicas.

Os usuários podem acessar a lista completa de ações compatíveis com o componente de botão usando o Editor de regras de Formulários adaptáveis. O Editor de regras permite que os usuários criem regras acionadas por diversos eventos, como quando um botão é clicado, um formulário é carregado ou um valor de campo é alterado. Essas regras podem ser usadas para executar diversas ações, como mostrar ou ocultar componentes, definir valores de campo ou enviar o formulário.

## Uso {#reasons-to-use-button}

Há vários motivos pelos quais é benéfico incluir um botão em um Formulário adaptável, incluindo:

* **Envio do formulário**: normalmente, um botão é usado para enviar um formulário, permitindo que os usuários enviem os dados inseridos ao servidor para processamento.

* **Redefinição de formulário**: os botões também podem ser usados para redefinir um formulário, limpando todos os dados inseridos.

* **Navegação**: os botões podem ser usados para navegar entre diferentes seções de um formulário ou páginas em um site.

* **Manipulação de eventos**: os botões podem ser usados para acionar eventos diferentes, como abrir um site, mostrar/ocultar componentes, adicionar uma instância de um painel ou componente ao botão.

* **Interatividade**: os botões podem ser usados para criar formulários interativos. Por exemplo, um botão pode ser usado para abrir uma caixa de diálogo modal ou para alternar uma seção do formulário.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de Botão de Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Para mais informações sobre o desenvolvimento dos Componentes principais, consulte a [Documentação do desenvolvedor dos componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de botão para visitantes com a caixa de diálogo Configurar. Você também pode definir propriedades de botão com facilidade para uma experiência do usuário perfeita.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/button_basictab.png)

* **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

* **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

* **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

* **Referência de vínculo de documento de registro**: essa opção permite associar um campo de formulário adaptável ao campo de documento de registro. Quando o usuário insere qualquer valor em um campo vinculado de um formulário adaptável, esse valor também aparece no campo vinculado do documento de registro correspondente. Por exemplo, uma referência de vínculo de um documento de registro pode ser usada para exibir o nome e o endereço de um cliente em um documento de registro com base na ID do cliente inserida no formulário. Dessa forma, o AEM Forms permite gerar um Documento de registro e oferece uma experiência do usuário perfeita para coletar e gerenciar dados.

* **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Conteúdo de ajuda {#help-content}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/button_helptab.png)

* **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

* **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/button_accessibilitytab.png)


* **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A Caixa de diálogo de Design é usada para definir e gerenciar estilos CSS para o componente de botão.

### Guia Estilos {#styles-tab}

O Componente principal de botão de Formulários adaptáveis é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design](/help/adaptive-forms/assets/button_designdialog.png)

* **Classes CSS Padrão**: você pode fornecer uma classe CSS padrão para o Componente principal de botão de Formulários adaptáveis.

* **Estilos permitidos**: você pode definir um estilo fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

## Artigo relacionado {#related-article}

* [Criar um formulário adaptável em uma página do AEM Sites ou fragmento de experiência](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=pt-BR)

* [Criar um formulário adaptável independente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=pt-BR)

>[!MORELIKETHIS]
>
>* [Acordeão](/help/adaptive-forms/components/accordion.md)
>* [Grupo de Caixa de seleção](/help/adaptive-forms/components/checkbox-group.md)
>* [Seletor de data](/help/adaptive-forms/components/date-picker.md)
>* [Lista suspensa](/help/adaptive-forms/components/drop-down.md)
>* [Entrada de email](/help/adaptive-forms/components/email-input.md)
>* [Container de formulário](/help/adaptive-forms/components/form-container.md)
>* [Anexo de arquivo](/help/adaptive-forms/components/file-attachment.md)
>* [Rodapé](/help/adaptive-forms/components/footer.md)
>* [Cabeçalho](/help/adaptive-forms/components/header.md)
>* [Guias horizontais](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Imagem](/help/adaptive-forms/components/image.md)
>* [Entrada de número](/help/adaptive-forms/components/number-input.md)
>* [Container do painel](/help/adaptive-forms/components/panel-container.md)
>* [Botão de opção](/help/adaptive-forms/components/radio-button.md)
>* [Botão Redefinir](/help/adaptive-forms/components/reset-button.md)
>* [Botão Enviar](/help/adaptive-forms/components/submit-button.md)
>* [Entrada de telefone](/help/adaptive-forms/components/telephone-input.md)
>* [Entrada de texto](/help/adaptive-forms/components/text-input.md)
>* [Texto](/help/adaptive-forms/components/text.md)
>* [Título](/help/adaptive-forms/components/title.md)
>* [Assistente](/help/adaptive-forms/components/wizard.md)


## Consulte também {#see-also}

{{see-also}}

