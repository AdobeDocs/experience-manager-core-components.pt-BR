---
title: Componente principal adaptável do Forms - botão Redefinir
description: Uso ou personalização do Componente principal do botão Adaptive Forms Reset .
role: Architect, Developer, Admin, User
exl-id: e5aa9d89-aece-491e-80a1-7fb9ea6c4b60
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1194'
ht-degree: 2%

---

# Redefinir {#reset-button}

Um botão de redefinição em um formulário adaptável é um botão que permite que os usuários limpem ou redefinam todos os campos do formulário para seus valores padrão. Quando o botão reset é clicado, os dados inseridos nos campos do formulário são excluídos e os campos retornam ao seu estado original. O botão de redefinição é normalmente usado como uma alternativa ao botão Enviar e fornece uma maneira de os usuários recomeçarem se inserirem dados incorretos ou indesejados no formulário.


## Uso {#reasons-to-use-reset-button}

Os motivos para usar um botão de redefinição em um formulário adaptável são:

* **Conveniência do usuário**: Um botão de redefinição fornece uma maneira rápida e fácil para os usuários limparem o formulário e recomeçarem, sem precisar excluir manualmente cada campo.

* **Maior usabilidade**: Um botão de redefinição pode melhorar a experiência do usuário, permitindo que os usuários corrijam erros ou alterem suas entradas facilmente.

* **Prevenção de erros**: Ao usar um botão de redefinição, os usuários podem evitar o envio acidental de dados incorretos, o que pode levar a erros ou problemas de processamento.

* **Consistência**: A inclusão de um botão de redefinição em um formulário oferece consistência na experiência do usuário, já que os botões de redefinição são um recurso comum dos formulários.

* **Melhor gerenciamento de dados**: Ao usar um botão de redefinição, os dados do formulário podem ser mantidos organizados e precisos, pois os usuários têm menos probabilidade de enviar dados inconsistentes ou incorretos.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal Adaptive Forms Accordion foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, AEM compatibilidade e links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com<br>[versão 2.0.4](/help/adaptive-forms/version.md) e posterior | Compatível com<br>[versão 1.1.12](/help/adaptive-forms/version.md) e posterior, mas inferior a 2.0.0. |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/adaptive-forms/version.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do botão Redefinição do Forms Adaptive na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de botão Redefinir para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de botão Redefinir com facilidade para uma experiência do usuário contínua.

### Guia básica {#basic-tab}

![Guia básica](/help/adaptive-forms/assets/button_basictab.png)

* **Nome** - É possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não deve conter espaços ou caracteres especiais.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.

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


**Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias assistivas, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente do botão Redefinir.


### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar estilos de CSS de um componente. O Componente principal do botão Adaptive Forms Reset suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Caixa de diálogo de design](/help/adaptive-forms/assets/reset_designdialog.png)

* **Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal do botão de redefinição adaptável do Forms.

* **Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.
