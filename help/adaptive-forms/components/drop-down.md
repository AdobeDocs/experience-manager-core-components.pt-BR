---
title: Componente principal adaptável do Forms - Lista suspensa
description: Uso ou personalização do Componente principal suspenso do Adaptive Forms.
role: Architect, Developer, Admin, User
source-git-commit: 1e6460d318f4f9a5dfdcbb81723da01b51b72f3f
workflow-type: tm+mt
source-wordcount: '1673'
ht-degree: 1%

---


# Lista suspensa {#drop-down-list-adaptive-forms-core-component}

Uma lista suspensa em um formulário adaptável permite que os usuários selecionem uma ou mais opções de uma lista de opções predefinidas. As opções podem ser do tipo String, Number ou Boolean. Além disso, o componente de lista suspensa pode ser configurado para ter validação e valores padrão diferentes.

**Exemplo**
![](/help/adaptive-forms/assets/drop-down-list.png)

## Uso {#reasons-to-use-drop-down-list}

Há vários motivos pelos quais é benéfico incluir uma lista suspensa em um Formulário adaptável, incluindo:

* **Lista longa de opções**: Listas suspensas são úteis para situações em que há uma lista longa de opções disponíveis para um campo. Eles ocupam menos espaço no formulário do que uma lista de botões de opção ou caixas de seleção e podem ser menos sobrecarregados para os usuários.

* **Consistência**: As listas suspensas fornecem consistência no design e no layout do formulário, tornando mais intuitivo e fácil para os usuários navegarem.

* **Clareza**: Listas suspensas podem tornar o formulário mais claro e fácil de entender, fornecendo uma lista clara e concisa de opções.

* **Experiência do usuário**: Listas suspensas podem ser usadas para tornar o formulário mais simples, fornecendo uma maneira clara e intuitiva para os usuários selecionarem opções.

* **Análise de dados**: Listas suspensas podem ser usadas para coletar dados de várias fontes e analisá-los, ou usá-los como entrada para processamento adicional.


**Caixa de diálogo Propriedades**

![](/help/adaptive-forms/assets/drop-down-list-properties.png)

Neste exemplo, o elemento Options é usado para definir os itens da lista. O **Exibir texto** é usado para fornecer um rótulo para itens de lista e **Valor dos dados** é usada para especificar o valor que é enviado para o servidor quando o formulário é enviado.

Cada opção da lista suspensa tem um valor de Dados exclusivo e um atributo Exibir texto . Se um usuário selecionar a opção &quot;Vermelho&quot;, o Valor de dados correspondente será enviado para o servidor quando o formulário for enviado. Esses dados podem ser processados por um script do lado do servidor para determinar quais opções foram selecionadas pelo usuário e podem ser usadas para executar várias ações, como atualizar outros campos no formulário ou enviar os dados do formulário para um script do lado do servidor para processamento adicional.

Além disso, a lista suspensa pode ser configurada para ter valores de processamento diferentes para cada opção, e isso pode ser definido usando o Editor de regras adaptável do Forms.

## Versão e compatibilidade {#version-and-compatibility}

A lista suspensa Adaptável Forms Componente principal foi lançada em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta é uma tabela que mostra todas as versões compatíveis, compatibilidade de AEM e links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível  com<br>[versão 2.0.4](/help/versions.md) e posterior | Compatível | Compatível |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal da lista suspensa Adaptive Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/dropdown/v1/dropdown). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de lista suspensa para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de lista suspensa com facilidade para uma experiência do usuário contínua.

![Guia Básica](/help/adaptive-forms/assets/dropdown_basictab.png)

* **Nome** - É possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não deve conter espaços ou caracteres especiais.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Ocultar Título** - Selecione a opção para ocultar o Título do componente.

* **Permitir seleção múltipla** - Selecione essa opção para selecionar várias opções em uma lista suspensa.

* **Salvar valor como** - Essa opção especifica o tipo de dados do valor enviado quando qualquer opção é selecionada. Se a variável **Salvar valor como** está definida como `Number` e adicionar dados da sequência de caracteres ao **Valor dos dados** &#x200B; &#x200B; no **Opções** , a tela exibe uma `Value type mismatch` mensagem de erro.

   No **Opções** , é possível adicionar valores de dados e exibir pares de texto usando o **Adicionar** botão. Depois que uma nova opção é adicionada, as seguintes ações são executadas:

   * **Valor dos dados** - Essa opção permite inserir o conteúdo a ser enviado quando uma opção for selecionada.
   * **Exibir texto** - Essa opção permite inserir o conteúdo a ser exibido em um formulário adaptável.
   * **Excluir** - Toque ou clique em para excluir a opção de um menu suspenso .
   * **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem da opção de um menu suspenso.

* **Opções padrão** - Essa opção permite adicionar valores padrão. Use o ícone excluir para remover a opção adicionada. Se a variável **Salvar valor como** está definida como `Number` e adicionar dados da sequência de caracteres ao **Opções padrão**, a tela exibe uma `Value type mismatch` mensagem de erro.

* **Texto de espaço reservado** - O texto do espaço reservado em um componente de formulário refere-se a um rótulo curto ou prompt que aparece em um campo de entrada como uma dica para o usuário sobre que tipo de informação deve ser inserida nesse campo. O texto do espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não atua como um rótulo ou valor permanente para o campo.

* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.

* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente** - Selecione a opção para desativar o componente. O componente desativado não é ativo ou editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Somente leitura** - Selecione a opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/dropdown_validationtab.png)

* **Obrigatório** - Selecione essa opção se desejar exibir o componente em um formulário adaptável. Não é possível selecionar a variável **Ocultar componente** ou **Desativar Componente**  no **Básico** quando essa opção estiver selecionada.

* **Mensagem de erro** - Essa opção permite que você insira uma mensagem que é exibida se a variável **Obrigatório** está marcada e o campo do formulário fica em branco.

* **Mensagem de validação de script** - Essa opção permite que você insira uma mensagem a ser exibida se a validação do script falhar.

### Guia Conteúdo da Ajuda {#help-content-tab}

![Guia Conteúdo da Ajuda](/help/adaptive-forms/assets/dropdown_helptab.png)

* **Descrição curta** - Uma breve descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative o **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta** - Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda** - O texto da Ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto da Ajuda fornece informações mais detalhadas do que o rótulo de um campo de formulário ou o texto de espaço reservado, e foi projetado para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/dropdown_accessibilitytab.png)

* **Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias assistivas, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente Lista suspensa .


### Guia Estilos {#styles-tab}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para um componente. A lista suspensa Adaptável Forms Componente principal suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para a lista suspensa Componente principal do Adaptive Forms.

**Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.


