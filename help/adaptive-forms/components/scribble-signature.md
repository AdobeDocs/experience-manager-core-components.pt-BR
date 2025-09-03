---
title: 'Componente principal de formulários adaptáveis: assinatura à mão'
description: Usar ou personalizar o componente principal de assinatura à mão dos formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 608c4368-d539-4d05-a75c-c077ea822f93
source-git-commit: 006f6c844ab9e7a784dabea026867939445479e9
workflow-type: tm+mt
source-wordcount: '1761'
ht-degree: 98%

---

# Componente de assinatura à mão

<span>O componente de assinatura assinável está no Programa de Primeiros usuários. Você pode escrever para `aem-forms-ea@adobe.com` a partir de sua ID de email oficial para participar do programa de adoção antecipada e solicitar acesso à funcionalidade.</span>

Um componente de assinatura à mão em um formulário adaptável é um elemento da interface do usuário que permite que os usuários desenhem sua **assinatura** diretamente no formulário com um mouse, caneta ou tela sensível ao toque. Ele garante uma captação precisa de consentimentos, aprovações ou verificações escritos à mão em fluxos de trabalho digitais.

**Exemplo**

![exemplo](/help/adaptive-forms/assets/scribble-signature.png){width=50%,align-center}

**Várias opções disponíveis na janela de assinatura**

- **A:** clique no ícone de **Desenhar** para desenhar a sua assinatura na tela.
- **B:** clique no ícone de **Limpar** para limpar a assinatura na tela.
- **C:** clique no ícone de **Geolocalização** para adicionar a geolocalização junto com a assinatura.
- **D:** clique no ícone de **Teclado** para digitar o seu nome na tela.

Depois de selecionar o ícone de **Salvar** na janela de assinatura à mão, você não poderá editar a assinatura. Caso você queira editar a assinatura, desconsidere a assinatura atual e assine novamente com a opção de pincel/teclado acima.

>[!NOTE]
>
> As assinaturas são sempre salvas no formato PNG.

## Uso {#reasons-to-use-scribble-signature}

Há vários motivos por que é vantajoso incluir um campo de assinatura à mão em um formulário, incluindo:

- **Consentimento digital**: permite que os usuários forneçam assinaturas válidas legalmente de forma eletrônica.
- **Experiência do usuário aprimorada**: fornece uma maneira natural de fazer logon diretamente em dispositivos sem verificação ou carregamento.
- **Fluxos de trabalho sem papel**: elimina a necessidade de imprimir, assinar e digitalizar novamente os documentos.
- **Autenticação**: atua como uma camada adicional de confirmação e aprovação.
- **Precisão dos dados**: garante uma captação correta da entrada escrita à mão do signatário em formato digital.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal de assinatura à mão dos formulários adaptáveis foi lançado em **agosto de 2025** como parte dos **Componentes principais 2.24.6** para o Cloud Service e posteriores.

| Versão do componente | AEM as a Cloud Service | AEM Forms 6.5.16.0 ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.24.6](/help/adaptive-forms/version.md) e posteriores | |

Para mais detalhes sobre versões, consulte [Versões dos componentes principais](/help/adaptive-forms/version.md).

## Detalhes técnicos {#technical-details}

Confira os detalhes técnicos mais recentes do componente principal de assinatura à mão dos formulários adaptáveis no [GitHub](https://github.com/adobe/aem-core-forms-components). Para mais informações sobre o desenvolvimento dos componentes principais, consulte a [documentação dos componentes principais para desenvolvedores](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite a personalização do componente de assinatura à mão.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/scribble-signature-basictab.png)

- **Nome**: O nome identifica exclusivamente o componente no editor de regras. Caracteres especiais e espaços não são permitidos nas strings de nome.

- **Título**: Título é uma string que aparece na parte superior de um componente em um Formulário adaptável. Título identifica exclusivamente o componente na estrutura em árvore de um Formulário adaptável. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.
- **Permitir rich text para título**: esse recurso permite formatar títulos de texto simples, incorporando recursos como negrito, itálico, texto sublinhado, várias fontes, tamanhos de fonte, cores e uma opção adicional para aprimorar a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção **Permitir rich text para título**, as opções de formatação se tornam visíveis para estilizar o título do componente. Para acessar todas as opções de formatação disponíveis, clique no ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: Selecione essa opção para ocultar o título do tipo de componente em um Formulário adaptável.
- **Texto de espaço reservado**: O texto do espaço reservado em um componente de formulário refere-se a um rótulo curto ou prompt que aparece em um campo de entrada como uma dica para o usuário sobre que tipo de informação deve ser inserida nesse campo. O texto de espaço reservado desaparece quando o usuário começa a digitar no campo e reaparece se o campo estiver vazio. Fornece uma dica visual ao usuário, mas não age como um rótulo ou valor permanente para o campo.

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.

- **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

- **Título da caixa de diálogo de assinatura**: o título da caixa de diálogo de assinatura define o texto exibido na parte superior da caixa de diálogo de captação da assinatura. Ele serve como um prompt ou instrução para o usuário quando for necessário fornecer uma assinatura. O texto ajuda a guiar o usuário pelo processo de assinatura, tornando a interação clara e intuitiva.

### Guia de validação

![guia de validação](/help/adaptive-forms/assets/scribble-signature-validation.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve fazer uma seleção antes de prosseguir com o envio de formulário. Não é possível selecionar a opção **Ocultar componente** ou **Desativar componente** na guia **Básico** quando essa opção estiver selecionada.

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

- **Mensagem de validação de script**: essa opção permite que inserir uma mensagem que será exibida se a validação do script falhar.

### Guia Conteúdo de ajuda {#help-content-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/scribble-signature-helptab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Habilite a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**- Habilite a opção para exibir a Descrição curta abaixo do componente.

- **Texto da ajuda**: O texto da ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade](/help/adaptive-forms/assets/scribble-signature-accessibilitytab.png)

- **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por pessoas com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.
   - **Texto personalizado**: selecione essa opção para usar o texto personalizado para rótulos de acessibilidade ARIA. Selecionar essa opção exibe a caixa de diálogo Texto personalizado. Você pode adicionar informações relevantes na caixa de diálogo Texto personalizado.
   - **Descrição**: selecione essa opção para usar a descrição para rótulos de acessibilidade ARIA.
   - **Título**: selecione essa opção para usar o título para rótulos de acessibilidade ARIA.
   - **Nome**: selecione essa opção para usar o nome para rótulos de acessibilidade ARIA.
   - **Nenhum**: selecione essa opção se não quiser adicionar rótulos de acessibilidade ARIA.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar estilos de CSS do componente de assinatura à mão.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de assinatura à mão dos formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo Design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes padrão do CSS**: é possível fornecer uma classe padrão do CSS ao componente principal de assinatura à mão dos formulários adaptáveis.

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
