---
title: Componente principal adaptável do Forms - guias verticais
description: Uso ou personalização do Componente principal de guias verticais adaptáveis do Forms.
role: Architect, Developer, Admin, User
exl-id: d5cd1c18-6840-4f2f-a767-a69b803e6075
source-git-commit: 4ca65f93e223fdd0b0a701ef335ed5be1fbab7fe
workflow-type: tm+mt
source-wordcount: '1904'
ht-degree: 65%

---

# Componente de Guias Verticais{#vertical-tabs-adaptive-forms-core-component}

Guias verticais em um Formulário adaptável se referem a um padrão de design em que várias seções de um formulário são agrupadas e exibidas como guias separadas, alinhadas verticalmente. O usuário pode alternar entre as guias para acessar diferentes seções do formulário. Cada guia atua como um acionador para mostrar e ocultar o conteúdo do formulário relacionado. As guias verticais ajudam a organizar formulários longos em seções gerenciáveis e melhorar a experiência do usuário. As guias podem ajudar a tornar um formulário mais acessível para pessoas com deficiências, pois elas podem alternar entre as seções usando a navegação pelo teclado.

Quando um usuário clica em uma guia, o conteúdo do formulário é atualizado dinamicamente para mostrar a seção correspondente.

![exemplo](/help/adaptive-forms/assets/horizontal-example.png)

## Uso {#reasons-to-use-vertical-tabs}

Os motivos comuns para usar guias verticais em um Formulário adaptável são:

- **Maior usabilidade**: guias verticais facilitam a navegação dos usuários pelo formulário, especialmente se ele tiver várias seções ou um grande número de campos.

- **Gerenciamento de espaço**: guias verticais ajudam a conservar o espaço na tela, agrupando seções de formulário relacionadas em guias e exibindo apenas uma seção por vez.

- **Melhor organização**: as guias fornecem uma estrutura clara e organizada para um formulário, tornando mais fácil para os usuários a compreensão e o preenchimento do formulário.

- **Maior engajamento do usuário**: guias verticais podem tornar um formulário visualmente mais atraente e envolvente para os usuários, o que pode melhorar a taxa de conclusão do formulário.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal de guias verticais do Forms adaptável foi lançado como parte dos Componentes principais 2.0.18. Esta tabela mostra todas as versões compatíveis, a compatibilidade com o AEM e os links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível com<br>[versão 2.0.18](/help/versions.md) e posterior | Compatível | Compatível |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de guias verticais adaptáveis do Forms na documentação técnica sobre [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/verticaltabs/v1/verticaltabs). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).


## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência com guias verticais para visitantes com a caixa de diálogo de configuração. Você também pode definir opções de Guias verticais com facilidade para obter uma experiência perfeita para o usuário.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/vertical-tab-basic.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Ocultar Título**: Selecione a opção para ocultar o Título do componente.

- **Agrupar dados de componentes secundários no envio do formulário (vincular dados no objeto)**: quando essa opção é selecionada, os dados dos componentes secundários são aninhados no objeto JSON do componente principal. No entanto, se a opção não estiver selecionada, os dados JSON enviados terão uma estrutura simples, sem qualquer objeto para o componente principal. Por exemplo:

   - Quando a opção é selecionada, os dados dos componentes secundários (por exemplo, Rua, Cidade e CEP) são aninhados no componente principal (Endereço) como um objeto JSON. Isso cria uma estrutura hierárquica e os dados são organizados no componente principal.

     Estrutura dos dados enviados:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Quando a opção não está selecionada, os dados JSON enviados têm uma estrutura simples sem qualquer objeto para o componente principal (Endereço). Todos os dados estão no mesmo nível, sem qualquer organização hierárquica.


     Estrutura dos dados enviados:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.
- **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Repetir tabulação vertical {#repeat-tabs-on-top}

![Repetir guia](/help/adaptive-forms/assets/vertical-tab-repeat-vertical-tab.png)

Você pode usar as opções de repetibilidade para duplicar o componente de guias verticais e seus componentes filhos, definir uma contagem de repetição mínima e máxima e facilitar a replicação de seções semelhantes em um formulário. Ao interagir com o componente de guias verticais e acessar suas configurações, as seguintes opções são apresentadas:

- **Tornar guias verticais repetíveis**: um recurso de alternância que permite aos usuários ativar ou desativar a funcionalidade de repetibilidade.
- **Mínimo de repetições**: estabelece o número mínimo de vezes que o componente de Guias verticais pode ser repetido. Um valor zero indica que o componente de guias verticais não é repetido; o valor padrão é zero.
- **Máximo de repetições**: define o número máximo de vezes que o componente de Guias verticais pode ser repetido. Por padrão, esse valor é ilimitado.

Para gerenciar com eficácia as seções repetíveis nas guias Verticais, siga as etapas fornecidas no [Criação de formulários com seções repetíveis](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=pt-BR) artigo.

### Guia Itens {#items-tab}

![Guia Itens](/help/adaptive-forms/assets/vertical-tab-items.png)

O botão **Adicionar** permite selecionar um componente da janela de seleção de componentes para adicionar como um painel. Após adicionar o componente, você verá as seguintes opções:

- **Ícone** - O ícone identifica o componente do painel na lista. Você pode passar o mouse sobre o ícone para ver o nome completo do componente como uma dica de ferramenta.
- **Descrição** - A descrição usada como o texto do painel. Por padrão, o nome do componente selecionado para o painel é usado.
- **Excluir** - Toque ou clique para excluir o painel do componente de Guias verticais.
- **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem dos painéis.

### Guia Conteúdo de ajuda {#help-content}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/vertical-tab-help.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/vertical-tab-accessibility.png)

- **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

- **Função de HTML para anúncio do leitor de tela**: a função HTML é um atributo usado para especificar a finalidade de um elemento HTML para tecnologias assistivas, como leitores de tela. O atributo de função é usado para fornecer contexto e significado semântico adicionais a um elemento, facilitando a interpretação e o anúncio do conteúdo pelos leitores de tela. Por exemplo, no AEM Forms, o rótulo de um campo de formulário pode ter a função de “rótulo” e seu campo de entrada pode ter a função de “caixa de texto”. Isso ajuda o leitor de tela a entender a relação entre o rótulo e o campo de entrada e anunciá-los corretamente ao usuário.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que os criadores de modelos controlem a exibição padrão dos elementos. Para o componente de guias verticais adaptáveis do Forms, você pode definir o seguinte:

- Os componentes principais que um criador de formulário pode adicionar às guias verticais no editor adaptável do Forms
- Nomes simples para estilos (classes CSS) que podem ser aplicados na caixa de diálogo de propriedades do componente de guias verticais no editor Forms adaptável.

Isso ajuda a tornar o processo de criação e personalização de formulários mais simples e eficiente.

### Guia Componentes permitidos {#allowed-components-tab}

![Guia Componentes permitidos](/help/adaptive-forms/assets/tabs-allowed-component.png)

A variável **Componentes permitidos** permite que o editor de modelo defina os componentes que podem ser adicionados como itens aos painéis no componente Guias verticais no editor Forms adaptável.

### Guia Estilos {#styles-tab}

![Guia Estilos](/help/adaptive-forms/assets/tabs-styles-tab.png)

A caixa de diálogo de design é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de guias verticais do Forms adaptável é compatível com AEM [Sistema de Estilos](/help/get-started/authoring.md#component-styling).

- **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o Componente principal de guias verticais do Forms adaptável.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Guia Propriedades personalizadas

![Guia Propriedades personalizadas](/help/adaptive-forms/assets/tabs-custom-properties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de valores chave) a um componente principal do formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Ela permite criar um comportamento de formulário dinâmico que se adapta com base nos valores de atributos personalizados. Por exemplo, os desenvolvedores podem projetar várias representações de um componente headless do Forms para plataformas móveis, de desktop ou da Web, melhorando significativamente a experiência do usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: Você pode fornecer um nome para identificar o grupo de propriedades personalizadas. Você pode adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Depois de adicionar o grupo de propriedades personalizadas, você pode ver as seguintes opções:

   - **Pares de valor-chave**: É possível adicionar vários nomes de propriedades personalizadas e valores de propriedades personalizadas clicando no **Adicionar** para cada grupo de propriedades personalizadas.

   - **Excluir**: Toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: Toque ou clique e arraste para reorganizar a ordem do nome e do valor da propriedade personalizada.

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}