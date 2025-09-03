---
title: 'Componente principal de formulários adaptáveis: data e hora'
description: Usar ou personalizar o componente principal de data e hora dos formulários adaptáveis.
role: Architect, Developer, Admin, User
source-git-commit: daeabccaff39e255c111c6af2540ca4d5be0c709
workflow-type: ht
source-wordcount: '1898'
ht-degree: 100%

---


# Componente de data e hora

Um componente de data e hora em um formulário adaptável é um elemento da interface que permite que os usuários selecionem **a data e a hora** por meio de uma interface de calendário e relógio, ou insiram valores manualmente em um formato específico. Ele garante uma entrada precisa e padronizada para casos de uso em que a data e a hora são essenciais.

**Exemplo**

![exemplo](/help/adaptive-forms/assets/date-time-picker.png)

## Uso {#reasons-to-use-date-time-picker}

Há vários motivos por que é vantajoso incluir um seletor de data e hora em um formulário, incluindo:

- **Conveniência**: permite que os usuários escolham facilmente a data e a hora sem precisar digitar valores manualmente.
- **Consistência**: força um formato padrão para entradas de data e hora no formulário.
- **Experiência do usuário aprimorada**: fornece uma interface intuitiva com seletores de calendário e hora.
- **Programação de eventos**: útil em formulários de programação de compromissos, entrevistas ou reuniões.
- **Viagens e reservas**: permite que os usuários selecionem datas e horas de check-in/check-out.
- **Precisão dos dados**: reduz os erros de entrada em comparação com a entrada de texto livre.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal de data e hora dos formulários adaptáveis foi lançado em **agosto de 2025** como parte dos **Componentes principais 2.24.6** para o Cloud Service e posteriores.

| Versão do componente | AEM as a Cloud Service | AEM Forms 6.5.16.0 ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.24.6](/help/adaptive-forms/version.md) e posteriores | |

Para mais detalhes sobre versões, consulte [Versões dos componentes principais](/help/adaptive-forms/version.md).

## Detalhes técnicos {#technical-details}

Confira os detalhes técnicos mais recentes do componente principal de data e hora dos formulários adaptáveis no [GitHub](https://github.com/adobe/aem-core-forms-components). Para mais informações sobre o desenvolvimento dos componentes principais, consulte a [documentação dos componentes principais para desenvolvedores](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite a personalização da data e da hora.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/datetime_basictab.png)

- **Nome**: O nome identifica exclusivamente o componente no editor de regras. Caracteres especiais e espaços não são permitidos nas strings de nome.

- **Título**: Título é uma string que aparece na parte superior de um componente em um Formulário adaptável. Título identifica exclusivamente o componente na estrutura em árvore de um Formulário adaptável. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.
- **Permitir rich text para título**: esse recurso permite formatar títulos de texto simples, incorporando recursos como negrito, itálico, texto sublinhado, várias fontes, tamanhos de fonte, cores e uma opção adicional para aprimorar a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção **Permitir rich text para título**, as opções de formatação se tornam visíveis para estilizar o título do componente. Para acessar todas as opções de formatação disponíveis, clique no ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: Selecione essa opção para ocultar o título do tipo de componente em um Formulário adaptável.

- **Texto de espaço reservado**: O texto do espaço reservado em um componente de formulário refere-se a um rótulo curto ou prompt que aparece em um campo de entrada como uma dica para o usuário sobre que tipo de informação deve ser inserida nesse campo. O texto de espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não age como um rótulo ou valor permanente para o campo.
- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.

- **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Data e hora padrão**: esta opção permite adicionar uma data e uma hora ao campo de formulário. A data inserida aparece por padrão no local do componente. Se nenhuma data ou hora for inserida pelo usuário, esse valor será enviado no momento do envio do formulário. Se a opção **Componente desabilitado** ou **Componente somente de leitura** for selecionada, a data e a hora padrão serão exibidas na tela e enviadas no momento do envio do formulário.

### Guia de validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/datetime_validation.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve fazer uma seleção antes de prosseguir com o envio de formulário. Não é possível selecionar a opção **Ocultar componente** ou **Desativar componente** na guia **Básico** quando essa opção estiver selecionada.

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

- **Mensagem de validação de script**: essa opção permite inserir uma mensagem que será exibida se a validação do script falhar.

- **Data mínima** - Essa opção permite inserir a data mínima exigida. Se você inserir uma data anterior à data especificada na data e hora mínimas, uma mensagem de erro aparecerá na tela. A caixa de diálogo **Mensagem de erro mínima** permite adicionar uma mensagem de erro personalizada.

- **Mensagem de erro de mínimo**: a caixa de diálogo **Mensagem de erro de mínimo** permite adicionar uma mensagem de erro personalizada a ser exibida se você inserir uma data ou uma hora anterior à especificada na opção **Data mínima**.

- **Data máxima**: esta opção permite que você insira a data e a hora máximas necessárias. Se você inserir uma data ou hora posterior à data ou hora especificada em “Data máxima”, uma mensagem de erro aparecerá na tela. A caixa de diálogo **Mensagem de erro máxima** permite adicionar uma mensagem de erro personalizada.

- **Mensagem de erro de máximo**: a caixa de diálogo **Mensagem de erro de máximo** permite adicionar uma mensagem de erro personalizada a ser exibida se você inserir uma data ou hora posterior à especificada na opção **Data máxima**.

### Guia Conteúdo de ajuda {#help-content-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/datetime_helptab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**- Ative a opção para exibir a Descrição curta abaixo do componente.

- **Texto da ajuda**: O texto da ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.


### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/datetime_accessibilitytab.png)

- **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por pessoas com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.
   - **Texto personalizado**: selecione essa opção para usar o texto personalizado para rótulos de acessibilidade ARIA. Selecionar essa opção exibe a caixa de diálogo Texto personalizado. Você pode adicionar informações relevantes na caixa de diálogo Texto personalizado.
   - **Descrição**: selecione essa opção para usar a descrição para rótulos de acessibilidade ARIA.
   - **Título**: selecione essa opção para usar o título para rótulos de acessibilidade ARIA.
   - **Nome**: selecione essa opção para usar o nome para rótulos de acessibilidade ARIA.
   - **Nenhum**: selecione essa opção se não quiser adicionar rótulos de acessibilidade ARIA.

<!--
### Formats Tab {#format-tab}

![Formats tab](/help/adaptive-forms/assets/datepicker_formattab.png)

-   **Display Format** - It represents the date format that is displayed to the user. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.

-   **Edit Format** - It represents a date format in which the user can edit the date. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.
-  **Format error message** - This option allows you to enter the message displayed on the screen when the entered date is not in the correct format.
- **Language** - This feature is used for formatting the specific field. When a user selects any language option from the **Type** drop-down menu, the **IETF BCP 47 language tag** option appears in the panel. You can choose the language for field formatting when translating an Adaptive Form into a specific language.
  
The set of languages is not visible by default, but users can input a custom **IETF BCP 47 language tag** by updating the template policy:

  1. Open the corresponding template associated with an Adaptive Form in the template editor.
  2. Select the existing policy as `datepicker-default-policy` from the drop-down menu.
   
        ![Date Picker template Policy](/help/adaptive-forms/assets/date-picker-template-policy.png)

  3. Click **Done**.

        >[!NOTE]
        >
        > For further information on how to translate an Adaptive Form to a specific locale, [click here](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).
-->

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar estilos de CSS do componente de data e hora.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de data e hora dos formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Guia Estilo](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Classes padrão do CSS**: você pode fornecer uma classe padrão do CSS ao componente principal de data e hora dos formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/datepicker_customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de chave e valor) a um componente principal de formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: toque ou clique e arraste para alterar a ordem do nome e do valor da propriedade personalizada.

<!--
### Formats Tab {#formats-tab}

The formats tab allows you to specify default and custom date formats.

![Formattab](/help/adaptive-forms/assets/datepicker_formatpolicy.png)



## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=pt-BR)

-->

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}


