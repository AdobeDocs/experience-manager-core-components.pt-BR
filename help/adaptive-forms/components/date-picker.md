---
title: Componente principal adaptável do Forms - Seletor de data
description: Uso ou personalização do Componente principal do seletor de data adaptável do Forms.
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1666'
ht-degree: 1%

---

# Seletor de data {#date-picker-adaptive-forms-core-component}

Um componente do seletor de datas em um formulário adaptável é um elemento da interface do usuário que permite aos usuários selecionar uma data em um calendário ou inserir manualmente uma data em um formato específico. O componente do seletor de datas pode ser configurado para ter formatação, validação e valores padrão diferentes.

**Exemplo**

![](/help/adaptive-forms/assets/date-picker.png)

## Uso {#reasons-to-use-drop-date-picker}

Há vários motivos pelos quais é benéfico incluir um seletor de datas em um formulário adaptável, incluindo:

* **Conveniência**: Um componente seletor de datas permite que os usuários selecionem facilmente uma data de um calendário sem precisar inserir manualmente a data em um campo de texto. Isso pode economizar tempo e reduzir erros.

* **Experiência do usuário**: O componente Seletor de data pode ser usado para tornar o formulário mais simples, fornecendo uma maneira clara e intuitiva para os usuários selecionarem a data.

* **Análise de dados**: O componente seletor de datas pode ser usado para coletar dados de várias fontes e analisá-los, ou usá-los como entrada para processamento adicional.

* **Gerenciamento de eventos**: O componente seletor de datas pode ser usado em sites de gerenciamento de eventos para selecionar a data do evento.

* **Reserva e reservas**: O componente seletor de data pode ser usado em sites de reserva e reserva para selecionar as datas de check-in e check-out.

* **Formato de data**: O componente Seletor de data pode ser usado para corrigir o formato no qual a data é exibida e inserida. Certifique-se de que o formato de data seja consistente em todo o formulário para garantir uma experiência do usuário consistente.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal Adaptive Forms Accordion foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, AEM compatibilidade e links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com<br>[versão 2.0.4](/help/adaptive-forms/version.md) e posterior | Compatível com<br>[versão 1.1.12](/help/adaptive-forms/version.md) e posterior, mas inferior a 2.0.0. |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/adaptive-forms/version.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do seletor de data da Forms adaptável na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de seletor de datas para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de seletor de datas com facilidade para uma experiência do usuário contínua.

### Guia básica {#basic-tab}

![Guia Básica](/help/adaptive-forms/assets/datepicker_basictab.png)

* **Nome** - O nome identifica exclusivamente o componente no editor de regras. Caracteres e espaços especiais não são permitidos nas sequências de nome.

* **Título** - Título é uma string que aparece na parte superior de um componente em um Formulário adaptável. Título identifica exclusivamente o componente na estrutura em árvore de um formulário adaptável. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Ocultar Título** - Selecione essa opção para ocultar o título do tipo de componente em um formulário adaptável.

* **Texto de espaço reservado** - O texto do espaço reservado em um componente de formulário refere-se a um rótulo curto ou prompt que aparece em um campo de entrada como uma dica para o usuário sobre que tipo de informação deve ser inserida nesse campo. O texto do espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não atua como um rótulo ou valor permanente para o campo.

* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente** - Selecione a opção para desativar o componente. O componente desativado não é ativo ou editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Somente leitura** - Selecione a opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Data padrão** - Essa opção permite adicionar uma data ao campo de formulário. A data inserida aparece por padrão no local do componente. Se nenhuma data for inserida pelo usuário, esse valor será enviado no momento do envio do formulário. Em caso **Componente desativado** ou **Componente somente leitura** for selecionada, a data padrão será exibida na tela e enviada no momento do envio do formulário.


### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/datepicker_validation.png)

* **Obrigatório** - Selecione essa opção se desejar exibir o componente em um formulário adaptável. Não é possível selecionar a variável **Ocultar componente** ou **Desativar Componente** no **Básico** quando essa opção estiver selecionada.

* **Mensagem de erro** - Essa opção permite que você insira uma mensagem que é exibida se a variável **Obrigatório** está marcada e o campo do formulário fica em branco.

* **Mensagem de validação de script** - Essa opção permite que você insira uma mensagem a ser exibida se a validação do script falhar.

* **Data mínima** - Essa opção permite inserir a data mínima exigida. Se você inserir uma data anterior à data especificada em Minimum Date (Data mínima), uma mensagem de erro será exibida na tela. O **Mensagem de erro mínima** caixa de diálogo permite adicionar uma mensagem de erro personalizada.

* **Mensagem de erro mínima** - O **Mensagem de erro mínima** caixa de diálogo permite adicionar uma mensagem de erro personalizada a ser exibida, caso insira uma data anterior à especificada no **Data mínima** opção.

* **Data máxima** - Essa opção permite que você insira a data máxima necessária. Se você inserir uma data posterior à data especificada em Data máxima, uma mensagem de erro será exibida na tela. O **Mensagem de erro máxima** caixa de diálogo permite adicionar uma mensagem de erro personalizada.

* **Mensagem de erro máxima** - O **Mensagem de erro máxima** caixa de diálogo permite adicionar uma mensagem de erro personalizada a ser exibida, se você inserir uma data posterior à data especificada no **Data máxima** opção.


### Guia Conteúdo da Ajuda {#help-content-tab}

![Guia Conteúdo da Ajuda](/help/adaptive-forms/assets/datepicker_helptab.png)

* **Descrição curta** - Uma breve descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative o **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta**- Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda** - O texto da Ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto da Ajuda fornece informações mais detalhadas do que o rótulo de um campo de formulário ou o texto de espaço reservado, e foi projetado para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.


### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

**Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias assistivas, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

### Guia Formatos {#format-tab}

![Guia Formatos](/help/adaptive-forms/assets/datepicker_formattab.png)

* **Exibir formato** - Representa o formato de data exibido ao usuário. O **Tipo** permite que o usuário selecione o formato de data. Você também pode personalizar o formato de data usando o **Personalizado** na **Tipo** menu suspenso.

* **Editar formato** - Representa um formato de data no qual o usuário pode editar a data. O **Tipo** permite que o usuário selecione o formato de data. Você também pode personalizar o formato de data usando o **Personalizado** na **Tipo** menu suspenso.

* **Exibir formato** - Representa o formato de data exibido ao usuário. A opção Tipo permite que o usuário selecione o formato de data. Você também pode personalizar o formato de data usando o **Personalizado** na **Tipo** menu suspenso.

* **Editar formato** - Representa um formato de data no qual o usuário edita a data. A opção Tipo permite que o usuário selecione o formato de data. Você também pode personalizar o formato de data usando o **Personalizado** na **Tipo** menu suspenso.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente Seletor de data.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar estilos de CSS de um componente. O Componente principal do seletor de data adaptável do Forms é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Guia Estilo](/help/adaptive-forms/assets/datepicker_styletab.png)

* **Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal do seletor de data da Forms adaptável.

* **Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Guia Formatos {#formats-tab}

A guia format permite especificar os formatos de data padrão e personalizados.

![Guia Formatação](/help/adaptive-forms/assets/datepicker_formatpolicy.png)
