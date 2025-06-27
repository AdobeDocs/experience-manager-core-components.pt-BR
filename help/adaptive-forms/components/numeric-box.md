---
title: Componente principal dos Formulários adaptáveis - Entrada de número
description: Utilização ou personalização do Componente principal de entrada de número dos Formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 75604ecf-1ec5-4e97-b934-d6ed49726147
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '2282'
ht-degree: 100%

---


# Componente Caixa numérica{#number-input-adaptive-forms-core-component}

Um componente Caixa numérica em um formulário adaptável é um tipo de campo de formulário que permite aos usuários inserir valores numéricos. Normalmente, o componente é representado por um campo de texto com uma seta para cima e para baixo para aumentar e diminuir o número.

Também pode ser usado com atributos como mín., máx., etapa, valor e muito mais. Esses atributos podem ser usados para definir os valores mínimo e máximo permitidos no campo, o intervalo de etapas para aumentar ou diminuir o número e o valor padrão do campo.

Esse componente pode ser usado para coletar dados numéricos, como idade, quantidade e muito mais. Ele também pode ser usado para executar operações matemáticas, como adição e subtração. Esse componente também pode ser usado para validar os dados numéricos inseridos pelo usuário.

Para acessibilidade, é importante especificar o “rótulo” que descreve a finalidade do campo de entrada do número e o tipo de entrada esperado.

{{traditional-aem}}

**Exemplo**

![exemplo](/help/adaptive-forms/assets/numeric-stepper.png)

## Uso {#reasons-to-use-number-input-numeric-stepper}

Há vários motivos pelos quais é vantajoso incluir um componente de entrada numérica em um Formulário adaptável, incluindo:

- **Operações matemáticas**: campos numéricos podem ser usados para executar operações matemáticas, como adição, subtração, multiplicação e divisão.

- **Intervalo de dados**: campos numéricos podem ser usados para definir um intervalo de valores válidos por meio do uso de atributos de valor mínimo, máximo e de etapa.

- **Conteúdo dinâmico**: o componente numérico pode ser usado para exibir dados dinâmicos com base nos campos do formulário.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal de caixa de numérica de formulários adaptáveis foi lançado em fevereiro de 2023 como parte dos componentes principais 2.0.4 para serviços na nuvem e dos componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM Forms 6.5.16.0 ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_br). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de entrada de número dos Formulários adaptáveiss na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/numberinput/v1/numberinput). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência de entrada de números para visitantes com a caixa de diálogo Configurar. Você também pode definir opções de entrada de número com facilidade para proporcionar uma experiência do usuário contínua.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/numberinput_basictab.png)

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
- **Somente leitura** - Selecione a opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Tipo de número**: essa opção permite selecionar o tipo de valores numéricos permitidos no campo de formulário. Você pode selecionar os tipos Decimal ou Inteiro no menu suspenso.
- **Valor padrão**: essa opção permite adicionar um valor padrão a um campo de formulário. Se o **Componente desativado** ou o **Componente somente leitura** for selecionado, o valor padrão será exibido na tela. Se nenhum valor for inserido pelo usuário no campo de formulário, esse valor será enviado no momento do envio do formulário

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/numberinput_validationtab.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve inserir um valor antes de prosseguir com o envio de formulário. Não é possível selecionar as opções **Ocultar componente** ou **Desativar Componente** na guia **Básico** quando essa opção está selecionada.

- **Mensagem de erro**: essa opção permite que você insira uma mensagem que será exibida se uma caixa de seleção **Obrigatória** estiver marcada mas o campo ficar em branco.

- **Mensagem de validação de script**: essa opção permite inserir uma mensagem que será exibida se a validação do script falhar.

- **Número mais baixo / Menor número**: use essa opção para selecionar o número mínimo permitido a ser inserido no campo de formulário. Se o valor inserido no campo de formulário for menor que o número especificado na opção **Número mais baixo / Menor número**, a mensagem de erro será exibida.

- **Mensagem de erro de mínimo**: essa opção permite inserir uma mensagem de erro que será exibida quando o usuário inserir um valor menor que o especificado na opção **Número mínimo/Número mínimo**.

- **Excluir valor mínimo**: marque essa caixa de seleção se não quiser que o valor mínimo especificado na opção **Número mais baixo / Menor número** seja incluído no intervalo de valores que podem ser inseridos no campo de formulário.

- **Número mais alto / Maior número**: use essa opção para selecionar o número máximo que pode ser inserido no campo de formulário. Se o número inserido no campo de formulário for maior que o número especificado na opção **Número mais alto / Maior número**, a mensagem de erro será exibida.

- **Mensagem de erro de máximo**: essa opção permite inserir uma mensagem de erro que será exibida quando o usuário inserir um valor maior que o especificado na opção **Número mais alto / Maior número**.

- **Excluir valor máximo**: marque essa caixa de seleção se não quiser que o valor máximo especificado na opção **Número mais alto / Maior número** seja incluído no intervalo de valores que podem ser inseridos no campo do formulário.

### Guia Conteúdo de ajuda {#help-content}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/numberinput_helptab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/numberinput_accessibility.png)

- **Texto para leitores de tela**: isso se refere ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por pessoas com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.
   - **Texto personalizado**: selecione essa opção para usar o texto personalizado para rótulos de acessibilidade ARIA. Selecionar essa opção exibe a caixa de diálogo Texto personalizado. Você pode adicionar informações relevantes na caixa de diálogo Texto personalizado.
   - **Descrição**: selecione essa opção para usar a descrição para rótulos de acessibilidade ARIA.
   - **Título**: selecione essa opção para usar o título para rótulos de acessibilidade ARIA.
   - **Nome**: selecione essa opção para usar o nome para rótulos de acessibilidade ARIA.
   - **Nenhum**: selecione essa opção se não quiser adicionar rótulos de acessibilidade ARIA.

### Guia Formatos {#formats-configure-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/numberinput_formattab.png)

- **Exibir formato**: isso permite selecionar opções de diferentes tipos de formatos inteiros-numéricos para exibição. Quando o usuário seleciona qualquer opção do menu suspenso **Tipo**, a opção **Formato** se torna visível no painel. É possível escolher um formato específico no qual os números serão exibidos para o usuário.
- **Idioma**: esse recurso é usado para formatar o campo específico. Quando um usuário seleciona qualquer opção de idioma no menu suspenso **Tipo**, a opção **Tag de idioma IETF BCP 47** aparece no painel. Você pode escolher o idioma para a formatação de campo ao traduzir um formulário adaptável para um idioma específico.

O conjunto de idiomas não está visível por padrão, mas os usuários podem inserir uma **Tag de idioma IETF BCP 47** personalizada atualizando a política do modelo:

1. Abra o modelo correspondente associado a um formulário adaptável no editor de modelo.
2. Selecione a política existente como `numberinput-default-policy` no menu suspenso.

   ![Política de modelo do seletor de data](/help/adaptive-forms/assets/numberinput-template-policy.png)

3. Clique em **Concluído**.

   >[!NOTE]
   >
   > Para obter mais informações sobre como traduzir um formulário adaptável para um idioma específico, [clique aqui](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).


## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar os estilos CSS do componente Caixa numérica.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de Entrada de número dos formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Guia Estilo](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o componente principal de caixa numérica de formulários adaptáveis.

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

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=pt-BR)

-->

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}
