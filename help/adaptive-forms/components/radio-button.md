---
title: Componente principal de Formulários adaptáveis - Botão de opção
description: Uso ou personalização do Componente principal de botão de opção dos Formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 86b5e9ec-58ac-4cd5-9c7c-4269247ec34f
source-git-commit: e843ccf5c030cd4f1015e3290347b5799828537a
workflow-type: ht
source-wordcount: '2079'
ht-degree: 100%

---

# Botão de opção {#radio-button-adaptive-forms-core-component}

<span class="preview"> Este artigo tem conteúdo sobre os recursos **Permitir rich text para título** e **Permitir rich text para opções**, recursos de pré-lançamento. O recurso de pré-lançamento pode ser acessado somente por meio do [canal de pré-lançamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=pt-BR#new-features).</span>

Um botão de opção em um Formulário adaptável é um tipo de elemento de entrada que permite ao usuário selecionar uma opção de um grupo de opções relacionadas. Ele é representado por um pequeno botão circular que pode estar preenchido ou vazio para indicar se a opção está selecionada ou não. Quando um usuário seleciona um botão de opção, os outros no grupo ficam desmarcados. Normalmente, os botões de opção são usados quando há várias opções mutuamente exclusivas e apenas uma pode ser selecionada de cada vez.

**Exemplo**

![exemplo](/help/adaptive-forms/assets/radio-button.png)

**Caixa de diálogo Propriedades**

![exemplo](/help/adaptive-forms/assets/radio-button-properties.png)

Neste exemplo, o elemento Opções é usado para agrupar os botões de opção. O elemento **Texto de exibição** é usado para fornecer um rótulo para um item e **Valor de dados** é usado para especificar o valor enviado para o servidor após o envio do formulário.

Cada opção de botão de opção tem um valor de dados exclusivo e um atributo Exibir texto. Se um usuário selecionar a opção “1-10”, o valor de dados correspondente será enviado para o servidor quando o formulário for enviado. Esses dados podem então ser processados por um script do lado do servidor para determinar quais opções foram selecionadas pelo usuário, e podem ser usados para executar várias ações, como atualizar outros campos no formulário ou enviar os dados do formulário para um script do lado do servidor para processamento adicional.

Além disso, cada botão de opção pode ser configurado para ter valores de processamento diferentes para cada opção, e isso pode ser definido usando o editor de regras de Formulários adaptáveis

## Uso {#reasons-to-use-radio-button}

Há vários motivos para usar botões de opção em um formulário, incluindo:

- **Opções limitadas**: os botões de opção são usados para fornecer uma lista de opções predefinidas para o usuário escolher, e apenas uma opção pode ser selecionada de cada vez. Isso é útil quando o número de opções é limitado e mutuamente exclusivo.

- **Representação clara**: botões de opção são claros e fáceis de entender, simplificando o processo de seleção para os usuários.

- **Consistência**: o uso de botões de opção garante uma maneira consistente e padronizada de apresentar opções aos usuários, facilitando sua compreensão e interação com o formulário.

- **Mais fácil de usar**: os botões de opção são fáceis de usar, especialmente para usuários não familiarizados com tecnologia ou com mobilidade limitada.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de botão de opção dos Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/radiobutton/v1/radiobutton). Para obter mais informações sobre o desenvolvimento dos componentes principais, consulte a [documentação do desenvolvedor dos componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência dos botões de opção para visitantes com a caixa de diálogo Configurar. Você também pode definir as opções dos botões de opção com facilidade para oferecer uma experiência do usuário contínua.

![Guia Básico](/help/adaptive-forms/assets/radiobutton_basictab.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.
- **Permitir rich text para título**: esse recurso permite formatar títulos de texto simples, incorporando recursos como negrito, itálico, texto sublinhado, várias fontes, tamanhos de fonte, cores e uma opção adicional para aprimorar a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção **Permitir rich text para título**, as opções de formatação se tornam visíveis para estilizar o título do componente. Para acessar todas as opções de formatação disponíveis, clique no ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: selecione essa opção para ocultar o título do componente.

- **Opções**: você pode adicionar pares de valores de dados e textos de exibição usando o botão **Adicionar**. \
  Depois que uma nova opção for adicionada, as seguintes ações poderão ser executadas:
   - **Valor de dados**: essa opção permite inserir o conteúdo a ser enviado quando uma opção for selecionada.
   - **Texto de exibição**: essa opção permite inserir o conteúdo a ser exibido em um Formulário adaptável.
   - **Excluir**: toque ou clique para excluir a opção de um botão de opção.
   - **Reorganizar**: toque ou clique e arraste para reorganizar a ordem das opções.
Você também pode formatar as opções do grupo de botões de opção usando **Permitir rich text para opções**.

  ![Suporte a rich text para opções](/help/adaptive-forms/assets/richtext-for-options.png)

  Depois de marcar a caixa de seleção **Permitir rich text para opções**, as opções de formatação se tornam visíveis para estilizar as opções do componente. Para acessar todas as opções de formatação disponíveis, clique no `Fullscreen` ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text para opções](/help/adaptive-forms/assets/richtextoptions-support.png)

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.

- **Tipo de dados do valor enviado**: essa opção especifica o tipo de dados do valor enviado quando qualquer opção é selecionada. Se o **tipo de dados do valor enviado** estiver definido como `Number` e você adicionar uma string de dados em **Valor de dados** na guia **Opções**, a tela exibirá uma mensagem de erro `Value type mismatch`.

- **Opção padrão**: essa opção permite adicionar valores padrão pré-selecionados quando o formulário for carregado. Se o **tipo de dados do valor enviado** estiver definido como `Number` e você adicionar uma string de dados em **Opções padrão**, a tela exibirá uma mensagem de erro de `Value type mismatch`.

- **Opções de exibição**: essa opção é usada para definir o alinhamento visual dos botões de opção em um Formulário adaptável. As duas opções compatíveis são:
   - **Horizontal**: quando essa opção for selecionada, os botões de opção serão exibidos da esquerda para a direita em um Formulário adaptável.
   - **Vertical**: quando essa opção for selecionada, os botões de opção serão exibidos de cima para baixo em um Formulário adaptável.
- **Ocultar componente**: selecione essa opção para ocultar o componente no formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/radiobutton_validationtab.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve fazer uma seleção antes de prosseguir com o envio de formulário. Não é possível selecionar **Ocultar componente** ou **Desativar componente** na guia **Básico** quando essa opção estiver selecionada.
- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

- **Mensagem de validação de script**: essa opção permite que inserir uma mensagem que será exibida se a validação do script falhar.

### Guia Conteúdo de ajuda {#helpcontent-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/radiobutton_helptab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/radiobutton_accessibilitytab.png)

**Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de Design é usada para definir e gerenciar estilos CSS para o componente de botão de opção.


### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de Botão de opção dos formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes padrão do CSS**: é possível fornecer uma classe padrão do CSS ao componente principal de botão de opção para formulários adaptáveis.

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
