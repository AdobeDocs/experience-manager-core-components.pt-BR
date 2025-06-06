---
title: Componente principal do Forms adaptável - Componente de revisão
description: Uso ou personalização do Componente principal de revisão adaptável do Forms.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: 04a685cfa2616839f4fec715847bf0821808bd59
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 14%

---


# Componente de revisão

O componente de Revisão no Adaptive Forms permite que os usuários revisem e verifiquem as informações inseridas antes de enviar o formulário. Ela serve como uma página de resumo, fornecendo uma visualização somente leitura de todos os campos e seus valores em um formato estruturado e fácil de usar. Esse recurso garante que os usuários possam identificar e corrigir erros ou omissões antes de finalizar o envio, melhorando a experiência geral do formulário. Ao clicar no ícone de edição, é possível modificar as informações inseridas antes do envio do formulário.

**Exemplo**

![Componente de revisão](/help/adaptive-forms/assets/review-component.png){width=50%, align=center}

## Uso

Abaixo estão os motivos para usar o componente de Revisão em um Formulário adaptável:

- **Precisão de dados aprimorada**: o Componente de Revisão permite que os usuários revisem todos os dados inseridos antes do envio. Isso ajuda a reduzir as chances de erros ou omissões, garantindo que os dados enviados sejam precisos.
- **Experiência do usuário aprimorada**: os usuários obtêm um resumo claro e organizado de todas as informações que preencheram, garantindo que o formulário esteja completo e preciso antes do envio final, o que melhora a experiência geral.
- **Detecção e correção de erros**: oferece a capacidade de editar informações no nível do painel ou do campo, permitindo que os usuários corrijam erros sem navegar de volta por várias guias. Clicar no ícone **Editar** ao lado de um painel ou campo facilita voltar e corrigir problemas.
- **Maior confiança do usuário**: os usuários podem revisar os dados inseridos, garantindo que as informações que estão enviando estão corretas, o que resulta em menos erros de envio e maior confiança na funcionalidade do formulário.
- **Impedir envios não intencionais**: os usuários frequentemente clicam em **Enviar** sem revisar todos os detalhes. O componente **Revisão** dá a eles a chance final de verificar seus dados, reduzindo a probabilidade de envios não intencionais.


## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de revisão do Forms adaptável na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência para visitantes com a caixa de diálogo de configuração para obter uma experiência do usuário contínua.

![Configurar caixa de diálogo](/help/adaptive-forms/assets/review-component-configure-dialog.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: o título permite identificar facilmente um componente em um formulário; por padrão, ele aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.
- **Ocultar Título**: Selecione a opção para ocultar o Título do componente.
- **Habilitar ações do modo de edição para** - As opções **Habilitar Ações do Modo de Edição para** permitem que os usuários modifiquem as informações inseridas. Os usuários podem editar as informações no nível do campo ou do painel.
   - Quando os usuários selecionam a opção **Campo**, eles podem editar campos de formulário individuais durante a revisão.
   - Quando os usuários selecionam a opção **Painel**, eles podem editar todos os campos em uma seção específica (painel).
   - Quando os usuários selecionam a opção **Campo e Painel**, eles podem clicar no ícone de edição ao lado de um campo para modificar informações específicas ou ao lado de um painel para editar todos os campos dentro desse painel.
   - Quando os usuários selecionam a opção **Nenhum**, eles podem editar qualquer campo ou painel dentro do formulário inteiro.

  Por padrão, a opção **Painel** está selecionada.

- **Painéis de Link** - A opção **Painéis de Link** permite que os usuários selecionem os painéis para revisão. Quando os painéis são vinculados, os usuários podem revisar as informações inseridas dos painéis selecionados e modificá-las antes de enviar.

## Caso de uso

Pegue um exemplo de um **Formulário de pedido de empréstimo** que consiste em quatro guias, onde cada guia coleta informações específicas sobre o usuário:

- **Detalhes Pessoais**: coleta os detalhes pessoais básicos do usuário, como nome, data de nascimento, informações de contato e endereço.

- **Detalhes do empréstimo**: reúne informações relacionadas ao empréstimo, incluindo o tipo de empréstimo, o valor desejado, o período de reembolso e campos calculados automaticamente, como taxa de juros e EMI mensal.

- **Documentos adicionais**: permite que o usuário carregue os documentos necessários, como prova de identidade, prova de endereço e prova de renda. Também inclui uma caixa de seleção de declaração para confirmar a aceitação dos termos.

- **Formulário de Revisão e Envio**: apresenta um Componente de Revisão que resume todas as entradas das guias anteriores. Os usuários podem verificar e editar seus dados antes de enviar o formulário. Esta guia também inclui o botão **Enviar** para enviar o aplicativo.

O vídeo abaixo demonstra como configurar o componente de **Revisão** para que ele ofereça ao usuário a flexibilidade de editar informações:

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}

