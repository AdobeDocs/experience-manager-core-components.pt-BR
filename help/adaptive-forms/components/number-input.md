---
title: Componente principal adaptável do Forms - Entrada de número
description: Uso ou personalização do Componente principal de entrada do Número do Forms adaptativo.
role: Architect, Developer, Admin, User
exl-id: 75604ecf-1ec5-4e97-b934-d6ed49726147
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 1%

---

# Entrada de número {#number-input-adaptive-forms-core-component}

Um componente Entrada de número em um formulário adaptável é um tipo de campo de formulário que permite que os usuários insiram valores numéricos. Normalmente, o componente é representado por um campo de texto com uma seta para cima e para baixo para aumentar e diminuir o número.

Também pode ser usado com atributos como mín., máx., etapa, valor e muito mais. Esses atributos podem ser usados para definir os valores mínimo e máximo permitidos no campo, o intervalo de etapas para aumentar ou diminuir o número e o valor padrão do campo.

Esse componente pode ser usado para coletar dados numéricos, como idade, quantidade e muito mais. Também pode ser usado para executar operações matemáticas como adição e subtração. Esse componente também pode ser usado para validar os dados numéricos inseridos pelo usuário.

Para acessibilidade, é importante especificar o &quot;rótulo&quot; que descreve a finalidade do campo de entrada do número e o tipo de entrada esperado.

**Exemplo**

![](/help/adaptive-forms/assets/numeric-stepper.png)

## Uso {#reasons-to-use-number-input-numeric-stepper}

Há vários motivos pelos quais é benéfico incluir um componente de entrada numérica em um Formulário adaptável, incluindo:

* **Operações matemáticas**: Campos numéricos podem ser usados para executar operações matemáticas, como adição, subtração, multiplicação e divisão.

* **Intervalo de dados**: Campos numéricos podem ser usados para definir um intervalo de valores válidos usando atributos mín., máx. e etapa.

* **Conteúdo dinâmico**: O componente numérico pode ser usado para exibir dados dinâmicos com base nos campos do formulário.


## Versão e compatibilidade {#version-and-compatibility}

O Componente principal Adaptive Forms Accordion foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, AEM compatibilidade e links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com<br>[versão 2.0.4](/help/adaptive-forms/version.md) e posterior | Compatível com<br>[versão 1.1.12](/help/adaptive-forms/version.md) e posterior, mas inferior a 2.0.0. |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/adaptive-forms/version.md) documento.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de entrada do número de Forms adaptável na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/numberinput/v1/numberinput). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de entrada de números para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de entrada de número com facilidade para uma experiência do usuário contínua.

### Guia básica {#basic-tab}

![Guia básica](/help/adaptive-forms/assets/numberinput_basictab.png)

* **Nome** - É possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não deve conter espaços ou caracteres especiais.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Ocultar Título** - Selecione a opção para ocultar o Título do componente.

* **Texto de espaço reservado** - O texto do espaço reservado em um componente de formulário refere-se a um rótulo curto ou prompt que aparece em um campo de entrada como uma dica para o usuário sobre que tipo de informação deve ser inserida nesse campo. O texto do espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não atua como um rótulo ou valor permanente para o campo.
* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.
* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente** - Selecione a opção para desativar o componente. O componente desativado não é ativo ou editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Somente leitura** - Selecione a opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Tipo de número** - Essa opção permite selecionar o tipo de valores numéricos &#x200B; &#x200B; permitidos no campo de formulário. Você pode selecionar os tipos Decimal ou Integer no menu suspenso.
* **Valor padrão** - Essa opção permite adicionar um valor padrão em um campo de formulário. If **Componente desativado** ou **Componente somente leitura** for selecionado, o valor padrão será exibido na tela . Se nenhum valor for inserido pelo usuário no campo de formulário, esse valor será enviado no momento do envio do formulário

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/numberinput_validationtab.png)

* **Obrigatório** - Selecione essa opção se desejar exibir o componente em um formulário adaptável. Não é possível selecionar a variável **Ocultar componente** ou **Desativar Componente**  no **Básico** quando essa opção estiver selecionada.

* **Mensagem de erro** - Essa opção permite que você insira uma mensagem que é exibida se a variável **Obrigatório** está marcada e o campo fica em branco.

* **Mensagem de validação de script** - Essa opção permite que você insira uma mensagem a ser exibida se a validação do script falhar.

* **Número mais baixo / Menor número** - Use essa opção para selecionar o número mínimo permitido a ser inserido no campo de formulário. Se o valor for menor que o número especificado em **Número mais baixo / Menor número** for inserida no campo de formulário, a mensagem de erro será exibida.

* **Mensagem de erro mínima** - Essa opção permite inserir uma mensagem de erro que é exibida quando o usuário insere um valor menor que o especificado na **Número Mínimo/Número Mínimo** opção.

* **Excluir valor mínimo** - Marque essa caixa de seleção se não quiser que o valor mínimo especificado na variável **Número mais baixo / Menor número** opção a ser incluída no intervalo de valores &#x200B; para inserir no campo de formulário.

* **Número mais alto/Maior número** - Use essa opção para selecionar o número máximo permitido a ser inserido no campo de formulário. Se o número for maior que o número especificado em **Número mais alto/Maior número** for inserida no campo de formulário, a mensagem de erro será exibida.

* **Mensagem de erro máxima** - Essa opção permite inserir uma mensagem de erro que é exibida quando o usuário insere um valor maior que o especificado na **Número mais alto/Maior número** opção.

* **Excluir valor máximo** - Marque essa caixa de seleção se não quiser que o valor máximo especificado na variável **Número mais alto/Maior número** opção a ser incluída no intervalo de valores a serem inseridos no campo do formulário.

### Guia Conteúdo da Ajuda {#help-content}

![Guia Conteúdo da Ajuda](/help/adaptive-forms/assets/numberinput_helptab.png)

* **Descrição curta** - Uma breve descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative o **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta** - Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda** - O texto da Ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto da Ajuda fornece informações mais detalhadas do que o rótulo de um campo de formulário ou o texto de espaço reservado, e foi projetado para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/numberinput_accessibility.png)

**Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que deve ser lido por tecnologias de assistência, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

### Guia Formatos {#formats-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/numberinput_formattab.png)

* **Exibir formato** - Essa opção permite selecionar opções de diferentes tipos numéricos para exibição. Quando o usuário seleciona qualquer opção do **Tipo** menu suspenso, o **Formato** se torna visível no painel. Você pode escolher um formato específico no qual os números são exibidos para o usuário.

* **Número de dígitos antes do separador decimal (1234.000)** - Use essa opção para especificar o número de dígitos que serão exibidos antes do ponto decimal.

* **Número de dígitos após o separador decimal (1234.000)** - Use essa opção para especificar o número de dígitos que serão exibidos após o ponto decimal.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente de entrada Number.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar estilos de CSS de um componente. O Componente principal de entrada Número adaptável do Forms é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Styletab](/help/adaptive-forms/assets/datepicker_styletab.png)

**Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal de entrada do Número do Forms adaptável.

**Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no Adaptive Forms . Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o editor, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Guia Formatos {#format-tab}

A guia Formatos permite especificar formatos de número padrão e personalizados.
![Guia Design](/help/adaptive-forms/assets/emailinput_designformattab.png)

