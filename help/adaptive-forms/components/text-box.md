---
title: 'Componente principal de Formulários adaptáveis: Entrada de texto (caixa de texto)'
description: Uso ou personalização do Componente principal de entrada de texto de Formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 49d9fe69-0578-4489-beaa-a18cdb14add7
source-git-commit: 732efc9ed450aa31078ecaad65c0c306679fe97e
workflow-type: ht
source-wordcount: '2124'
ht-degree: 100%

---

# Componente de caixa de texto{#text-input-adaptive-forms-core-component}

Um componente de entrada de texto (caixa de texto) permite que um usuário insira e edite uma única ou várias linhas de texto, dependendo do atributo tipo do elemento de entrada. O componente de entrada de texto pode ser colocado em um formulário e geralmente é rotulado com um texto que identifica facilmente sua finalidade. Esses são elementos fundamentais de qualquer formulário, amplamente usados para coletar diferentes tipos de dados dos usuários. Eles são simples, flexíveis e podem ser configurados para validar entradas e melhorar a precisão da coleção de dados.

**Exemplo**

![exemplo](/help/adaptive-forms/assets/text-input.png)


## Uso {#reasons-to-use-text-input-field}

Há vários motivos para usar o componente de entrada de texto em um Formulário adaptável:

- **Coleção de dados**: os campos de entrada de texto são um dos elementos de formulário mais comuns usados para coletar uma grande variedade de informações dos usuários, como nomes, endereços de email, números de telefone e outros tipos de dados de texto.

- **Fácil de usar**: os campos de entrada de texto são simples e fáceis de usar, facilitando a inserção e edição de texto pelos usuários.

- **Flexibilidade**: os campos de entrada de texto podem ser usados para coletar uma grande variedade de informações, desde entradas de texto curtas com uma única linha até entradas de texto mais longas com várias linhas.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal de caixa de texto de formulários adaptáveis foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM Forms 6.5.16.0 ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre as guias dos Formulários adaptáveis nos melhores Componentes principais na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de entrada de texto para visitantes com a caixa de diálogo Configurar. Você também pode definir opções de entrada de texto com facilidade para uma experiência do usuário perfeita.

### Guia Básico

![Guia Básico](/help/adaptive-forms/assets/textinput_basictab.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: o título permite identificar facilmente um componente em um formulário; por padrão, ele aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.
- **Permitir rich text para título**: esse recurso permite formatar títulos de texto simples, incorporando recursos como negrito, itálico, texto sublinhado, várias fontes, tamanhos de fonte, cores e uma opção adicional para aprimorar a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção **Permitir rich text para título**, as opções de formatação se tornam visíveis para estilizar o título do componente. Para acessar todas as opções de formatação disponíveis, clique no ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: selecione essa opção para ocultar o título do componente.

- **Texto de espaço reservado**: o texto de espaço reservado em um componente de formulário refere-se a um rótulo curto ou exemplo que aparece em um campo de entrada como uma dica para o usuário sobre que tipo de informação deve ser inserida nesse campo. O texto de espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não age como um rótulo ou valor permanente para o campo.
- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.
- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.

- **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

- **Valor padrão**: essa opção permite adicionar um valor padrão a um campo de formulário. O texto desaparece quando o usuário começa a digitar no campo. Se o **Componente desativado** ou o **Componente de somente leitura** for selecionado, o valor padrão será exibido na tela. Se nenhum valor for inserido pelo usuário no campo de formulário, esse será o valor enviado no momento do envio do formulário.

- **Permitir várias linhas**: essa opção permite que o usuário insira várias linhas em um campo de formulário.

- **Preencher atributo automaticamente**: a opção permite que os usuários insiram um valor que é preenchido automaticamente no campo de formulário com base nas informações armazenadas.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/textinput_validationtab.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve inserir um valor antes de prosseguir com o envio de formulário. Não é possível selecionar as opções **Ocultar componente** ou **Desativar Componente** na guia **Básico** quando essa opção está selecionada.

- **Mensagem de erro**: essa opção permite que você insira uma mensagem que será exibida se uma caixa de seleção **Obrigatória** estiver marcada mas o campo ficar em branco.

- **Mensagem de validação de script**: essa opção permite que você insira uma mensagem que será exibida caso haja falha na validação do script.

- **Número máximo de caracteres**: essa opção permite especificar o número máximo de caracteres permitidos no componente. Se você inserir mais caracteres que o valor especificado em **Número máximo de caracteres**, uma mensagem de erro será exibida na tela. A caixa de diálogo **Mensagem de erro de máximo de caracteres** permite adicionar uma mensagem de erro personalizada.

- **Mensagem de erro de máximo de caracteres**: a caixa de diálogo **Mensagem de erro de máximo de caracteres** permite adicionar uma mensagem de erro personalizada que será exibida se você inserir mais caracteres que o valor especificado na opção **Número máximo de caracteres**.

- **Número mínimo de caracteres**: essa opção possibilita especificar o número mínimo de caracteres permitidos no campo. Se você inserir menos caracteres que o valor especificado em **Número mínimo de caracteres**, uma mensagem de erro será exibida na tela. A caixa de diálogo **Mensagem de erro de mínimo de caracteres** permite adicionar uma mensagem de erro personalizada.

- **Mensagem de erro de mínimo de caracteres**: a caixa de diálogo **Mensagem de erro de mínimo de caracteres** permite adicionar uma mensagem de erro personalizada que será exibida se você inserir menos caracteres que o valor especificado na opção **Número mínimo de caracteres**.

A opção **Padrão de validação** permite inserir um padrão para validar o texto inserido. Caso haja falha ao validar o texto com o valor inserido na opção **Padrão**, a mensagem de erro será exibida na tela.

- **Padrão**: essa opção permite inserir os padrões permitidos de verificação de texto. Expressões regulares também são permitidas.

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida na tela caso haja falha ao validar o texto inserido com o valor definido na opção **Padrão**

### Guia Conteúdo de ajuda {#help-content-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/textinput_helptab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/textinput_accessibiltytab.png)

- **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.
   - **Texto personalizado**: selecione essa opção para usar o texto personalizado para rótulos de acessibilidade ARIA. Selecionar essa opção exibe a caixa de diálogo Texto personalizado. Você pode adicionar informações relevantes na caixa de diálogo Texto personalizado.
   - **Descrição**: selecione essa opção para usar a descrição para rótulos de acessibilidade ARIA.
   - **Título**: selecione essa opção para usar o título para rótulos de acessibilidade ARIA.
   - **Nome**: selecione essa opção para usar o nome para rótulos de acessibilidade ARIA.
   - **Nenhum**: selecione essa opção se não quiser adicionar nada aos rótulos de acessibilidade ARIA.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar os estilos CSS do componente Caixa de texto.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de Caixa de texto de formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Guia Estilo](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Classes CSS padrão**: é possível fornecer uma classe CSS padrão para o Componente principal de caixa de texto de formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

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
