---
title: Componente principal adaptável do Forms - Componente de switch
description: Uso ou personalização do Componente principal do switch Forms adaptável.
role: Architect, Developer, Admin, User
hide: true
hidefromToC: true
source-git-commit: d172e019c5621d950a94cbdd8d27e4834dbabe3b
workflow-type: tm+mt
source-wordcount: '1689'
ht-degree: 67%

---


# Alternar componente{#switch-adaptive-forms-core-component}

O componente de switch é uma interface gráfica do usuário usada em formulários que permite aos usuários selecionar entre duas opções. Normalmente, é um botão de alternância de dois estados que permite aos usuários escolher entre dois estados, ativando ou desativando um recurso, uma configuração ou uma funcionalidade. O componente de switch foi projetado para representar visualmente o estado atual e exibir se um recurso específico está ativado ou desativado.

O componente switch é um elemento de controle booleano que define o valor como verdadeiro ou falso. Por exemplo, ele é usado para ativar ou desativar um recurso, como ativar ou desativar o som, ativar ou desativar o Bluetooth ou WiFi.

![Exemplo de componente Switch](/help/adaptive-forms/assets/switch-example.png)

## Uso {#reasons-to-use-switch}

Os motivos comuns para usar a alternância em um Formulário adaptável são:

- **Interação do usuário**: os usuários podem interagir com o componente de switch clicando ou tocando nele.

- **Estados**: O componente de opção tem dois estados: LIGADO e DESLIGADO. O estado inicial do componente de switch depende da configuração padrão ou do status atual do recurso que ele controla.

- **Representação visual**: o componente de alternância reflete visualmente seu estado atual alterando a cor ou a posição.

- **Funcionalidade de controle**: o componente de switch é usado para ativar ou desativar funcionalidades específicas em um Formulário AEM. Por exemplo, permite que os usuários ativem ou desativem um recurso.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal do switch Forms adaptável foi lançado como parte dos componentes principais 2.0.64. Esta tabela mostra todas as versões compatíveis, a compatibilidade com o AEM e os links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível com a <br>[versão 2.0.64](/help/adaptive-forms/version.md) e posteriores | Compatível | Compatível |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do switch Forms adaptável na documentação técnica sobre [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/switch/v1/switch). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do componente Alternar para visitantes com a Caixa de diálogo de configuração. Você também pode definir opções de componentes de Switch com facilidade para obter uma experiência perfeita para o usuário.

### Guia Básico

![Guia Básico](/help/adaptive-forms/assets/switch-basic.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: com o título, é possível identificar facilmente um componente em um formulário; por padrão, o título aparece ao lado do componente. Se você não adicionar um título, o componente não será exibido.

- **Ocultar título**: selecione essa opção para ocultar o título do componente.

- **Preservar valor de estado de Desmarcar** - Selecionar essa opção permite especificar o valor a ser retornado quando o componente de alternância não estiver selecionado.
- **Opções** - Especifique o valor dos dados e o texto de exibição para cada opção.
   - **No valor de dados** - Especifique o valor a ser enviado quando a opção for ativada em um Formulário adaptável.
   - **Texto na exibição** - Especifique o texto a ser exibido como rótulo quando a opção for ativada em um Formulário adaptável.
   - **Valor de dados desativado** - Especifique o valor a ser enviado quando a opção não estiver ativada em um Formulário adaptável. Essa opção estará visível somente se a variável **Preservar valor de estado de Desmarcar** switch está habilitado.
   - **Fora do texto exibido** - Especifique o texto a ser exibido como rótulo quando a opção não estiver ativada em um Formulário adaptável. Essa opção estará visível somente se a variável **Preservar valor de estado de Desmarcar** switch está habilitado.

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.
- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.

- **Tipo de dados do valor enviado**: esta opção especifica o tipo de dados do valor enviado quando uma opção é selecionada. Se o **tipo de dados do valor enviado** estiver definido como `Number` e você adicionar uma string de dados em **Valor de dados** na guia **Opções**, a tela exibirá uma mensagem de erro `Value type mismatch`.
- **Ocultar componente**: Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

- **Desabilitar componente**: selecione essa opção para desabilitar ou bloquear o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

- **Valor padrão**: essa opção permite adicionar um valor padrão a um campo de formulário. Se o **Componente desativado** ou o **Componente de somente leitura** for selecionado, o valor padrão será exibido na tela. Se nenhum valor for inserido pelo usuário no campo de formulário, esse será o valor enviado no momento do envio do formulário.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/switch-validation.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve fazer uma seleção antes de prosseguir com o envio de formulário. Não é possível selecionar **Ocultar componente** ou **Desativar componente** na guia **Básico** quando essa opção estiver selecionada.

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

- **Mensagem de validação de script**: essa opção permite que inserir uma mensagem que será exibida se a validação do script falhar.

### Guia Conteúdo de ajuda {#helpcontent-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/switch-help.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/switch-accessibility.png)

**Texto para leitores de tela**: isso se refere ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

### Guia Estilos {#styles-tab}

![Guia Estilos](/help/adaptive-forms/assets/switch-styles.png)

- **Ocultar rótulos** - Selecione esta opção para ocultar os rótulos do componente de switch.

- **Mostrar rótulos** - Selecione esta opção para mostrar os rótulos do componente de comutação.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar estilos CSS para o componente Switch.

### Guia Estilos {#styles-design-tab}

O componente principal do switch Forms adaptável é compatível com AEM [Sistema de Estilos](/help/get-started/authoring.md#component-styling).

![Caixa de diálogo de design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o Componente principal do grupo de switches Forms adaptável.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de valores chave) a um componente principal do formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: Toque ou clique e arraste para reorganizar o nome da propriedade personalizada e o valor da propriedade personalizada.

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}








