---
title: Componente principal adaptável do Forms - Entrada de email
description: Uso ou personalização do Componente principal de entrada de email adaptável do Forms.
role: Architect, Developer, Admin, User
exl-id: f6a2974b-991e-4cea-9ef8-0b03e8975eeb
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 1%

---

# Entrada de email {#Email-input-adaptive-forms-core-component}

O Componente principal de entrada de email do formulário adaptável é usado para coletar endereços de email dos usuários. O campo de entrada de email permite que o navegador valide se os dados inseridos são um formato de endereço de email válido. Normalmente, ele é representado como uma caixa de texto e tem validações de padrão para aceitar apenas endereços de email válidos. O campo de entrada de email pode ser personalizado ainda mais com atributos adicionais, como &quot;obrigatório&quot;, &quot;espaço reservado&quot; e &quot;padrão&quot; para definir validações para os dados de entrada.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

Há vários motivos pelos quais é benéfico incluir um componente de entrada de email em um Formulário adaptável, incluindo:

* **Conveniência do usuário**: Uma entrada de email facilita a inserção de endereços de email pelos usuários, pois fornece uma indicação clara dos dados esperados no campo.

* **Comunicação personalizada**: A coleta de endereços de email de usuários por meio de um formulário permite comunicação personalizada, como o envio de emails de confirmação ou informativos.

* **Geração de leads**: Ao coletar endereços de email por meio de um formulário, as empresas podem criar sua lista de email e usá-la para geração de leads.

* **Autenticação do usuário**: Endereços de email podem ser usados como meio de autenticação para acessar conteúdo ou serviços restritos.

* **Coleção de comentários**: Uma entrada de email em um formulário de feedback permite que a empresa se comunique com o usuário para obter acompanhamento ou esclarecimentos sobre seus comentários.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal Adaptive Forms Accordion foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, AEM compatibilidade e links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com<br>[versão 2.0.4](/help/adaptive-forms/version.md) e posterior | Compatível com<br>[versão 1.1.12](/help/adaptive-forms/version.md) e posterior, mas inferior a 2.0.0. |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/adaptive-forms/version.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de entrada de email adaptável do Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de entrada de email para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de entrada de email com facilidade para uma experiência do usuário contínua.

### Guia básica {#basic-tab}

![Guia Básica](/help/adaptive-forms/assets/email_basictab.png)

* **Nome** - O nome identifica exclusivamente o componente no editor de regras.Caracteres e espaços especiais não são permitidos nas sequências de nome.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Ocultar Título** - Selecione a opção para ocultar o Título do componente.

* **Texto de espaço reservado** - O texto do espaço reservado em um componente de formulário refere-se a um rótulo curto ou prompt que aparece em um campo de entrada como uma dica para o usuário sobre que tipo de informação deve ser inserida nesse campo. O texto do espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não atua como um rótulo ou valor permanente para o campo.

* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.
* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente** - Selecione a opção para desativar o componente. O componente desativado não é ativo ou editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Somente leitura** - Selecione a opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

* **Valor padrão** - Essa opção permite adicionar um valor padrão em um campo de formulário. If **Componente desativado** ou **Componente somente leitura** for selecionado, o valor padrão será exibido na tela . Se nenhum valor for inserido pelo usuário no campo de formulário, esse valor será enviado no momento do envio do formulário


### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/email_validationtab.png)

* **Obrigatório** - Selecione essa opção se desejar exibir o componente em um formulário adaptável. Não é possível selecionar a variável **Ocultar componente** ou **Desativar Componente**  no **Básico** quando essa opção estiver selecionada.

* **Mensagem de erro** - Essa opção permite que você insira uma mensagem que é exibida se a variável **Obrigatório** está marcada e o campo do formulário fica em branco.

* **Mensagem de validação de script** - Essa opção permite que você insira uma mensagem a ser exibida se a validação do script falhar.

* **Número máximo de caracteres** - Essa opção permite especificar o número máximo de caracteres permitidos no campo. Se você digitar caracteres maiores que o valor especificado em **Número máximo de caracteres**, uma mensagem de erro é exibida na tela . O **Mensagem de erro de máximo de caracteres** caixa de diálogo permite adicionar uma mensagem de erro personalizada.

* **Mensagem de erro de máximo de caracteres** - O **Mensagem de erro de máximo de caracteres** caixa de diálogo permite adicionar uma mensagem de erro personalizada se você digitar caracteres maiores que o valor especificado na **Número máximo de caracteres** opção.

* **Número mínimo de caracteres** - Essa opção permite especificar o número mínimo de caracteres permitidos no campo. Se você digitar caracteres menores que o valor especificado em **Número mínimo de caracteres**, uma mensagem de erro é exibida na tela . O **Mensagem de erro de caracteres mínimos** caixa de diálogo permite adicionar uma mensagem de erro personalizada.

* **Mensagem de erro de caracteres mínimos** - O **Mensagem de erro de caracteres mínimos** caixa de diálogo permite adicionar uma mensagem de erro personalizada se você digitar caracteres menores que o valor especificado na **Número mínimo de caracteres** opção.

<br>

    A opção **Padrão de validação** permite inserir um padrão para validar a ID de email inserida. Caso a ID de email não seja validada com o valor inserido na opção **Padrão** , a mensagem de erro será exibida na tela.
    * **Padrão** - Essa opção permite inserir os padrões de verificação permitidos para o email. Expressões regulares também são permitidas.
    * **Mensagem de erro** - Essa opção permite inserir uma mensagem que é exibida na tela se a ID do email não for validada com o valor inserido na opção **Padrão**

### Guia Conteúdo da Ajuda {#help-content-tab}

![Guia Conteúdo da Ajuda](/help/adaptive-forms/assets/email_helptab.png)

* **Descrição curta** - Uma breve descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative o **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta** - Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda** - O texto da Ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto da Ajuda fornece informações mais detalhadas do que o rótulo de um campo de formulário ou o texto de espaço reservado, e foi projetado para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/email_accessibilitytab.png)

**Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias assistivas, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente de entrada de Email .

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar estilos de CSS de um componente. O Componente principal de entrada de email adaptável do Forms é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Guia Estilo](/help/adaptive-forms/assets/email_designdialog.png)

* **Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal de entrada de email adaptável do Forms.

* **Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Guia Formatos {#format-tab}

A guia format permite especificar os formatos de data padrão e personalizados.

![Guia Design](/help/adaptive-forms/assets/emailinput_designformattab.png)

