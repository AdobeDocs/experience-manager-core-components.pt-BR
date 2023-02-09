---
title: Componente principal adaptável do Forms - Entrada de telefone
description: Uso ou personalização do Componente principal de entrada Adaptive Forms Telephone.
role: Architect, Developer, Admin, User
source-git-commit: 0e4fb8454b7ef84eb5b1b73b01c982a2f9c12381
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 1%

---


# Entrada de telefone {#telephone-input-adaptive-forms-core-component}

O Componente principal de entrada do telefone do formulário adaptável permite que os usuários insiram um número de telefone. O campo de entrada de telefone exibe teclados em dispositivos móveis que são relevantes para números de telefone. Ele pode ser personalizado com atributos adicionais, como &quot;padrão&quot; e &quot;espaço reservado&quot; para especificar o formato e a descrição do número de telefone.

O campo de entrada do telefone é usado normalmente em formulários de contato, formulários de registro e outros formulários, onde um número de telefone é necessário como meio de contato. O campo de entrada do telefone também pode ser usado para garantir que o usuário insira um número de telefone válido, pois o navegador pode impor determinadas restrições, como o comprimento e o formato do número de telefone, com base no atributo &quot;padrão&quot;.

## Uso {#reasons-to-use-telephone-input}

Os motivos comuns para usar um campo de entrada de telefone em um Formulário adaptável são:

* **Informações de contato**: Normalmente, um campo de entrada de telefone é usado para coletar o número de telefone de um usuário como meio de contato.

* **Precisão dos dados aprimorada**: Usando um campo de entrada de telefone, o formulário pode impor determinadas restrições no formato do número de telefone, o que pode ajudar a garantir que os dados inseridos sejam precisos e completos.

* **Melhor experiência do usuário**: Um campo de entrada de telefone fornece uma maneira clara e intuitiva para os usuários inserirem seus números de telefone e podem melhorar a experiência do usuário, permitindo que os usuários insiram suas informações de contato de forma rápida e fácil.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal de entrada Adaptive Forms Telephone foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta é uma tabela que mostra todas as versões suportadas, a compatibilidade AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível  com<br>[versão 2.0.4](/help/versions.md) e posterior | Compatível | Compatível |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de entrada Adaptive Forms Telephone na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/telephoneinput/v1/telephoneinput). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de entrada de telefone para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de entrada de telefone com facilidade para uma experiência do usuário contínua.

![Guia básica](/help/adaptive-forms/assets/telephoneinput_basictab.png)

* **Nome** - É possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não deve conter espaços ou caracteres especiais.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.
* **Ocultar Título** - Selecione a opção para ocultar o Título do componente.

* **Texto de espaço reservado** - O texto do espaço reservado em um componente de formulário refere-se a um rótulo curto ou prompt que aparece em um campo de entrada como uma dica para o usuário sobre que tipo de informação deve ser inserida nesse campo. O texto do espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não atua como um rótulo ou valor permanente para o campo.
* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.
* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente** - Selecione a opção para desativar o componente. O componente desativado não é ativo ou editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Somente leitura** - Selecione a opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Valor padrão** - Essa opção permite adicionar um valor padrão em um campo de formulário. If **Componente desativado** ou **Componente somente leitura** for selecionado, o valor padrão será exibido na tela . Se nenhum valor for inserido pelo usuário no campo de formulário, esse valor será enviado no momento do envio do formulário

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/telephoneinput_validationtab.png)

* **Obrigatório** - Selecione essa opção se desejar exibir o componente em um formulário adaptável. Não é possível selecionar a variável **Ocultar componente** ou **Desativar Componente**  no **Básico** quando essa opção estiver selecionada.

* **Mensagem de erro** - Essa opção permite que você insira uma mensagem que é exibida se a variável **Obrigatório** está marcada e o campo fica em branco.

* **Mensagem de validação de script** - Essa opção permite que você insira uma mensagem a ser exibida se a validação do script falhar.

* **Número máximo de caracteres** - Essa opção permite especificar o número máximo de caracteres permitidos no componente. Se você digitar caracteres maiores que o valor especificado em **Número máximo de caracteres**, uma mensagem de erro é exibida na tela . O **Mensagem de erro de máximo de caracteres** caixa de diálogo permite adicionar uma mensagem de erro personalizada.

* **Mensagem de erro de máximo de caracteres** - O **Mensagem de erro de máximo de caracteres** caixa de diálogo permite adicionar uma mensagem de erro personalizada se você digitar caracteres maiores que o valor especificado na **Número máximo de caracteres** opção.

* **Número mínimo de caracteres** - Essa opção permite especificar o número mínimo de caracteres permitidos no campo. Se você digitar caracteres menores que o valor especificado em **Número mínimo de caracteres**, uma mensagem de erro é exibida na tela . O **Mensagem de erro de caracteres mínimos** caixa de diálogo permite adicionar uma mensagem de erro personalizada.

* **Mensagem de erro de caracteres mínimos** - O **Mensagem de erro de caracteres mínimos** caixa de diálogo permite adicionar uma mensagem de erro personalizada se você digitar caracteres menores que o valor especificado na **Número mínimo de caracteres** opção.

O **Padrão de validação** permite inserir um padrão para validar o número de telefone inserido. O número de telefone inserido é validado em relação ao valor inserido no **Padrão** opção. Caso o número de telefone não seja validado com o valor inserido em **Padrão** , a mensagem de erro será exibida na tela.
* **Padrão** - Essa opção permite que você insira os padrões de verificação permitidos para o número de telefone. Expressões regulares também são permitidas.
* **Mensagem de erro** - Esta opção permite que você insira uma mensagem que é exibida na tela se o número de telefone inserido não conseguir validar com o valor inserido no **Padrão** opção

### Guia Conteúdo da Ajuda {#help-content-tab}

![Guia Conteúdo da Ajuda](/help/adaptive-forms/assets/telephoneinput_helptab.png)

* **Descrição curta** - Uma breve descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative o **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta** - Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda** - O texto da Ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto da Ajuda fornece informações mais detalhadas do que o rótulo de um campo de formulário ou o texto de espaço reservado, e foi projetado para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/telephoneinput_accessibilitytab.png)

* **Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias assistivas, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.


## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente de entrada Telephone.

### Guia Estilos {#styles-tab}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para um componente. O Componente principal de entrada Adaptive Forms Telephone suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal de entrada Adaptive Forms Telephone.

**Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Guia Formatos {#format-tab}

A guia Formatos permite especificar formatos de número padrão e personalizados.