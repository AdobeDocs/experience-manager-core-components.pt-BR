---
title: 'Componente principal dos formulários adaptáveis: componente Interruptor'
description: Utilização ou personalização do componente principal interruptor para formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 6ff2ca76-1514-42eb-bde3-60259af2d187
hide: true
hidefromtoc: true
source-git-commit: a6c3fd98bcdcbb0d6d5697b93306adc9ef7e3fc9
workflow-type: tm+mt
source-wordcount: '1867'
ht-degree: 100%

---

# Componente interruptor{#switch-adaptive-forms-core-component}

<span class="preview"> Este artigo tem conteúdo sobre os recursos **Permitir rich text para título** e **Permitir rich text para opções**, recursos de pré-lançamento. O recurso de pré-lançamento pode ser acessado somente por meio do [canal de pré-lançamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=pt-BR#new-features).</span>

O componente interruptor é uma interface gráfica usada em formulários que permite selecionar entre duas opções. Normalmente, é um botão de alternância entre dois estados que permite a escolha entre esses dois estados, ativando ou desativando um recurso, uma configuração ou uma funcionalidade. O componente interruptor foi projetado para representar visualmente o estado atual e exibir se um recurso específico está ativado ou desativado.

O componente interruptor é um elemento de controle booleano que define o valor como verdadeiro ou falso. Por exemplo, ele é usado para ativar ou desativar um recurso, como ligar ou desligar o som, o Bluetooth ou o Wi-Fi.

![Exemplo do componente interruptor](/help/adaptive-forms/assets/switch-example.png)

## Uso {#reasons-to-use-switch}

Estes são alguns motivos comuns para usar interruptores em um formulário adaptável:

- **Interação do usuário**: os usuários podem interagir com o componente de interruptor, clicando ou tocando nele.

- **Estados**: o componente interruptor tem dois estados: LIGADO e DESLIGADO. O estado inicial do componente interruptor depende da configuração padrão ou do status atual do recurso que ele controla.

- **Representação visual**: o componente interruptor reflete visualmente seu estado atual, alterando a cor ou a posição.

- **Controle de funcionalidades**: o componente interruptor é usado para ativar ou desativar funcionalidades específicas em um formulário do AEM. Por exemplo, ele permite ativar ou desativar um recurso.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal interruptor para formulários adaptáveis foi lançado como parte dos componentes principais 2.0.64. Esta tabela mostra todas as versões compatíveis, bem como a compatibilidade com o AEM, e inclui links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível com a <br>[versão 2.0.64](/help/adaptive-forms/version.md) e posteriores | Compatível | Compatível |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal interruptor para formulários adaptáveis na documentação técnica, encontrada no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/switch/v1/switch). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência com o componente interruptor para visitantes com a caixa de diálogo “Configurar”. Também é possível definir as opções do componente interruptor com facilidade para uma experiência do usuário suave.

### Guia Básico

![Guia Básico](/help/adaptive-forms/assets/switch-basic.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: com o título, é possível identificar facilmente um componente em um formulário; por padrão, o título aparece ao lado do componente. Se você não adicionar um título, o componente não será exibido.
- **Permitir rich text para título**: esse recurso permite formatar títulos de texto simples, incorporando recursos como negrito, itálico, texto sublinhado, várias fontes, tamanhos de fonte, cores e uma opção adicional para aprimorar a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção **Permitir rich text para título**, as opções de formatação se tornam visíveis para estilizar o título do componente. Para acessar todas as opções de formatação disponíveis, clique no ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: selecione essa opção para ocultar o título do componente.

- **Preservar o valor do estado desmarcado**: selecionar esta opção permite especificar o valor a ser retornado quando o componente interruptor não estiver selecionado.
- **Opções**: especifique o valor dos dados e o texto de exibição de cada opção.
   - **Valor dos dados quando ativado**: especifique o valor a ser enviado quando a opção estiver habilitada em um formulário adaptável.
   - **Texto de exibição quando ativado**: especifique o texto a ser exibido como rótulo quando o interruptor estiver habilitado em um formulário adaptável.
   - **Valor dos dados quando desativado**: especifique o valor a ser enviado quando a opção não estiver habilitada em um formulário adaptável. Esta opção estará visível somente se a opção **Preservar o valor do estado desmarcado** estiver habilitado.
   - **Texto de exibição quando desativado**: especifique o texto a ser exibido como rótulo quando a opção não estiver habilitada em um formulário adaptável. Esta opção estará visível somente se a opção **Preservar o valor do estado desmarcado** estiver habilitado.

  Também é possível formatar as opções do componente de alternância usando **Permitir rich text para opções**.

  ![Suporte a rich text para opções](/help/adaptive-forms/assets/switch-optipn-rich-text.png)

  Depois de marcar a caixa de seleção **Permitir rich text para opções**, as opções de formatação se tornam visíveis para estilizar as opções do componente. Para acessar todas as opções de formatação disponíveis, clique no `Fullscreen` ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text para opções](/help/adaptive-forms/assets/switch-richtext-for-display.png)

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

- **Ocultar rótulos**: selecione esta opção para ocultar os rótulos do componente interruptor.

- **Mostrar rótulos**: selecione esta opção para mostrar os rótulos do componente interruptor.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar os estilos do CSS do componente interruptor.

### Guia Estilos {#styles-design-tab}

O componente principal de interruptor para formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes padrão do CSS**: você pode fornecer uma classe padrão do CSS ao componente principal do grupo de interruptores para formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de chave e valor) a um componente principal para formulários adaptáveis, usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.
- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reordenar**: toque ou clique e arraste para reordenar o nome e o valor da propriedade personalizada.

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}
