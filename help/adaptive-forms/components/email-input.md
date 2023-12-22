---
title: Componente principal de formulários adaptáveis - Entrada de email
description: Uso ou personalização do componente principal de entrada de email de formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: f6a2974b-991e-4cea-9ef8-0b03e8975eeb
source-git-commit: 120f8023ac2e13380e59703e199dc929176a59b6
workflow-type: ht
source-wordcount: '1916'
ht-degree: 100%

---


# Entrada de email {#Email-input-adaptive-forms-core-component}

O componente principal de entrada de email de formulários adaptáveis é usado para coletar endereços de email dos usuários. O campo de entrada de email permite que o navegador confirme se os dados inseridos estão em um formato de endereço de email válido. Normalmente, ele é representado como uma caixa de texto e tem um padrão de validação que aceita apenas endereços de email válidos. O campo de entrada de email pode ser personalizado ainda mais com atributos adicionais, como “obrigatório”, “espaço reservado” e “padrão” para definir validações para os dados de entrada.

**Exemplo**
![exemplo](/help/adaptive-forms/assets/emailid-example.png)

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

Há várias vantagens de se incluir um componente de entrada de email em um formulário adaptável, incluindo:

- **Conveniente para o usuário**: uma entrada de email facilita a inserção de endereços de email pelos usuários, pois fornece uma indicação clara dos dados esperados no campo.

- **Comunicação personalizada**: a coleta de endereços de email de usuários por meio de um formulário permite uma comunicação personalizada, como o envio de emails de confirmação ou boletins informativos.

- **Geração de clientes potenciais**: ao coletar endereços de email por meio de um formulário, as empresas podem criar suas listas de emails e usá-las para a geração de clientes potenciais.

- **Autenticação do usuário**: endereços de email podem ser usados como um meio de autenticação para acessar conteúdos ou serviços restritos.

- **Coleta de feedback**: uma entrada de email em um formulário de feedback permite que a empresa se comunique com o usuário para obter acompanhamento ou esclarecimentos sobre seu feedback.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal de entrada de email de formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput). Para mais informações sobre o desenvolvimento dos Componentes principais, consulte a [Documentação do desenvolvedor dos componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência de entrada de email para visitantes com a caixa de diálogo de configuração. Você também pode definir opções de entrada de email com facilidade para uma experiência de usuário perfeita.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/email_basictab.png)

- **Nome**: o nome identifica exclusivamente o componente no editor de regras. Caracteres especiais e espaços não podem ser usados nas strings de nome.

- **Título**: Com o Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Ocultar título**: Selecione a opção para ocultar o Título do componente.

- **Texto de espaço reservado**: o texto de espaço reservado de um componente de formulário refere-se a um rótulo curto ou mensagem que aparece em um campo de entrada, fornecendo ao usuário uma dica sobre que tipo de informação deve ser inserida nesse campo. O texto de espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não age como um rótulo ou valor permanente para o campo.

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.
- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.
- **Ocultar componente**: Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

- **Valor padrão**: essa opção permite adicionar um valor padrão a um campo de formulário. Se o **Componente desativado** ou o **Componente somente leitura** for selecionado, o valor padrão será exibido na tela. Se nenhum valor for inserido pelo usuário no campo de formulário, esse valor será enviado no momento do envio do formulário


### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/email_validationtab.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve inserir um valor antes de prosseguir com o envio do formulário. Não é possível selecionar **Ocultar componente** ou **Desabilitar componente** na guia **Básico** quando essa opção está selecionada.

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

- **Mensagem de validação de script**: essa opção permite inserir uma mensagem que será exibida se a validação do script falhar.

- **Número máximo de caracteres**: essa opção permite especificar o número máximo de caracteres permitidos no campo. Se você inserir mais caracteres que o valor especificado em **Número máximo de caracteres**, uma mensagem de erro será exibida na tela. A caixa de diálogo **Mensagem de erro de máximo de caracteres** permite adicionar uma mensagem de erro personalizada.

- **Mensagem de erro de máximo de caracteres**: a caixa de diálogo **Mensagem de erro de máximo de caracteres** permite adicionar uma mensagem de erro personalizada que será exibida se você inserir mais caracteres que o valor especificado na opção **Número máximo de caracteres**.

- **Número mínimo de caracteres**: essa opção possibilita especificar o número mínimo de caracteres permitidos no campo. Se você inserir menos caracteres que o valor especificado em **Número mínimo de caracteres**, uma mensagem de erro será exibida na tela. A caixa de diálogo **Mensagem de erro de mínimo de caracteres** permite adicionar uma mensagem de erro personalizada.

- **Mensagem de erro de mínimo de caracteres**: a caixa de diálogo **Mensagem de erro de mínimo de caracteres** permite adicionar uma mensagem de erro personalizada que será exibida se você inserir menos caracteres que o valor especificado na opção **Número mínimo de caracteres**.
<br>

A opção **Padrão de validação** permite inserir um padrão para validar a ID de email inserida. Caso o valor de ID de email inserido na opção **Padrão** não seja validado, uma mensagem de erro será exibida na tela.

- **Padrão**: essa opção permite inserir os padrões de verificação permitidos para email. Expressões regulares também são permitidas.
- **Mensagem de erro**: esta opção permite inserir uma mensagem a ser exibida na tela se a ID de email não for validada com o valor inserido na opção **Padrão** 

### Guia Conteúdo de ajuda {#help-content-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/email_helptab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/email_accessibilitytab.png)

**Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar estilos CSS para o componente de entrada de email.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de Entrada de email de formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Guia Estilo](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Classes CSS Padrão**: você pode fornecer uma classe CSS padrão para o Componente principal do seletor de datas dos Formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/datepicker_customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de chave e valor) a um componente principal de formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: toque ou clique e arraste para alterar a ordem do nome e do valor da propriedade personalizada.

### Guia Formatos {#formats-tab}

A guia Formatos permite especificar os formatos de data padrão e personalizados.

![Guia Formato](/help/adaptive-forms/assets/emailinput_formattab.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}
