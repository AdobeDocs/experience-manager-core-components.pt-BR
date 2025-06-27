---
title: 'Componente principal dos formulários adaptáveis: componente de revisão'
description: Uso ou personalização do componente principal de revisão de formulários adaptáveis.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
exl-id: acd230ed-284b-4df2-98e0-a0090cd73611
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '742'
ht-degree: 100%

---


# Componente de revisão

O componente de revisão de formulários adaptáveis permite que os usuários revisem e verifiquem as informações inseridas antes de enviar o formulário. Ele serve como uma página de resumo, fornecendo uma visualização do tipo somente leitura de todos os campos e seus valores em um formato estruturado e fácil de usar. Esse recurso garante que os usuários possam identificar e corrigir erros ou omissões antes de finalizar o envio, melhorando a experiência geral com o formulário. Ao clicar no ícone de edição, é possível modificar as informações inseridas antes de enviar o formulário.

{{traditional-aem}}

**Exemplo**

![Componente de revisão](/help/adaptive-forms/assets/review-component.png){width=50%, align=center}

## Uso

Confira abaixo os motivos para usar o componente de revisão em um formulário adaptável:

- **Precisão de dados aprimorada**: o componente de revisão permite que os usuários revisem todos os dados inseridos antes do envio. Isso ajuda a reduzir as chances de erros ou omissões, garantindo que os dados enviados estejam corretos.
- **Experiência do usuário aprimorada**: os usuários obtêm um resumo claro e organizado de todas as informações que preencheram, garantindo que o formulário esteja completo e correto antes do envio final, o que melhora a experiência geral.
- **Detecção e correção de erros**: permite editar informações na camada do painel ou do campo, permitindo que os usuários corrijam erros sem navegar de volta por várias guias. Clicar no ícone de **Editar** ao lado de um painel ou campo ajuda a voltar e corrigir problemas.
- **Maior confiança do usuário**: os usuários podem revisar os dados inseridos, garantindo que as informações que estão enviando estejam corretas, o que resulta em menos erros de envio e uma maior confiança na funcionalidade do formulário.
- **Impedir envios não intencionais**: os usuários frequentemente clicam em **Enviar** sem revisar todos os detalhes. O componente de **Revisão** proporciona uma chance final de verificar os dados, reduzindo a probabilidade de envios não intencionais.


## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal de revisão de formulários adaptáveis na documentação técnica, encontrada no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência para visitantes com a caixa de diálogo de configuração para obter uma experiência do usuário fluida.

![Caixa de diálogo de configuração](/help/adaptive-forms/assets/review-component-configure-dialog.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: o título permite identificar facilmente um componente em um formulário; por padrão, ele aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.
- **Ocultar Título**: Selecione a opção para ocultar o Título do componente.
- **Habilitar ações no modo de edição para**: as opções de **Habilitar ações no modo de edição para** permitem que os usuários modifiquem as informações inseridas. Os usuários podem editar as informações na camada do campo ou do painel.
   - Quando os usuários selecionam a opção **Campo**, eles podem editar campos individuais do formulário durante a revisão.
   - Quando os usuários selecionam a opção **Painel**, eles podem editar todos os campos de uma seção (painel) específica.
   - Quando os usuários selecionam a opção **Campo e painel**, eles podem clicar no ícone de edição ao lado de um campo para modificar informações específicas ou ao lado de um painel para editar todos os campos dentro desse painel.
   - Quando os usuários selecionam a opção **Nenhum**, eles podem editar qualquer campo ou painel dentro do formulário inteiro.

  Por padrão, a opção **Painel** é selecionada.

- **Vincular painéis**: a opção **Vincular painéis** permite que os usuários selecionem os painéis para revisão. Quando os painéis são vinculados, os usuários podem revisar as informações inseridas nos painéis selecionados e modificá-las antes de enviar.

## Caso de uso

Neste exemplo, um **Formulário de pedido de empréstimo** consiste em quatro guias, onde cada guia coleta informações específicas sobre o usuário:

- **Detalhes pessoais**: coleta os detalhes pessoais básicos do usuário, como nome, data de nascimento, informações para contato e endereço.

- **Detalhes do empréstimo**: reúne informações relacionadas ao empréstimo, incluindo o tipo de empréstimo, o valor desejado, o prazo de pagamento e campos calculados automaticamente, como taxa de juros e parcelas mensais.

- **Documentos adicionais**: permite que o usuário carregue os documentos necessários, como comprovante de identidade, comprovante de endereço e comprovante de renda. Também inclui uma caixa de seleção de declaração para confirmar a aceitação dos termos.

- **Revisar e enviar formulário**: consiste em um componente de revisão que resume todas as entradas das guias anteriores. Os usuários podem verificar e editar os dados antes de enviar o formulário. Esta guia também inclui o botão **Enviar** para enviar o pedido.

O vídeo abaixo demonstra como configurar o componente de **Revisão**, de modo que ele ofereça ao usuário a flexibilidade de editar informações:

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}
