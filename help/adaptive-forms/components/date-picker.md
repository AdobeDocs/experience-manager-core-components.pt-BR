---
title: Componente principal de Formulários adaptáveis - Seletor de datas
description: Utilização ou personalização do Componente principal do seletor de datas de Formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '1738'
ht-degree: 100%

---

# Seletor de data {#date-picker-adaptive-forms-core-component}

Um componente do seletor de datas em um Formulário adaptável é um elemento da interface que permite aos usuários selecionar uma data em um calendário ou inserir manualmente uma data em um formato específico. O componente do seletor de datas pode ser configurado para ter formatação, validação e valores padrão diferentes.

**Exemplo**

![](/help/adaptive-forms/assets/date-picker.png)

## Uso {#reasons-to-use-drop-date-picker}

Há vários motivos pelos quais é vantajoso incluir um seletor de datas em um Formulário adaptável, incluindo:

* **Praticidade**: um componente seletor de datas permite que os usuários selecionem facilmente uma data de um calendário sem precisar inserir manualmente a data em um campo de texto. Isso pode economizar tempo e reduzir erros.

* **Experiência do usuário**: o componente seletor de datas pode ser usado para tornar o formulário mais simples, fornecendo uma maneira clara e intuitiva para os usuários selecionarem a data.

* **Análise de dados**: o componente seletor de datas pode ser usado para coletar dados de várias fontes e analisá-los, ou usá-los como entrada para processamento adicional.

* **Gerenciamento de eventos**: o componente seletor de datas pode ser usado em sites de gerenciamento de eventos para selecionar a data do evento.

* **Reservas**: o componente seletor de datas pode ser usado em sites de reservas para selecionar as datas de check-in e check-out.

* **Formato de data**: o componente seletor de datas pode ser usado para corrigir o formato em que a data é exibida e inserida. Verifique se o formato de data é uniforme em todo o formulário para garantir uma experiência do usuário consistente.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do seletor de datas de Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de seletor de datas para visitantes com a caixa de diálogo Configurar. Você também pode definir opções de seletor de datas com facilidade para proporcionar uma experiência do usuário contínua.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/datepicker_basictab.png)

* **Nome**: O nome identifica exclusivamente o componente no editor de regras. Caracteres especiais e espaços não são permitidos nas strings de nome.

* **Título**: Título é uma string que aparece na parte superior de um componente em um Formulário adaptável. Título identifica exclusivamente o componente na estrutura em árvore de um Formulário adaptável. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

* **Ocultar título**: Selecione essa opção para ocultar o título do tipo de componente em um Formulário adaptável.

* **Texto de espaço reservado**: O texto do espaço reservado em um componente de formulário refere-se a um rótulo curto ou prompt que aparece em um campo de entrada como uma dica para o usuário sobre que tipo de informação deve ser inserida nesse campo. O texto de espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não age como um rótulo ou valor permanente para o campo.

* **Ocultar Componente**: Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Data padrão**: Essa opção permite adicionar uma data ao campo de formulário. A data inserida aparece por padrão no local do componente. Se nenhuma data for inserida pelo usuário, esse valor será enviado no momento do envio do formulário. Se a opção **Componente desativado** ou **Componente somente leitura** for selecionada, a data padrão será exibida na tela e enviada no momento do envio do formulário.


### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/datepicker_validation.png)

* **Obrigatório** - Selecione essa opção se quiser exibir o componente em um Formulário adaptável. Não é possível selecionar a opção **Ocultar componente** ou **Desativar componente** na guia **Básico** quando essa opção estiver selecionada.

* **Mensagem de erro** - Essa opção permite que você insira uma mensagem que é exibida quando a caixa de seleção **Obrigatório** está marcada e o campo do formulário fica em branco.

* **Mensagem de validação de script** - Essa opção permite que você insira uma mensagem que será exibida se a validação do script falhar.

* **Data mínima** - Essa opção permite inserir a data mínima exigida. Se você inserir uma data anterior à data especificada em Data mínima, uma mensagem de erro será exibida na tela. A caixa de diálogo **Mensagem de erro mínima** permite adicionar uma mensagem de erro personalizada.

* **Mensagem de erro mínima** - A caixa de diálogo **Mensagem de erro mínima** permite adicionar uma mensagem de erro personalizada que será exibida se você inserir uma data anterior à especificada na opção **Data mínima**.

* **Data máxima** - Essa opção permite que você insira a data máxima necessária. Se você inserir uma data posterior à data especificada em Data máxima, uma mensagem de erro será exibida na tela. A caixa de diálogo **Mensagem de erro máxima** permite adicionar uma mensagem de erro personalizada.

* **Mensagem de erro máxima** - A caixa de diálogo **Mensagem de erro máxima** permite adicionar uma mensagem de erro personalizada que será exibida se você inserir uma data posterior à data especificada na opção **Data máxima**.


### Guia Conteúdo de ajuda {#help-content-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/datepicker_helptab.png)

* **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta**- Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda**: O texto da ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.


### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

**Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

### Guia Formatos {#format-tab}

![Guia Formatos](/help/adaptive-forms/assets/datepicker_formattab.png)

* **Exibir formato** - Representa o formato de data exibido ao usuário. A opção **Tipo** permite que o usuário selecione o formato de data. Você também pode personalizar o formato de data usando a opção **Personalizado** no menu suspenso **Tipo**.

* **Editar formato** - Representa um formato de data em que o usuário pode editar a data. A opção **Tipo** permite que o usuário selecione o formato de data. Você também pode personalizar o formato de data usando a opção **Personalizado** no menu suspenso **Tipo**.

* **Exibir formato** - Representa o formato de data exibido ao usuário. A opção Tipo permite que o usuário selecione o formato de data. Você também pode personalizar o formato de data usando a opção **Personalizado** no menu suspenso **Tipo**.

* **Editar formato** - Representa um formato de data em que o usuário edita a data. A opção Tipo permite que o usuário selecione o formato de data. Você também pode personalizar o formato de data usando a opção **Personalizado** no menu suspenso **Tipo**.

## Caixa de diálogo de Design {#design-dialog}

A caixa de diálogo de Design é usada para definir e gerenciar estilos de CSS para o componente Seletor de datas.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal do Seletor de datas de formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Guia Estilo](/help/adaptive-forms/assets/datepicker_styletab.png)

* **Classes CSS Padrão**: você pode fornecer uma classe CSS padrão para o Componente principal do seletor de datas dos Formulários adaptáveis.

* **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Guia Formatos {#formats-tab}

A guia Formatos permite especificar os formatos de data padrão e personalizados.

![Guia Formato](/help/adaptive-forms/assets/datepicker_formatpolicy.png)

## Artigo relacionado {#related-article}

* [Criar um formulário adaptável em uma página do AEM Sites ou fragmento de experiência](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=pt-BR)

* [Criar um formulário adaptável independente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=pt-BR)


>[!MORELIKETHIS]
>
>* [Acordeão](/help/adaptive-forms/components/accordion.md)
>* [Botão](/help/adaptive-forms/components/button.md)
>* [Grupo de Caixa de seleção](/help/adaptive-forms/components/checkbox-group.md)
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