---
title: Componente principal adaptável do Forms - Caixa de seleção
description: Uso ou personalização do Componente principal da caixa de seleção Forms adaptável.
role: Architect, Developer, Admin, User
exl-id: c6ca4800-bd10-4aeb-957a-fb1780cf94f3
source-git-commit: f0b450ef93a32a56000c31d82bf92394c57b55f9
workflow-type: tm+mt
source-wordcount: '1708'
ht-degree: 53%

---

# Caixa de seleção {#checkbox-component}

Uma caixa de seleção é um elemento da interface gráfica do usuário geralmente usado em aplicativos de software e formulários para permitir que os usuários façam uma escolha binária entre duas opções: marcada (selecionada) ou desmarcada (desmarcada).

Normalmente, uma caixa de seleção é representada como um pequeno quadrado que pode ser ativado ou desativado ao clicar ou tocar nela. Quando uma caixa de seleção é marcada, ela exibe uma marca de seleção para mostrar que a opção ou o recurso associado está ativo ou ativado.

**Exemplo**

![grupo de caixas de seleção](/help/adaptive-forms/assets/checkbox-example.png)

## Uso {#reasons-to-use-checkbox}

Os motivos comuns para usar a caixa de seleção em um Formulário adaptável são:

- **Facilidade de uso**: As caixas de seleção são visualmente claras e fornecem uma maneira simples de fazer escolhas binárias. Eles são intuitivos e fáceis de entender, tornando-os fáceis de usar.

- **Consentimento e Contrato**: as caixas de seleção são usadas para obter o consentimento do usuário para vários propósitos, por exemplo, aceitar termos e condições, assinar boletins informativos ou confirmar a verificação de idade. Eles deixam claro que o usuário está concordando ativamente com algo.

- **Confirmação visual**: as caixas de seleção marcadas fornecem uma confirmação visual aos usuários de que a seleção foi registrada. Esse feedback ajuda a evitar erros do usuário e garante que ele saiba que suas escolhas foram registradas.

- **Prevenção de erros**: as caixas de seleção reduzem a probabilidade de erros, permitindo que os usuários revisem e confirmem as opções antes do envio do formulário.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal da caixa de seleção do Forms adaptável foi lançado em fevereiro de 2023 como parte dos componentes principais 2.0.4. Esta tabela mostra todas as versões compatíveis, a compatibilidade com o AEM e os links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível com a <br>[versão 2.0.4](/help/versions.md) e posteriores | Compatível | Compatível |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal da caixa de seleção Forms adaptável na documentação técnica sobre [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkbox/v1/checkbox). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência da Caixa de seleção para visitantes com a Caixa de diálogo de configuração. Você também pode definir opções de Caixa de seleção com facilidade para obter uma experiência perfeita para o usuário.

![Guia Básico](/help/adaptive-forms/assets/checkbox-basic.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título** - Com seu Título, você pode identificar facilmente um componente em um formulário e, por padrão, o título aparece ao lado do componente. Se você não adicionar um título, o componente não será exibido.

- **Ocultar Título**: Selecione a opção para ocultar o Título do componente.

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

- **Marcar como elemento de formulário não vinculado**: selecione a opção para configurar um campo de formulário não vinculado a nenhum schema. Essa opção permite salvar dados sem atualizar a fonte de dados. Ela também permite manipular dados de forma personalizada, separada da integração de banco de dados padrão.

- **Tipo de dados do valor enviado**: esta opção especifica o tipo de dados do valor enviado quando qualquer opção é selecionada. Se o **tipo de dados do valor enviado** estiver definido como `Number` e você adicionar uma string de dados em **Valor de dados** na guia **Opções**, a tela exibirá uma mensagem de erro `Value type mismatch`.

- **Ocultar componente**: Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

- **Desativar componente** - Selecione a opção para desativar ou bloquear o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Quando Marcado, retornar o valor** -Selecione esta opção para especificar qual valor deve ser associado à caixa de seleção quando ela estiver marcada ou selecionada. É a ação que ocorre quando você marca ou marca a caixa de seleção.
- **Habilitar desmarcação.**- Selecione a opção para ativar ou desativar a capacidade de desmarcar uma caixa de seleção que foi marcada anteriormente.
   - Se **Habilitar Desmarcar** estiver ativado ou definido como true, significa que o usuário pode marcar e desmarcar a caixa de seleção a seu critério. Eles podem ativar e desativar a caixa de seleção conforme necessário.

   - Se **Habilitar Desmarcar** estiver desativado ou definido como falso, significa que, uma vez marcada a caixa de seleção, o usuário não poderá desmarcá-la.
- **Quando Desmarcado, retorna o valor** - A opção permite especificar qual valor deve ser associado à caixa de seleção quando estiver em um estado desmarcado ou desmarcado.

- **Valor padrão**: essa opção permite adicionar um valor padrão em um campo de formulário. Se o **Componente desativado** ou o **Componente de somente leitura** for selecionado, o valor padrão será exibido na tela. Se nenhum valor for inserido pelo usuário no campo de formulário, esse será o valor enviado no momento do envio do formulário.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/checkbox-validation.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve fazer uma seleção antes de prosseguir com o envio de um formulário. Não é possível selecionar **Ocultar componente** ou **Desativar componente** na guia **Básico** quando essa opção estiver selecionada.

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

- **Mensagem de validação de script**: essa opção permite que inserir uma mensagem que será exibida se a validação do script falhar.

### Guia Conteúdo de ajuda {#helpcontent-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/checkbox-help.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/checkbox-accessibility.png)

**Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar estilos CSS para o componente Caixa de seleção.

### Guia Estilos {#styles-tab}

O componente principal da caixa de seleção Forms adaptável é compatível com AEM [Sistema de Estilos](/help/get-started/authoring.md#component-styling).

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
