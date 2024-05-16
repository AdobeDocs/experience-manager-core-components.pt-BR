---
title: Componente principal de formulários adaptáveis - Caixa de seleção
description: Uso ou personalização do componente principal de Caixa de seleção para formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: c6ca4800-bd10-4aeb-957a-fb1780cf94f3
source-git-commit: 58a0f0f2ef6d9dec3ce2436dad954a8a7aca188c
workflow-type: ht
source-wordcount: '1780'
ht-degree: 100%

---

# Componente Caixa de seleção{#checkbox-component}

<span class="preview"> Este artigo tem conteúdo sobre o recurso **Permitir Texto formatado para Título**, um recurso de pré-lançamento. O recurso de pré-lançamento pode ser acessado somente por meio do [canal de pré-lançamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=pt-BR#new-features).</span>

Uma caixa de seleção é um elemento gráfico da interface geralmente usado em aplicativos de software e formulários para permitir que usuários façam uma escolha binária entre duas opções: marcada (selecionada) ou desmarcada (não selecionada).

Normalmente, uma caixa de seleção é representada como um pequeno quadrado que pode ser ativado ou desativado pelo clique ou toque. Quando uma caixa de seleção é marcada, ela exibe uma marca de seleção para mostrar que a opção ou o recurso associado está ativo ou habilitado.

>[!NOTE]
>
> Para o AEM 6.5 Forms, esse componente foi introduzido com o Pacote de serviços 19 do AEM 6.5 Forms (6.5.19.0). Para habilitar esse componente, verifique se as versões necessárias dos Componentes principais do Forms e do WCM estão instaladas. Para obter informações detalhadas sobre as versões dos Componentes principais de formulários adaptáveis, consulte [Versões dos Componentes principais de formulários adaptáveis](/help/adaptive-forms/version.md)

**Exemplo**

![Grupo de caixas de seleção](/help/adaptive-forms/assets/checkbox-example.png)

## Uso {#reasons-to-use-checkbox}

Estes são alguns motivos comuns para se usar caixas de seleção em um formulário adaptável:

- **Facilidade de uso**: as caixas de seleção são de fácil identificação e fornecem uma maneira simples de fazer escolhas binárias. Elas são intuitivas e fáceis de entender e usar.

- **Consentimento e contrato**: as caixas de seleção são usadas para obter o consentimento do usuário para vários propósitos como, por exemplo, aceitar termos e condições, assinar informativos ou realizar uma verificação de idade. Elas deixam claro que a pessoa está concordando ativamente com o que foi apresentado.

- **Confirmação visual**: as caixas de seleção marcadas fornecem uma confirmação visual de que a seleção foi registrada. Esse feedback ajuda a evitar erros do usuário e garante que saibam que suas escolhas foram registradas.

- **Prevenção de erros**: as caixas de seleção reduzem a probabilidade de erros, permitindo que usuários revisem e confirmem as escolhas antes do envio do formulário.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Caixa de seleção para formulários adaptáveis foi lançado como parte dos Componentes principais 2.0.52. Esta tabela mostra todas as versões compatíveis, a compatibilidade com o AEM e inclui links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível com a <br>[versão 2.0.52](/help/adaptive-forms/version.md) e posteriores | Compatível | Compatível |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal de Caixa de seleção para formulários adaptáveis na documentação técnica, encontrada no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkbox/v1/checkbox). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência das caixas de seleção para visitantes com a caixa de diálogo Configurar. Também é possível definir opções de caixa de seleção com facilidade para uma experiência de usuário perfeita.

![Guia Básico](/help/adaptive-forms/assets/checkbox-basic.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: com o título, é possível identificar facilmente um componente em um formulário; por padrão, o título aparece ao lado do componente. Se você não adicionar um título, o componente não será exibido.

- **Permitir rich text para título**: esse recurso permite formatar títulos de texto simples, incorporando recursos como negrito, itálico, texto sublinhado, várias fontes, tamanhos de fonte, cores e uma opção adicional para aprimorar a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção **Permitir rich text para título**, as opções de formatação se tornam visíveis para estilizar o título do componente. Para acessar todas as opções de formatação disponíveis, clique no ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: selecione essa opção para ocultar o título do componente.

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.

- **Tipo de dados do valor enviado**: esta opção especifica o tipo de dados do valor enviado quando uma opção é selecionada. Se o **tipo de dados do valor enviado** estiver definido como `Number` e você adicionar uma string de dados em **Valor de dados** na guia **Opções**, a tela exibirá uma mensagem de erro `Value type mismatch`.

- **Ocultar componente**: Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

- **Desabilitar componente**: selecione essa opção para desabilitar ou bloquear o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
  <!-- - **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.-->
- **Quando marcada, retornar o valor**: selecione essa opção para especificar qual valor deve ser associado à caixa de seleção quando ela estiver marcada ou selecionada. Essa é a ação que ocorre quando você marca a caixa de seleção.
- **Preservar o valor do estado Desmarcar**: selecionar esta opção permite especificar o valor a ser retornado quando o componente de caixa de seleção não estiver selecionado. Se a opção **Preservar o valor do estado Desmarcado** estiver habilitada ou definida como verdadeira, a opção **Quando Desmarcado, retornar o valor** é exibida.
- **Quando desmarcada, retornar o valor**: essa opção permite especificar qual valor deve ser associado à caixa de seleção quando ela estiver desmarcada ou não for selecionada.

- **Valor padrão**: essa opção permite adicionar um valor padrão a um campo de formulário. Se o **Componente desativado** ou o **Componente de somente leitura** for selecionado, o valor padrão será exibido na tela. Se nenhum valor for inserido pelo usuário no campo de formulário, esse será o valor enviado no momento do envio do formulário.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/checkbox-validation.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve fazer uma seleção antes de prosseguir com o envio de formulário. Não é possível selecionar **Ocultar componente** ou **Desativar componente** na guia **Básico** quando essa opção estiver selecionada.

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

A caixa de diálogo de design é usada para definir e gerenciar estilos CSS do componente Caixa de seleção.

### Guia Estilos {#styles-tab}

O componente principal de Caixa de seleção para formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes padrão do CSS**: você pode fornecer uma classe padrão do CSS ao componente principal caixa de seleção para formulários adaptáveis.

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
