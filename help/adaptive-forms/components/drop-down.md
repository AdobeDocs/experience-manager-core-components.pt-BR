---
title: 'Componente principal de Formulários adaptáveis: Lista suspensa'
description: Uso ou personalização do Componente principal Lista suspensa de Formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 9d59d0d2-d38f-4ed5-8b43-984c45f26f27
source-git-commit: e843ccf5c030cd4f1015e3290347b5799828537a
workflow-type: tm+mt
source-wordcount: '2125'
ht-degree: 92%

---

# Lista suspensa {#drop-down-list-adaptive-forms-core-component}

<span class="preview"> Este artigo contém conteúdo sobre o **Permitir Rich Text para Título** recurso, um recurso de pré-lançamento do. O recurso de pré-lançamento pode ser acessado somente por meio de [canal de pré-lançamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

Uma lista suspensa em um Formulário adaptável permite que os usuários selecionem uma ou mais opções de uma lista de opções predefinidas. As opções podem ser do tipo string, número ou booleano. Além disso, o componente de lista suspensa pode ser configurado para ter validação diferente e valores padrão.

**Exemplo**
![exemplo](/help/adaptive-forms/assets/drop-down-list.png)

## Uso {#reasons-to-use-drop-down-list}

Há vários motivos pelos quais é benéfico incluir uma lista suspensa em um Formulário adaptável, incluindo:

- **Lista longa de opções**: listas suspensas são úteis para situações em que há uma longa lista de opções disponíveis para um campo. Elas ocupam menos espaço no formulário do que uma lista de botões de opção ou caixas de seleção e podem ser mais simples para os usuários.

- **Consistência**: as listas suspensas fornecem consistência no design e no layout do formulário, tornando mais intuitivo e fácil para os usuários navegarem.

- **Clareza**: listas suspensas podem tornar o formulário mais claro e fácil de entender, fornecendo uma lista clara e concisa de opções.

- **Experiência do usuário**: listas suspensas podem ser usadas para tornar o formulário mais fácil de usar, fornecendo uma maneira clara e intuitiva para os usuários selecionarem opções.

- **Análise de dados**: listas suspensas podem ser usadas para coletar dados de várias fontes e analisá-los, ou usá-los como entrada para processamento adicional.

**Caixa de diálogo Propriedades**

![Caixa de diálogo Propriedades](/help/adaptive-forms/assets/drop-down-list-properties.png)

Neste exemplo, o elemento Opções é usado para definir os itens da lista. O elemento **Texto exibido** é usado para fornecer um rótulo para itens da lista e o **Valor de dados** é usado para especificar o valor que é enviado para o servidor quando o formulário é enviado.

Cada opção da lista suspensa tem um atributo valor de dados e um atributo de texto exibido exclusivos. Se um usuário selecionar a opção “Vermelho”, o valor de dados correspondente será enviado para o servidor quando o formulário for enviado. Esses dados podem então ser processados por um script do lado do servidor para determinar quais opções foram selecionadas pelo usuário, e podem ser usados para executar várias ações, como atualizar outros campos no formulário ou enviar os dados do formulário para um script do lado do servidor para processamento adicional.

Além disso, a lista suspensa pode ser configurada para ter valores de processamento diferentes para cada opção, e isso pode ser definido usando o Editor de regras de Formulários adaptáveis.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de Lista suspensa de Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/dropdown/v1/dropdown). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de lista suspensa para visitantes com a caixa de diálogo Configurar. Você também pode definir opções de lista suspensa com facilidade para uma experiência do usuário perfeita.

![Guia Básico](/help/adaptive-forms/assets/dropdown_basictab.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.
- **Permitir Rich Text para Título** - Esse recurso permite que os usuários formatem títulos de texto simples, incorporando recursos como negrito, itálico, texto sublinhado, várias fontes, tamanhos de fonte, cores e opção adicional para aprimorar a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção para **Permitir Rich Text para Título** , as opções de formatação se tornam visíveis para estilizar o título do componente. Para acessar todas as opções de formatação disponíveis, clique no botão ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png) guia.

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar Título**: selecione essa opção para ocultar o Título do componente.

- **Permitir seleção múltipla**: selecione essa opção para tornar possível selecionar várias opções na lista suspensa.
- **Salvar valor como**: essa opção especifica o tipo de dados do valor enviado quando qualquer opção é selecionada. Se **Salvar valor como** estiver definido como `Number` e você adicionar dados de string ao **Valor de dados** na guia **Opções**, a tela exibirá uma mensagem de erro de `Value type mismatch`.

  Na guia **Opções**, é possível adicionar pares de valores de dados e textos exibidos usando o botão **Adicionar**. Uma vez que uma nova opção for adicionada, as seguintes ações serão executadas:

   - **Valor dos dados**: essa opção permite definir o conteúdo que vai ser enviado quando a opção for selecionada.
   - **Texto exibido**: essa opção permite definir o conteúdo que vai ser exibido no Formulário adaptável.
   - **Excluir**: toque ou clique nesse botão para excluir a opção do menu suspenso.
   - **Reorganizar**: toque ou clique nesse botão e em seguida arraste as opções do menu suspenso para reorganizar a sua ordem.

- **Opção padrão** - Essa opção permite adicionar valores padrão. Use o ícone de excluir para remover a opção adicionada. Se **Salvar valor como** estiver definido como `Number` e você adicionar dados de string às **Opções padrão**, a tela exibirá uma mensagem de erro de `Value type mismatch`.

- **Texto de espaço reservado**: o texto de espaço reservado em um componente de formulário refere-se a um rótulo curto ou exemplo que aparece em um campo de entrada como uma dica para o usuário sobre que tipo de informação deve ser inserida nesse campo. O texto de espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não age como um rótulo ou valor permanente para o campo.

- **Opções** - É possível adicionar valores de dados e exibir pares de texto usando o **Adicionar** botão.  Depois que uma nova opção é adicionada, as seguintes ações podem ser executadas:
   - **Valor de dados**: essa opção permite inserir o conteúdo a ser enviado quando uma opção for selecionada.
   - **Texto de exibição** - Esta opção permite inserir o conteúdo a ser exibido em um Formulário adaptável.
   - **Excluir** - Toque ou clique para excluir a opção de uma caixa de seleção.
   - **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem dos painéis.

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.
- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.

- **Ocultar componente**: Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/dropdown_validationtab.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve fazer uma seleção antes de prosseguir com o envio de formulário. Não é possível selecionar **Ocultar componente** ou **Desativar componente** na guia **Básico** quando essa opção estiver selecionada.

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

- **Mensagem de validação de script**: essa opção permite que inserir uma mensagem que será exibida se a validação do script falhar.

### Guia Conteúdo de ajuda {#help-content-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/dropdown_helptab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/dropdown_accessibilitytab.png)


**Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.


## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente Lista suspensa.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de Lista suspensa dos formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes padrão do CSS**: você pode fornecer uma classe padrão do CSS ao componente principal lista suspensa para formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de chave e valor) a um componente principal de formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: toque ou clique e arraste para alterar a ordem do nome e do valor da propriedade personalizada.

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}
