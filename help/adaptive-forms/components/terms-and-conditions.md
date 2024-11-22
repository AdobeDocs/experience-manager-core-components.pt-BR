---
title: Componente principal de formulários adaptáveis - Termos e condições
description: Uso ou personalização do componente principal Termos e condições para formulários adaptáveis
role: Architect, Developer, Admin, User
exl-id: c607d554-ad2d-4434-856d-91e174ef3149
source-git-commit: 732efc9ed450aa31078ecaad65c0c306679fe97e
workflow-type: tm+mt
source-wordcount: '3256'
ht-degree: 98%

---

# Componente de Termos e condições

Um componente de **Termos e condições** refere-se a uma seção de um formulário que descreve os termos, regras e condições com os quais os usuários devem concordar ou aderir ao usar um serviço ou acessar conteúdo.

O componente de **Termos e condições** é composto por outros componentes, como: Texto, Caixa de seleção e Link. O componente de texto contém um título e uma breve visão geral da finalidade e do escopo dos termos e condições. Também é utilizada uma caixa de seleção para obter o consentimento explícito do usuário. Além disso, é possível substituir um texto de consentimento por links.

>[!NOTE]
>
> Para o AEM 6.5 Forms, esse componente foi introduzido com o Pacote de serviços 19 do AEM 6.5 Forms (6.5.19.0). Para habilitar esse componente, verifique se as versões necessárias dos Componentes principais do Forms e do WCM estão instaladas. Para obter informações detalhadas sobre as versões dos Componentes principais de formulários adaptáveis, consulte [Versões dos Componentes principais de formulários adaptáveis](/help/adaptive-forms/version.md)

**Exemplo**

![termos e condições](/help/adaptive-forms/assets/terms-and-conditions.png)

Consulte a seção [Subcomponentes do componente de Termos e condições](#sub-component) para saber mais sobre os diferentes componentes que integram os Termos e condições.

## Uso {#reasons-to-use-termsandconditions}

- **Contrato do usuário**: esse componente serve como um contrato entre o provedor de serviços e o usuário. Os usuários e usuárias devem reconhecer e concordar com os termos antes de acessar o serviço ou conteúdo.

- **Conformidade legal**: garante proteção e conformidade legal ao provedor de serviços, descrevendo os direitos, responsabilidades e obrigações de ambas as partes.

- **Processos de registro**: os formulários de registro ou inscrição incluem o componente de **Termos e condições**, o qual exige que os usuários concordem explicitamente com os termos antes de criar uma conta ou usar um serviço.

- **Transações de comércio eletrônico**: os sites incluem o componente de **Termos e condições** para que usuários sejam solicitados a concordar com os termos e condições durante o processo de finalização de compras online.

- **Contratos de segurança e privacidade**: o componente de **Termos e condições** inclui detalhes sobre como os dados do usuário são coletados, armazenados e usados, o que geralmente é complementado por uma política de privacidade separada

## Versão e compatibilidade {#version-and-compatibility}

O componente principal dos Termos e condições adaptáveis do Forms foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.62 para Cloud Service e Componentes principais 1.1.28 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.62](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.28](/help/adaptive-forms/version.md) e posteriores que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal termos e condições para formulários adaptáveis na documentação técnica, encontrada no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

É possível personalizar facilmente a experiência do componente de termos e condições para visitantes por meio da caixa de diálogo Configurar. Também é possível definir opções de termos e condições com facilidade para uma experiência de usuário perfeita.

### Guia Básico

![Guia Básico](/help/adaptive-forms/assets/terms-and-conditions-basic-tab.png)

- **Nome**: O nome identifica exclusivamente o componente no editor de regras. Caracteres especiais e espaços não são permitidos nas strings de nome.

- **Título**: o título permite identificar facilmente um componente em um formulário; por padrão, ele aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.
- **Permitir rich text para título**: esse recurso permite formatar títulos de texto simples, incorporando recursos como negrito, itálico, texto sublinhado, várias fontes, tamanhos de fonte, cores e uma opção adicional para aprimorar a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção **Permitir rich text para título**, as opções de formatação se tornam visíveis para estilizar o título do componente. Para acessar todas as opções de formatação disponíveis, clique no ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Mostrar opção de aprovação**: selecione essa opção para mostrar a caixa de seleção usada para obter o consentimento explícito do usuário.

- **Mostrar como pop-up**: selecione essa opção para exibir o componente de termos e condições em uma janela pop-up.

- **Substituir texto de consentimento por um link da web**: selecione essa opção para substituir um texto de consentimento por um link da web.  Se a opção estiver desmarcada, o texto de consentimento será exibido por padrão.

- **Ocultar título**: selecione essa opção para ocultar o título do componente.

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

- **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.
   - **Texto personalizado**: selecione essa opção para usar o texto personalizado para rótulos de acessibilidade ARIA. Selecionar essa opção exibe a caixa de diálogo Texto personalizado. Você pode adicionar informações relevantes na caixa de diálogo Texto personalizado.
   - **Descrição**: selecione essa opção para usar a descrição para rótulos de acessibilidade ARIA.
   - **Título**: selecione essa opção para usar o título para rótulos de acessibilidade ARIA.
   - **Nome**: selecione essa opção para usar o nome para rótulos de acessibilidade ARIA.
   - **Nenhum**: selecione essa opção se não quiser adicionar nada aos rótulos de acessibilidade ARIA.
- **Função de HTML para anúncio do leitor de tela**: a função HTML é um atributo usado para especificar a finalidade de um elemento HTML para tecnologias assistivas, como leitores de tela. O atributo de função é usado para fornecer contexto e significado semântico adicionais a um elemento, facilitando a interpretação e o anúncio do conteúdo pelos leitores de tela. Por exemplo, no AEM Forms, o rótulo de um campo de formulário pode ter a função de “rótulo” e seu campo de entrada pode ter a função de “caixa de texto”. Isso ajuda o leitor de tela a entender a relação entre o rótulo e o campo de entrada e anunciá-los corretamente ao usuário.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar estilos CSS do componente de Termos e condições.


### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de Termos e condições para formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes padrão do CSS**: você pode fornecer uma classe padrão do CSS ao componente principal termos e condições para formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de chave e valor) a um componente principal de formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: toque ou clique e arraste para alterar a ordem do nome e do valor da propriedade personalizada.

## Subcomponentes do componente de Termos e condições {#sub-component}

O componente de **Termos e condições** é composto pelos seguintes subcomponentes:
- [Componente de link](#link)
- [Componente de texto](#text)
- [Componente de caixa de seleção](#checkbox)

### Componente de link{#link}

Este componente substitui um texto de consentimento por um ou mais links da web. Isso é usado em um cenário no qual o usuário pretende apresentar referências a seções específicas, informações adicionais ou documentos externos. É possível personalizar facilmente o componente de **link** de maneira individual para visitantes com a caixa de diálogo Configurar.

#### Guia Básico

![Guia Básico](/help/adaptive-forms/assets/link-basic-tab.png)

- **Nome**: O nome identifica exclusivamente o componente no editor de regras. Caracteres especiais e espaços não são permitidos nas strings de nome.

- **Título**: o título permite identificar facilmente um componente em um formulário; por padrão, ele aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.
- **Permitir rich text para título**: esse recurso permite formatar títulos usando opções como negrito, itálico, estilos de fonte, cores e alinhamento, aprimorando a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção **Permitir rich text para título**, as opções de formatação se tornam visíveis para estilizar o título do componente. Para acessar todas as opções de formatação disponíveis, clique no ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: selecione essa opção para ocultar o título do componente.

- **Links**: especifique o link e o texto de exibição correspondente que será usado no lugar do texto de consentimento. É possível adicionar vários links clicando no botão **Adicionar**.
Depois que uma nova opção for adicionada, as seguintes ações poderão ser executadas:
   - **Link**: essa opção permite inserir o URL para redirecionar quando uma opção for selecionada.
   - **Texto de exibição**: essa opção permite inserir o conteúdo a ser exibido em um Formulário adaptável.
   - **Excluir**: toque ou clique para excluir a opção de um botão de opção.
   - **Reorganizar**: toque ou clique e arraste para reorganizar a ordem das opções.

  Você também pode formatar as opções para o grupo de caixas de seleção usando **Permitir rich text para opções**. Depois de marcar a caixa de seleção **Permitir rich text para opções**, as opções de formatação se tornam visíveis para estilizar as opções do componente. Para acessar todas as opções de formatação disponíveis, clique no `Fullscreen` ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text para opções](/help/adaptive-forms/assets/link-options.png)

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.
- **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

- **Desabilitar componente**: selecione essa opção para desabilitar ou bloquear o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

#### Guia Validação

![Guia Validação](/help/adaptive-forms/assets/link-validation-tab.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve fazer uma seleção antes de prosseguir com o envio de formulário. Não é possível selecionar **Ocultar componente** ou **Desativar componente** na guia **Básico** quando essa opção estiver selecionada.

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

- **Mensagem de validação de script**: essa opção permite que inserir uma mensagem que será exibida se a validação do script falhar.

### Guia Conteúdo de ajuda {#helpcontent-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/link-help-tab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade

![Guia Acessibilidade](/help/adaptive-forms/assets/link-accessibilty-tab.png)

- **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.
   - **Texto personalizado**: selecione essa opção para usar o texto personalizado para rótulos de acessibilidade ARIA. Selecionar essa opção exibe a caixa de diálogo Texto personalizado. Você pode adicionar informações relevantes na caixa de diálogo Texto personalizado.
   - **Descrição**: selecione essa opção para usar a descrição para rótulos de acessibilidade ARIA.
   - **Título**: selecione essa opção para usar o título para rótulos de acessibilidade ARIA.
   - **Nome**: selecione essa opção para usar o nome para rótulos de acessibilidade ARIA.
   - **Nenhum**: selecione essa opção se não quiser adicionar nada aos rótulos de acessibilidade ARIA.

### Componente de texto {#text}

O componente de **texto** exibe o conteúdo textual que fornece informações a usuários. Esse componente inclui os termos e condições reais, o idioma legal ou qualquer outra informação textual relevante.

É possível personalizar facilmente o [componente de texto](/help/adaptive-forms/components/text.md) de maneira individual para visitantes com a caixa de diálogo Configurar. Para definir opções de texto com facilidade e obter uma experiência de usuário perfeita, use a [caixa de diálogo Configurar do componente de texto](/help/adaptive-forms/components/text.md#configure-dialog).


### Componente de caixa de seleção {#checkbox}

A caixa de seleção é usada para obter o consentimento ou reconhecimento do usuário. Ela serve como um indicador visual de que o usuário leu e concordou com os termos descritos. É obrigatório marcar a caixa de seleção para indicar o consentimento.

É possível personalizar facilmente o [componente de caixa de seleção](/help/adaptive-forms/components/checkbox.md) de maneira individual para visitantes com a caixa de diálogo Configurar. Para definir as propriedades da caixa de seleção e obter uma experiência de usuário perfeita, use a [caixa de diálogo Configurar do componente de caixa de seleção](/help/adaptive-forms/components/checkbox.md#configure-dialog).


## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}
