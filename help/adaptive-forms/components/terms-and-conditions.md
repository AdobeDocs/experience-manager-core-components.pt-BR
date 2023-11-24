---
title: Componente principal do Forms adaptável - Termos e condições
description: Uso ou personalização do Componente principal dos Termos e condições adaptáveis do Forms.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: ecc6ba79ba5e90bd6e759353d15ca85ce404d769
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Componente dos Termos e condições

A **Termos e condições** componente refere-se a uma seção em um formulário que descreve os termos, as regras e as condições que os usuários devem concordar ou cumprir ao usar um serviço ou acessar conteúdo.

A variável **Termos e condições** é um componente composto que consiste em componentes Texto, Caixa de seleção e Link. O componente de texto contém um título e uma breve visão geral da finalidade e do escopo dos termos e condições. Também inclui uma caixa de seleção usada para obter o consentimento explícito do usuário. Você também pode substituir um texto de consentimento por links.

**Exemplo**

![termos e condições](/help/adaptive-forms/assets/terms-and-conditions.png)

Consulte [Subcomponentes do componente dos Termos e condições](#sub-component) para saber mais sobre os diferentes componentes do componente dos Termos e condições.

## Uso {#reasons-to-use-termsandconditions}

- **Contrato do Usuário**: o componente serve como um contrato entre o provedor de serviços e o usuário. Os usuários devem reconhecer e concordar com os termos antes de acessar o serviço ou conteúdo.

- **Conformidade legal**: garante a conformidade legal e a proteção ao provedor de serviços, descrevendo os direitos, as responsabilidades e as responsabilidades de ambas as partes.

- **Processos de registro**: Os formulários de registro ou inscrição incluem o **Termos e condições** componente, exigindo que os usuários concordem explicitamente com os termos antes de criar uma conta ou usar um serviço.

- **Transações de comércio eletrônico**: os sites online incluem o **Termos e condições** para que os usuários concordem com os termos e condições como parte do processo de finalização antes de fazer compras online.

- **Contratos de segurança e privacidade**: A variável **Termos e condições** O componente inclui detalhes sobre como os dados do usuário são coletados, armazenados e usados, muitas vezes complementados por uma política de privacidade separada

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do grupo de caixas de seleção de Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do componente de Termos e condições para visitantes com a caixa de diálogo de configuração. Você também pode definir opções de termos e condições com facilidade para obter uma experiência perfeita para o usuário.

### Guia Básico

![Guia Básico](/help/adaptive-forms/assets/terms-and-conditions-basic-tab.png)

- **Nome**: O nome identifica exclusivamente o componente no editor de regras. Caracteres especiais e espaços não são permitidos nas strings de nome.

- **Título**: Com o Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Mostrar opção de aprovação** - Marque a opção para mostrar a caixa de seleção de consentimento usada para obter o consentimento explícito do usuário.

- **Mostrar como pop-up** - Selecione a opção para exibir o componente de termos e condições em uma janela pop-up.

- **Substituir texto de consentimento por link(s) da Web**: selecione a opção para substituir um texto de consentimento por um link da Web.  Se a opção estiver desmarcada, o texto de consentimento será exibido por padrão.

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
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Conteúdo de ajuda {#help-content-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/terms-and-conditions-help-tab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade

![Guia Acessibilidade](/help/adaptive-forms/assets/terms-and-conditions-accessibility-tab.png)

**Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar estilos CSS para o componente de Termos e condições.


### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal dos Termos e condições adaptáveis do Forms é compatível com o AEM [Sistema de Estilos](/help/get-started/authoring.md#component-styling).

![Caixa de diálogo de design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o Componente principal do grupo de caixas de seleção de Formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades Personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de valores chave) a um componente principal do formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Ela permite criar um comportamento de formulário dinâmico que se adapta com base nos valores de atributos personalizados. Por exemplo, os desenvolvedores podem projetar várias representações de um componente headless do Forms para plataformas móveis, de desktop ou da Web, melhorando significativamente a experiência do usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: Você pode fornecer um nome para identificar o grupo de propriedades personalizadas. Você pode adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Depois de adicionar o grupo de propriedades personalizadas, você pode ver as seguintes opções:

   - **Pares de valor-chave**: É possível adicionar vários nomes de propriedades personalizadas e valores de propriedades personalizadas clicando no **Adicionar** para cada grupo de propriedades personalizadas.

   - **Excluir**: Toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: Toque ou clique e arraste para reorganizar a ordem do nome e do valor da propriedade personalizada.

## Subcomponentes do componente dos Termos e condições {#sub-component}

**Termos e condições** componente é um componente composto que inclui os seguintes subcomponentes:
- [Vincular componente](#link)
- [Componente de texto](#text)
- [Componente da caixa de seleção](#checkbox)

### Vincular componente{#link}

Este componente substitui um texto de consentimento por um link da Web ou links. Ela é usada em um cenário no qual o usuário pretende oferecer referências a seções específicas, informações adicionais ou documentos externos. É possível personalizar facilmente a variável **Link** componente individualmente para visitantes com a caixa de diálogo de configuração.

#### Guia Básico

![Guia Básico](/help/adaptive-forms/assets/link-basic-tab.png)

- **Nome**: O nome identifica exclusivamente o componente no editor de regras. Caracteres especiais e espaços não são permitidos nas strings de nome.

- **Título**: Com o Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Ocultar Título**: Selecione a opção para ocultar o Título do componente.

- **Links** - Especifique o link e o texto de exibição correspondente que é usado no lugar do texto de consentimento. É possível adicionar vários links clicando no ícone **Adicionar** botão.

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

- **Marcar como elemento de formulário não vinculado**: selecione a opção para configurar um campo de formulário não vinculado a nenhum schema. Essa opção permite salvar dados sem atualizar a fonte de dados. Ela também permite manipular dados de forma personalizada, separada da integração de banco de dados padrão.

- **Ocultar componente**: Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

- **Desativar componente** - Selecione a opção para desativar ou bloquear o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

#### Guia Validação

![Guia Validação](/help/adaptive-forms/assets/link-validation-tab.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve fazer uma seleção antes de prosseguir com o envio de um formulário. Não é possível selecionar **Ocultar componente** ou **Desativar componente** na guia **Básico** quando essa opção estiver selecionada.

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

- **Mensagem de validação de script**: essa opção permite que inserir uma mensagem que será exibida se a validação do script falhar.

### Guia Conteúdo de ajuda {#helpcontent-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/link-help-tab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade

![Guia Acessibilidade](/help/adaptive-forms/assets/link-accessibilty-tab.png)

**Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

### Componente de texto {#text}

**Texto** exibe o conteúdo textual que fornece informações aos usuários. Esse componente inclui os termos e condições reais, o idioma legal ou qualquer outra informação textual relevante.

É possível personalizar facilmente a variável [Componente de texto](/help/adaptive-forms/components/text.md) individualmente para visitantes com a caixa de diálogo Configurar. Para definir opções de texto com facilidade para uma experiência perfeita do usuário, use o [caixa de diálogo de configuração do componente de texto](/help/adaptive-forms/components/text.md#configure-dialog).


### Componente da caixa de seleção {#checkbox}

Uma caixa de seleção é usada para obter consentimento ou confirmação do usuário. Ele serve como um indicador visual de que o usuário leu e concordou com os termos descritos. É obrigatório marcar a caixa de seleção para indicar o consentimento do usuário.

É possível personalizar facilmente a variável [Componente da caixa de seleção](/help/adaptive-forms/components/checkbox.md) individualmente para visitantes com a caixa de diálogo Configurar. Para definir as propriedades da caixa de seleção para uma experiência do usuário perfeita, use o [caixa de diálogo de configuração do componente caixa de seleção](/help/adaptive-forms/components/checkbox.md#configure-dialog).


## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}

