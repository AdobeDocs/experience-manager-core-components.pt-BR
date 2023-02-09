---
title: Componente principal adaptável do Forms - Grupo de caixas de seleção
description: Uso ou personalização do Componente principal do grupo da caixa de seleção adaptável do Forms.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 2%

---


# Grupos de caixa de seleção {#button-component-adaptive-forms-core-component}

Um grupo de caixas de seleção em um formulário adaptável é um conjunto de caixas de seleção relacionadas que permitem aos usuários selecionar uma ou mais opções de uma lista. Cada caixa de seleção é representada por um Valor de dados (valor usado para processar itens de um grupo de caixas de seleção) e Valor de exibição (rótulo para cada item de caixa de seleção que descreve sua finalidade)

**Exemplo**

![](/help/adaptive-forms/assets/checkbox-group.png)

**Caixa de diálogo Propriedades**

![](/help/adaptive-forms/assets/checkbox-group-properties.png)

Neste exemplo, o elemento Options é usado para agrupar as caixas de seleção. O **Exibir texto** é usado para fornecer um rótulo para um item e **Valor dos dados** é usada para especificar o valor que é enviado para o servidor quando o formulário é enviado.

Cada opção/item de caixa de seleção tem um valor de Dados exclusivo e um atributo Texto de exibição . Se um usuário marcar as caixas de seleção &quot;Filho&quot; e &quot;Filho&quot;, o Valor de Dados correspondente será enviado para o servidor quando o formulário for enviado. Esses dados podem ser processados por um script do lado do servidor para determinar quais opções foram selecionadas pelo usuário e podem ser usadas para executar várias ações, como atualizar outros campos no formulário ou enviar os dados do formulário para um script do lado do servidor para processamento adicional.

Além disso, o grupo de caixas de seleção pode ser configurado para ter valores de processamento diferentes para cada opção, e isso pode ser definido usando o Editor de regras adaptável do Forms.

## Uso {#reasons-to-use-check-box-group}

Há vários motivos pelos quais é benéfico incluir um grupo de caixas de seleção em um formulário adaptável, incluindo:

* **Várias seleções**: Um grupo de caixas de seleção permite que os usuários selecionem várias opções de uma lista, o que pode ser útil em situações em que várias seleções são permitidas ou obrigatórias.

* **Experiência do usuário**: O grupo de caixa de seleção pode ser usado para tornar o formulário mais simples, fornecendo uma maneira clara e intuitiva para os usuários selecionarem várias opções.

* **Análise de dados**: O grupo de caixa de seleção pode ser usado para coletar dados de várias fontes e analisá-los, ou usá-los como entrada para processamento adicional.

* **Pesquisas**: O grupo de caixa de seleção pode ser usado em pesquisas para selecionar várias opções para uma pergunta.

* **Preferências do usuário**: O grupo de caixa de seleção pode ser usado para coletar as preferências do usuário para opções diferentes.

* **Valor dos dados**: O grupo de caixa de seleção também pode ser usado para processar itens de um grupo de caixa de seleção.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal do grupo da caixa de seleção adaptável do Forms foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta é uma tabela que mostra todas as versões suportadas, AEM compatibilidade e links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível  com<br>[versão 2.0.4](/help/versions.md) e posterior | Compatível | Compatível |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do grupo de caixas de seleção adaptáveis do Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de caixa de seleção para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de caixa de seleção com facilidade para uma experiência do usuário contínua.


### Guia básica {#basic-tab}

![Guia Básica](/help/adaptive-forms/assets/checkbox_basictab.png)

* **Nome** - O nome identifica exclusivamente o componente no editor de regras.Caracteres e espaços especiais não são permitidos nas sequências de nome.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Ocultar Título** - Selecione a opção para ocultar o Título do componente.

* **Opções** - Você pode adicionar valores de dados e exibir pares de texto usando o **Adicionar** botão. Depois que uma nova opção é adicionada, as seguintes ações podem ser executadas:

   * **Valor dos dados** - Essa opção permite inserir o conteúdo a ser enviado quando uma opção for selecionada.
   * **Exibir texto** - Essa opção permite inserir o conteúdo a ser exibido em um formulário adaptável.
   * **Excluir** - Toque ou clique para excluir a opção de uma caixa de seleção .
   * **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem dos painéis.

* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.

* **Tipo de dados do valor enviado** - Essa opção especifica o tipo de dados do valor enviado quando qualquer opção é selecionada. Se a variável **tipo de dados do valor enviado** está definida como `Number` e adicionar dados da sequência de caracteres ao **Valor dos dados** &#x200B; &#x200B; no **Opções** , a tela exibe uma `Value type mismatch` mensagem de erro.

* **Opções de exibição** - Essa opção é usada para definir o alinhamento visual das caixas de seleção em um formulário adaptável. As duas opções compatíveis são:
   * **Horizontal** - Quando essa opção é selecionada, as caixas de seleção são exibidas da esquerda para a direita em um formulário adaptável.
   * **Vertical** - Quando essa opção é selecionada, as caixas de seleção são exibidas de cima para baixo em um formulário adaptável.

* **Opções padrão** - Essa opção permite que você adicione valores padrão pré-selecionados quando o formulário for carregado. Use o ícone excluir para remover as opções adicionadas. Se a variável **tipo de dados do valor enviado** está definida como `Number` e adicionar dados da sequência de caracteres ao **Opções padrão**, a tela exibe uma `Value type mismatch` mensagem de erro.
* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente** - Selecione a opção para desativar o componente. O componente desativado não é ativo ou editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Somente leitura** - Selecione a opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/checkbox_validationtab.png)

* **Obrigatório** - Selecione essa opção se desejar exibir o componente em um formulário adaptável. Não é possível selecionar a variável **Ocultar componente** ou **Desativar Componente**  no **Básico** quando essa opção estiver selecionada.

* **Mensagem de erro** - Essa opção permite que você insira uma mensagem que é exibida se a variável **Obrigatório** está marcada e o campo do formulário fica em branco.

* **Mensagem de validação de script** - Essa opção permite que você insira uma mensagem a ser exibida se a validação do script falhar.

### Guia Conteúdo da Ajuda {#helpcontent-tab}

![Guia Conteúdo da Ajuda](/help/adaptive-forms/assets/checkbox_helptab.png)

* **Descrição curta** - Uma breve descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative o **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta** - Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda** - O texto da Ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto da Ajuda fornece informações mais detalhadas do que o rótulo de um campo de formulário ou o texto de espaço reservado, e foi projetado para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/checkbox_accessibility.png)

No **Acessibilidade** , os valores são definidos para [Acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) rótulos do componente. Várias opções estão disponíveis para usar o texto para leitor de tela:

* **Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias assistivas, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

   * **Texto personalizado**: Selecione essa opção para usar o texto personalizado para rótulos de acessibilidade ARIA. Selecionar essa opção exibe a caixa de diálogo Texto personalizado . Você pode adicionar informações relevantes na caixa de diálogo Texto personalizado.

   * **Título**: Selecione essa opção para usar o título para rótulos de acessibilidade ARIA.


## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente Grupo de caixa de seleção.

### Guia Estilos {#styles-tab}

O Componente principal do grupo da caixa de seleção adaptável do Forms é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal do grupo de caixas de seleção adaptável do Forms.

**Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

