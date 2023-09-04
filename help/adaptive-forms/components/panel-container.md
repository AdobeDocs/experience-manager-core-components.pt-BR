---
title: Componente principal dos Formulários adaptáveis - Container do painel
description: Utilização ou personalização do Componente principal de container do painel dos Formulários adaptáveis.
role: Architect, Developer, Admin, User
source-git-commit: b6e3a443c7425a60fc6c3469dc273960a4e29088
workflow-type: tm+mt
source-wordcount: '1539'
ht-degree: 99%

---

# Container do painel {#panel-container-adaptive-forms-core-component}

Em um Formulário adaptável, um painel é um elemento de container que pode ser usado para agrupar elementos de formulário relacionados. Ele permite agrupar e organizar diferentes elementos de formulário de forma lógica e significativa. Isso pode ajudar a melhorar a estrutura geral e a legibilidade do formulário, facilitando a compreensão e a navegação pelos usuários.

Painéis também podem ser usados para criar seções recolhidas, o que pode ser útil para ocultar campos de formulário complexos ou usados com menos frequência, mantendo o formulário simples e fácil de usar. Também permite incluir outros componentes, como texto, caixa de seleção, botão etc.

Também pode ser usado para definir diferentes ações baseadas em regras, como enviar formulário, abrir um site, mostrar/ocultar componentes ou adicionar uma instância de um painel.

**Exemplo**

![](/help/adaptive-forms/assets/panel-container.png)

## Uso {#reasons-to-use-panel-container}

Há vários motivos para usar um painel em um formulário, incluindo:

- **Organizar elementos de formulário**: um painel pode ser usado para agrupar elementos de formulário relacionados, facilitando a compreensão e a navegação dos usuários.

- **Melhoria da estrutura dos formulários**: ao agrupar elementos de formulário em painéis, é possível melhorar a estrutura geral e a legibilidade do formulário, facilitando sua compreensão.

- **Criação de seções recolhidas**: painéis podem ser usados para criar seções recolhidas, o que pode ser útil para ocultar campos de formulário complexos ou usados com menos frequência, mantendo o formulário simples e fácil de usar.

- **Aprimoramento da usabilidade**: ao usar painéis para organizar elementos de formulário, ele pode tornar o formulário mais fácil de usar e intuitivo, o que pode resultar em taxas de conclusão mais altas.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal de Container do painel dos Formulários adaptáveis foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade com o AEM e os links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível com a <br>[versão 2.0.4](/help/versions.md) e posteriores | Compatível | Compatível |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de Container do painel dos Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Para mais informações sobre o desenvolvimento dos Componentes principais, consulte a [Documentação do desenvolvedor dos componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do container do painel para visitantes com a caixa de diálogo Configurar. Você também pode definir opções de container de painel com facilidade para proporcionar uma experiência do usuário contínua.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/basic-panel.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Ocultar Título**: Selecione a opção para ocultar o Título do componente.

- **Agrupar dados de componentes secundários no envio do formulário (vincular dados no objeto)**: quando essa opção é selecionada, os dados dos componentes secundários são aninhados no objeto JSON do componente principal. No entanto, se a opção não estiver selecionada, os dados JSON enviados terão uma estrutura simples, sem qualquer objeto para o componente principal. Por exemplo:

   - Quando a opção é selecionada, os dados dos componentes secundários (por exemplo, Rua, Cidade e CEP) são aninhados no componente principal (Endereço) como um objeto JSON. Isso cria uma estrutura hierárquica e os dados são organizados no componente principal.

     Estrutura dos dados enviados:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Quando a opção não está selecionada, os dados JSON enviados têm uma estrutura simples sem qualquer objeto para o componente principal (Endereço). Todos os dados estão no mesmo nível, sem qualquer organização hierárquica.


     Estrutura dos dados enviados:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Layout**: o assistente pode ter um layout fixo (simples) ou um layout flexível (grade responsiva). O layout simples mantém tudo fixo no lugar, enquanto a grade responsiva permite que você ajuste a posição dos componentes para atender às suas necessidades. Por exemplo, use a grade responsiva para alinhar “Nome”, “Nome do meio” e “Sobrenome” em uma única linha do formulário.

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.
- **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Repetir painel Guia {#repeat-panel}

![repetir guia](/help/adaptive-forms/assets/repeat-panel.png)

É possível usar as opções de repetibilidade para duplicar o container do painel e seus componentes secundários, definir uma contagem de repetição mínima e máxima e facilitar a replicação de seções semelhantes em um formulário. Ao interagir com o componente de container do painel e acessar suas configurações, as seguintes opções são apresentadas:

- **Tornar o Assistente repetível**: um recurso que permite habilitar ou desabilitar a funcionalidade de repetibilidade.
- **Repetições mínimas**: estabelece o número mínimo de vezes que o container do painel pode ser repetido. O valor padrão é zero e ele indica que o painel Assistente não é repetido.
- **Máximo de repetições**: define o número máximo de vezes que o container do painel pode ser repetido. Por padrão, esse valor é ilimitado.

Para gerenciar com eficácia as seções repetíveis no container do painel, siga as etapas fornecidas no artigo [Criação de formulários com seções repetíveis](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=pt-BR).

### Guia Conteúdo de ajuda {#help-content}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/helpcontent-panel.png)


- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/accessibilty-panel.png)


- **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

- **Função de HTML para anúncio do leitor de tela**: a função HTML é um atributo usado para especificar a finalidade de um elemento HTML para tecnologias assistivas, como leitores de tela. O atributo de função é usado para fornecer contexto e significado semântico adicionais a um elemento, facilitando a interpretação e o anúncio do conteúdo pelos leitores de tela. Por exemplo, no AEM Forms, o rótulo de um campo de formulário pode ter a função de “rótulo” e seu campo de entrada pode ter a função de “caixa de texto”. Isso ajuda o leitor de tela a entender a relação entre o rótulo e o campo de entrada e anunciá-los corretamente ao usuário.

## Artigo relacionado {#related-article}

- [Criar um formulário adaptável em uma página do AEM Sites ou fragmento de experiência](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=pt-BR)

- [Criar um formulário adaptável independente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=pt-BR)


## Consulte Também {#see-also}

- [Acordeão](/help/adaptive-forms/components/accordion.md)
- [Botão](/help/adaptive-forms/components/button.md)
- [Grupo de Caixa de seleção](/help/adaptive-forms/components/checkbox-group.md)
- [Seletor de data](/help/adaptive-forms/components/date-picker.md)
- [Lista suspensa](/help/adaptive-forms/components/drop-down.md)
- [Entrada de email](/help/adaptive-forms/components/email-input.md)
- [Containeres de formulário](/help/adaptive-forms/components/form-container.md)
- [Anexo de arquivo](/help/adaptive-forms/components/file-attachment.md)
- [Rodapé](/help/adaptive-forms/components/footer.md)
- [Cabeçalho](/help/adaptive-forms/components/header.md)
- [Guias horizontais](/help/adaptive-forms/components/horizontal-tabs.md)
- [Imagem](/help/adaptive-forms/components/image.md)
- [Entrada de número](/help/adaptive-forms/components/number-input.md)
- [Botão de opção](/help/adaptive-forms/components/radio-button.md)
- [Botão Redefinir](/help/adaptive-forms/components/reset-button.md)
- [Botão Enviar](/help/adaptive-forms/components/submit-button.md)
- [Entrada de telefone](/help/adaptive-forms/components/telephone-input.md)
- [Entrada de texto](/help/adaptive-forms/components/text-input.md)
- [Texto](/help/adaptive-forms/components/text.md)
- [Título](/help/adaptive-forms/components/title.md)
- [Assistente](/help/adaptive-forms/components/wizard.md)