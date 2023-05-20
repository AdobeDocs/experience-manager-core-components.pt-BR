---
title: Componente principal de formulários adaptáveis - Entrada de telefone
description: Uso ou personalização do componente principal de entrada de telefone de formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: d06179ac-04bd-4af4-b6ac-c4c78086058c
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1721'
ht-degree: 100%

---

# Entrada de telefone {#telephone-input-adaptive-forms-core-component}

O componente principal de entrada de telefone de formulários adaptáveis permite que os usuários insiram um número de telefone. O campo de entrada de telefone exibe teclados em dispositivos móveis que são relevantes para números de telefone. Ele pode ser personalizado com atributos adicionais, como um “padrão” e um “espaço reservado”, para especificar o formato e a descrição do número de telefone.

O campo de entrada de telefone é usado normalmente em formulários de contato, de registro e outros formulários nos quais um número de telefone é necessário como meio de contato. O campo de entrada de telefone também pode ser usado para garantir que o usuário insira um número de telefone válido, pois o navegador pode impor determinadas restrições, como o comprimento e o formato do número de telefone, com base no atributo “padrão”.

## Uso {#reasons-to-use-telephone-input}

Os motivos comuns para se usar um campo de entrada de telefone em um formulário adaptável são:

* **Informações de contato**: normalmente, um campo de entrada de telefone é usado para coletar o número de telefone de um usuário como meio de contato.

* **Precisão dos dados aprimorada**: usando um campo de entrada de telefone, o formulário pode impor determinadas restrições no formato do número de telefone, o que pode ajudar a garantir que os dados inseridos sejam precisos e completos.

* **Melhor experiência de usuário**: um campo de entrada de telefone fornece uma maneira clara e intuitiva para os usuários inserirem seus números de telefone, o que pode melhorar a experiência deles, permitindo que insiram suas informações de contato de forma rápida e fácil.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal de entrada de telefone de formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/telephoneinput/v1/telephoneinput). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência de entrada de telefone para visitantes com a caixa de diálogo de configuração. Você também pode definir opções de entrada de telefone com facilidade para uma experiência de usuário perfeita.

![Guia Básico](/help/adaptive-forms/assets/telephoneinput_basictab.png)

* **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

* **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

* **Ocultar título**: selecione essa opção para ocultar o Título do componente.

* **Texto de espaço reservado**: o texto de espaço reservado em um componente de formulário refere-se a um rótulo curto ou exemplo que aparece em um campo de entrada como uma dica para o usuário sobre que tipo de informação deve ser inserida nesse campo. O texto de espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não age como um rótulo ou valor permanente para o campo.

* **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

* **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

* **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

* **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

* **Valor padrão**: essa opção permite adicionar um valor padrão a um campo de formulário. Se o **Componente desativado** ou o **Componente somente leitura** for selecionado, o valor padrão será exibido na tela. Se nenhum valor for inserido pelo usuário no campo de formulário, esse valor será enviado no momento do envio do formulário

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/telephoneinput_validationtab.png)

* **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Não é possível selecionar as opções **Ocultar componente** ou **Desativar Componente** na guia **Básico** quando essa opção está selecionada.

* **Mensagem de erro**: essa opção permite que você insira uma mensagem que será exibida se uma caixa de seleção **Obrigatória** estiver marcada mas o campo ficar em branco.

* **Mensagem de validação de script**: essa opção permite que você insira uma mensagem que será exibida caso haja falha na validação do script.

* **Número máximo de caracteres**: essa opção permite especificar o número máximo de caracteres permitidos no componente. Se você inserir mais caracteres que o valor especificado em **Número máximo de caracteres**, uma mensagem de erro será exibida na tela. A caixa de diálogo **Mensagem de erro de máximo de caracteres** permite adicionar uma mensagem de erro personalizada.

* **Mensagem de erro de máximo de caracteres**: a caixa de diálogo **Mensagem de erro de máximo de caracteres** permite adicionar uma mensagem de erro personalizada que será exibida se você inserir mais caracteres que o valor especificado na opção **Número máximo de caracteres**.

* **Número mínimo de caracteres**: essa opção possibilita especificar o número mínimo de caracteres permitidos no campo. Se você inserir menos caracteres que o valor especificado em **Número mínimo de caracteres**, uma mensagem de erro será exibida na tela. A caixa de diálogo **Mensagem de erro de mínimo de caracteres** permite adicionar uma mensagem de erro personalizada.

* *Mensagem de erro de mínimo de caracteres**: a caixa de diálogo **Mensagem de erro de mínimo de caracteres** permite adicionar uma mensagem de erro personalizada que será exibida se você inserir menos caracteres que o valor especificado na opção **Número mínimo de caracteres**.

A opção **Padrão de validação** permite inserir um padrão para validar o número de telefone inserido. O número de telefone inserido é validado em relação ao valor inserido na opção **Padrão**. Caso o número de telefone não seja validado com o valor inserido na opção **Padrão**, a mensagem de erro será exibida na tela.

* **Padrão**: essa opção permite inserir os padrões de verificação permitidos para o número de telefone. Expressões regulares também são permitidas.

* **Mensagem de erro**: essa opção permite inserir uma mensagem que será exibida na tela se o número de telefone inserido não puder ser validado com relação ao valor inserido na opção **Padrão** 

### Guia Conteúdo de ajuda {#help-content-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/telephoneinput_helptab.png)

* **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

* **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/telephoneinput_accessibilitytab.png)

**Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar estilos CSS para o componente de entrada de telefone.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de Entrada de telefone de formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design](/help/adaptive-forms/assets/telephoneinput_designdialog.png)

* **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o componente principal de entrada de telefone de formulários adaptáveis.

* **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Guia Formatos {#format-tab}

A guia Formatos permite especificar formatos de número padrão e personalizados.

![Guia Formato](/help/adaptive-forms/assets/telephoneinput_format.png)

