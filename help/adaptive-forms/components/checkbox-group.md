---
title: Componente principal de Formulários adaptáveis - Grupo de caixa de seleção
description: Utilização ou personalização do Componente principal do grupo de caixa de seleção de Formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 2ced0223-e664-470b-a400-b6865d3a67c9
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '2102'
ht-degree: 99%

---

# Componente do grupo de caixas de seleção {#button-component-adaptive-forms-core-component}

Um grupo de caixas de seleção em um formulário adaptável é um conjunto de caixas de seleção relacionadas que permitem selecionar uma ou mais opções de uma lista. Cada caixa de seleção é representada por um Valor de dados (usado para processar itens de um grupo de caixas de seleção) e Valor de exibição (rótulo para cada item de caixa de seleção que descreve sua finalidade)
**Exemplo**

![exemplo de grupo de caixas de seleção](/help/adaptive-forms/assets/checkbox-group.png)

**Caixa de diálogo Propriedades**

![caixa de diálogo de propriedades do grupo de caixas de seleção](/help/adaptive-forms/assets/checkbox-group-properties.png)

Neste exemplo, o elemento Opções é usado para agrupar as caixas de seleção. O elemento **Texto de exibição** é usado para fornecer um rótulo para um item e **Valor de dados** é usado para especificar o valor enviado para o servidor após o envio do formulário.

Cada item/opção de caixa de seleção tem um Valor de dados e um atributo de Texto de exibição exclusivos. Se um usuário marcar as caixas de seleção “Filho” e “Filha”, o Valor de dados correspondente será enviado para o servidor após o envio do formulário. Esses dados podem então ser processados por um script do lado do servidor para determinar quais opções foram selecionadas pelo usuário, e podem ser usados para executar várias ações, como atualizar outros campos no formulário ou enviar os dados do formulário para um script do lado do servidor para processamento adicional.

Além disso, o grupo de caixas de seleção pode ser configurado para ter valores de processamento diferentes para cada opção, o que pode ser definido usando o Editor de regras de Formulários adaptáveis.

## Uso {#reasons-to-use-check-box-group}

Incluir um grupo de caixas de seleção em um Formulário adaptável é vantajoso por diversos motivos, dentre eles:

- **Várias seleções**: um grupo de caixas de seleção permite que os usuários selecionem várias opções de uma lista, o que pode ser útil em situações em que várias seleções são permitidas ou obrigatórias.

- **Experiência do usuário**: o grupo de caixas de seleção pode ser usado para tornar o formulário mais simples, proporcionando uma maneira clara e intuitiva para os usuários selecionarem várias opções.

- **Análise de dados**: o grupo de caixas de seleção pode ser usado para coletar dados de várias fontes e analisá-los ou usá-los como entrada para processamento adicional.

- **Pesquisas**: o grupo de caixa de seleção pode ser usado em pesquisas para selecionar várias opções para uma pergunta.

- **Preferências do usuário**: o grupo de caixas de seleção pode ser usado para coletar as preferências do usuário para opções diferentes.

- **Valor de dados**: o grupo de caixas de seleção também pode ser usado para processar itens de um grupo de caixas de seleção.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do grupo de caixas de seleção de Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência de caixas de seleção para os visitantes com a caixa de diálogo Configurar. Você também pode definir opções de caixas de seleção com facilidade para uma experiência do usuário ininterrupta.


### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/checkbox_basictab.png)

- **Nome**: o nome identifica exclusivamente o componente no editor de regras. Caracteres especiais e espaços não podem ser usados nas strings de nome.

- **Título**: Com o Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Permitir rich text para título**: esse recurso permite formatar títulos de texto simples, incorporando recursos como negrito, itálico, texto sublinhado, várias fontes, tamanhos de fonte, cores e uma opção adicional para aprimorar a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção **Permitir rich text para título**, as opções de formatação se tornam visíveis para estilizar o título do componente. Para acessar todas as opções de formatação disponíveis, clique no `Fullscreen` ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: selecione essa opção para ocultar o título do componente.

- **Opções**: você pode adicionar pares de valores de dados e textos de exibição usando o botão **Adicionar**. \
  Depois que uma nova opção for adicionada, as seguintes ações poderão ser executadas:
   - **Valor de dados**: essa opção permite inserir o conteúdo a ser enviado quando uma opção for selecionada.
   - **Texto de exibição** - Esta opção permite inserir o conteúdo a ser exibido em um Formulário adaptável.
   - **Excluir** - Toque ou clique para excluir a opção de uma caixa de seleção.
   - **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem dos painéis.

  Você também pode formatar as opções para o grupo de caixas de seleção usando **Permitir rich text para opções**.

  ![Suporte a rich text para opções](/help/adaptive-forms/assets/richtext-for-options.png)

  Depois de marcar a caixa de seleção **Permitir rich text para opções**, as opções de formatação se tornam visíveis para estilizar as opções do componente. Para acessar todas as opções de formatação disponíveis, clique no `Fullscreen` ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).
  ![Suporte a rich text para opções](/help/adaptive-forms/assets/richtextoptions-support.png)

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.

- **Tipo de dados do valor enviado**: essa opção especifica o tipo de dados do valor enviado quando qualquer opção é selecionada. Se o **tipo de dados do valor enviado** estiver definido como `Number` e você adicionar string de dados ao **Valor de dados** na guia **Opções**, a tela exibirá uma mensagem de erro de `Value type mismatch`.

- **Opções de exibição**: Esta opção é usada para definir o alinhamento visual das caixas de seleção em um Formulário adaptável. As duas opções compatíveis são:
   - **Horizontal** - Quando essa opção é selecionada, as caixas de seleção são exibidas da esquerda para a direita em um Formulário adaptável.
   - **Vertical** - Quando essa opção é selecionada, as caixas de seleção são exibidas de cima para baixo em um Formulário adaptável.

- **Opções padrão**: Essa opção permite que você adicione valores padrão pré-selecionados quando o formulário é carregado. Use o ícone excluir para remover as opções adicionadas. Se o **tipo de dados do valor enviado** está definido como `Number` e você adicionar dados da string às **Opções padrão**, a tela exibe uma `Value type mismatch` mensagem de erro.
- **Ocultar componente**: Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/checkbox_validationtab.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve fazer uma seleção antes de prosseguir com o envio de formulário. Não é possível selecionar **Ocultar componente** ou **Desativar componente** na guia **Básico** quando essa opção estiver selecionada.

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

- **Mensagem de validação de script**: essa opção permite que inserir uma mensagem que será exibida se a validação do script falhar.

### Guia Conteúdo de ajuda {#helpcontent-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/checkbox_helptab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/checkbox_accessibility.png)

- **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.
   - **Texto personalizado**: selecione essa opção para usar o texto personalizado para rótulos de acessibilidade ARIA. Selecionar essa opção exibe a caixa de diálogo Texto personalizado. Você pode adicionar informações relevantes na caixa de diálogo Texto personalizado.
   - **Descrição**: selecione essa opção para usar a descrição para rótulos de acessibilidade ARIA.
   - **Título**: selecione essa opção para usar o título para rótulos de acessibilidade ARIA.
   - **Nome**: selecione essa opção para usar o nome para rótulos de acessibilidade ARIA.
   - **Nenhum**: selecione essa opção se não quiser adicionar nada aos rótulos de acessibilidade ARIA.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente Grupo de caixa de seleção.

### Guia Estilos {#styles-tab}

O Componente principal do grupo da caixa de seleção de Formulários adaptáveis é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o Componente principal do grupo de caixas de seleção de Formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de chave e valor) a um componente principal de formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: toque ou clique e arraste para alterar a ordem do nome e do valor da propriedade personalizada.

## Artigos relacionados {#related-articles}

{{more-like-this}})

## Consulte também {#see-also}

{{see-also}}
