---
title: Componente principal de Formulários adaptáveis - botão Redefinir
description: Utilização ou personalização do Componente principal do botão Redefinir de Formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: e5aa9d89-aece-491e-80a1-7fb9ea6c4b60
source-git-commit: e0ed415bd7f45fdca6fbbb8ba409604d9e82a647
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Redefinir {#reset-button}

Um botão de redefinição em um Formulário adaptável é um botão que permite que os usuários limpem ou redefinam todos os campos do formulário para seus valores padrão. Ao clicar no botão redefinir, os dados inseridos nos campos do formulário são excluídos e os campos retornam ao seu estado original. O botão redefinir é normalmente usado como uma alternativa ao botão Enviar e fornece uma maneira de os usuários recomeçarem se inserirem dados incorretos ou indesejados no formulário.

![exemplo](/help/adaptive-forms/assets/example-reset.png)

## Uso {#reasons-to-use-reset-button}

Os motivos para usar um botão redefinir em um Formulário adaptável são:

- **Praticidade para o usuário**: o botão redefinir fornece uma maneira rápida e fácil para os usuários limparem o formulário e recomeçarem, sem precisar excluir manualmente cada campo.

- **Melhor usabilidade**: o botão redefinir pode melhorar a experiência do usuário, permitindo que os usuários corrijam erros ou alterem as informações com facilidade.

- **Prevenção de erros**: ao usar o botão redefinir, os usuários podem evitar o envio acidental de dados incorretos, o que pode gerar erros ou problemas de processamento.

- **Consistência**: a inclusão de um botão redefinir em um formulário oferece consistência na experiência do usuário, já que os botões de redefinição são um recurso comum dos formulários.

- **Melhor gerenciamento de dados**: ao usar o botão redefinir, os dados do formulário podem ser mantidos organizados e precisos, pois os usuários têm menos probabilidade de enviar dados inconsistentes ou incorretos.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do botão Redefinir dos Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Para mais informações sobre o desenvolvimento dos Componentes principais, consulte a [Documentação do desenvolvedor dos componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do botão Redefinir para visitantes com a caixa de diálogo Configurar. Você também pode definir as opções do botão Redefinir com facilidade para proporcionar uma experiência do usuário contínua.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/button_basictab.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.
- **Marcar como elemento de formulário não vinculado**: selecione a opção para configurar um campo de formulário não vinculado a nenhum schema. Essa opção permite salvar dados sem atualizar a fonte de dados. Ela também permite manipular dados de forma personalizada, separada da integração de banco de dados padrão.

- **Ocultar componente**: Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Conteúdo de ajuda {#help-content}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/button_helptab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/button_accessibilitytab.png)


**Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de Design {#design-dialog}

A caixa de diálogo de Design é usada para definir e gerenciar os estilos CSS para o componente do botão Redefinir.


### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal do botão Redefinir de formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

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

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}