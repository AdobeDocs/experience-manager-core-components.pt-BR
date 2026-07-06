---
title: Componente principal adaptável do Forms - Opção de imagem
description: Uso do Componente principal da Opção de imagem.
role: Developer, Admin, User
hide: true
source-git-commit: 0af65c80f9cc58c4ba48d5b3dc7a026820bd2833
workflow-type: tm+mt
source-wordcount: '1318'
ht-degree: 58%

---

# Campo ImageChoice do formulário adaptável {#image-choice}

O componente Opção de imagem em um formulário permite que os usuários façam seleções com base em representações visuais, como imagens, em vez de opções baseadas em texto. Apresenta uma série de imagens, cada uma representando uma escolha distinta. Os usuários podem selecionar uma ou mais imagens, com feedback visual indicando sua seleção. Este componente é útil para opções como variantes de produtos, respostas de pesquisas ou imagens de perfis. Ele aumenta o engajamento e a clareza do usuário, oferecendo um método de seleção intuitivo e visualmente atraente.

## Uso

Existem vários recursos principais do Componente de escolha de imagem, como:

- **Representação de Imagem:** Os usuários veem imagens em vez dos rótulos de texto tradicionais ou botões de opção. Cada imagem corresponde a uma escolha que podem selecionar, fornecendo uma representação visual das opções disponíveis.

- **Imagens Clicáveis:** Os usuários podem selecionar uma opção clicando diretamente na imagem. A imagem selecionada frequentemente fica realçada para indicar que foi escolhida.

- **Seleções únicas ou múltiplas:** Dependendo do design do componente, os usuários podem selecionar uma única imagem ou várias imagens.

## Versão e compatibilidade {#version-and-compatibility}

O componente Adaptive Forms Image Choice foi lançado como parte dos Componentes principais 2.0.64. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service |
|---|---|
| v1 | Compatível com a <br>[versão 2.0.64](/help/adaptive-forms/version.md) e posteriores |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal Adaptive Forms Image Choice na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/). Para obter mais informações sobre o desenvolvimento dos componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Com a caixa de diálogo de configuração, é possível personalizar facilmente a experiência do componente Opção de imagem para visitantes.


### Guia Básico {#basic-tab}

![Escolha básica de imagem de guia](basic-tab-imagechoice.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título** - Com seu Título, você pode identificar facilmente um tipo de componente em um formulário adaptável e, por padrão, o título aparece ao lado do componente.

- **Ocultar Título** - Você pode ocultar o título marcando a caixa Ocultar Título.

- **Opções** - Ajuda você a adicionar uma ou várias imagens e personalizar as propriedades de escolha de imagem. As propriedades de escolha de imagem incluem Valor de dados, Ativo de referência de imagem e Texto alternativo para cada uma das imagens.

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados.

  Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.

- **Tipo de dados do valor enviado**: esta opção especifica o tipo de dados do valor enviado quando uma opção é selecionada. Se o **tipo de dados do valor enviado** estiver definido como `Number` e você adicionar uma string de dados em **Valor de dados** na guia **Opções**, a tela exibirá uma mensagem de erro `Value type mismatch`.

- **Opções de Exibição**: oferece uma opção para exibir o campo de escolha de imagem na horizontal ou na vertical.

- **Valor Padrão**: esta opção permite adicionar um valor padrão (valor de dados) em um campo de formulário. Se um **Componente Desabilitado** ou **Componente Somente Leitura** for selecionado, o valor padrão será exibido na tela. Se nenhum valor for inserido pelo usuário no campo de formulário, esse valor será enviado no momento do envio do formulário.

- **Ocultar componente**: selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

- **Desabilitar Componente**: selecione a opção para desabilitar ou bloquear o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

- **Somente Leitura**: esta opção permite adicionar um valor padrão (valor de dados) em um campo de formulário. Se um **Componente Desabilitado** ou **Componente Somente Leitura** for selecionado, o valor padrão será exibido na tela. Se nenhum valor for inserido pelo usuário no campo de formulário, esse valor será enviado no momento do envio do formulário.

- **Tipo de seleção**: essa opção permite que seus usuários selecionem uma ou várias seleções de campos de escolha de imagem.

### Guia Validação {#validation-tab}

![Opção de imagem da guia de validação](validation-tab-image-choice.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve fazer uma seleção antes de prosseguir com o envio de formulário. Você não pode selecionar o **Ocultar Componente** ou **Desabilitar Componente na guia** Básico** quando esta opção está selecionada.

- **Mensagem de Erro** - Essa opção permite inserir uma mensagem que será exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo de escolha de imagem não estiver selecionado.

- **Mensagem de validação de script**: essa opção permite que inserir uma mensagem que será exibida se a validação do script falhar.

### Guia Conteúdo de ajuda {#helpcontent-tab}

![Escolha de imagem de conteúdo de ajuda](help-content-imagechoice.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Habilite a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: habilite essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.



### Guia Acessibilidade {#accessibility-tab}

![Opção de imagem de acessibilidade](accessibility-imagechoice.png)

- **Texto para leitores de tela**: isso se refere ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por pessoas com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.
   - **Texto personalizado**: selecione essa opção para usar o texto personalizado para rótulos de acessibilidade ARIA. Selecionar essa opção exibe a caixa de diálogo Texto personalizado. Você pode adicionar informações relevantes na caixa de diálogo Texto personalizado.
   - **Título**: selecione essa opção para usar o título para rótulos de acessibilidade ARIA.

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}


