---
title: Componente principal de formulários adaptáveis - Assistente
description: Uso ou personalização do componente principal do assistente de formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: fd785cd2-5ed6-4efb-997f-ce9056ed113d
source-git-commit: 0026734a2e43c51c7f5af2b37492d61e8f779ac7
workflow-type: tm+mt
source-wordcount: '1866'
ht-degree: 100%

---

# Assistente {#wizard-adaptive-forms-core-component}

O layout de assistente em um formulário adaptável refere-se a um formulário dividido em várias etapas ou páginas, permitindo que o usuário se mova pelo formulário uma etapa de cada vez. Esse layout é chamado de “assistente” porque guia o usuário passo a passo através do formulário.

Cada etapa do assistente normalmente contém um grupo de campos de formulário relacionados e um mecanismo de navegação, como botões “Avançar” e “Voltar”, para percorrer as etapas. O usuário só poderá prosseguir para a próxima etapa depois que a etapa atual tiver sido concluída e todos os campos obrigatórios tiverem sido preenchidos.

O layout de assistente é útil em formulários que possuem muitos campos ou informações que precisam ser coletadas, pois divide o formulário em partes menores e mais fáceis de se controlar. Também ajuda os usuários a se concentrarem em um conjunto de campos por vez, o que pode simplificar o processo de preenchimento de formulário.

No entanto, ele também pode aumentar a complexidade do formulário, pois o usuário precisará percorrer várias páginas para terminar de preencher o formulário. Portanto, é necessário avaliar os requisitos do formulário e as necessidades do usuário antes de decidir usar um layout de assistente.

Você pode usar o componente principal de layout de assistente em um formulário adaptável para criar o layout de assistente.


**Exemplo**

![](/help/adaptive-forms/assets/wizard.png)

## Uso {#reasons-to-use-wizard-in-an-adaptive-form}

Há várias vantagens de se usar um layout de assistente em um formulário adaptável:

* **Simplicidade**: dividir um formulário em várias etapas pode melhorar a compreensão dos usuários para que eles o concluam mais facilmente, pois eles podem se concentrar em um conjunto de campos por vez.

* **Organização**: um layout de assistente pode ajudar a organizar os formulários por tópico ou finalidade e também pode agrupar campos relacionados, tornando o processo de preenchimento do formulário mais lógico e eficiente.

* **Validação**: um layout de assistente permite a validação passo a passo, o que pode ajudar os usuários a identificar e corrigir erros durante o processo ao invés de esperar até o fim do formulário.

* **Indicador de progresso**: um layout de assistente pode exibir o progresso do formulário, o que pode ajudar o usuário a entender o quanto ainda resta para ser preenchido no formulário.

* **Formulários longos**: se o formulário tiver muitos campos, pode ser difícil para o usuário visualizar todos ao mesmo tempo, então separá-los em partes menores e mais controláveis pode torná-lo menos intimidador.

* **Evitar o abandono**: um layout de assistente também pode ajudar a reduzir o abandono de formulário, pois os usuários têm mais probabilidade de concluir um formulário caso possam ver o progresso e saber o quanto falta.

* **Experiência móvel**: um layout de assistente também pode ser benéfico para formulários acessados em dispositivos móveis, pois são utilizadas páginas menores que carregam mais rápido e são mais fáceis de navegar.

Em geral, o layout de assistente pode tornar o processo de preenchimento de formulário mais controlável e eficiente para os usuários, mas é importante considerar a complexidade do formulário e as necessidades do usuário antes de decidir usar esse tipo de layout.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal do layout de assistente de formulários adaptáveis foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta tabela mostra todas as versões compatíveis, a compatibilidade com o AEM e inclui links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível com a <br>[versão 2.0.4](/help/versions.md) e posteriores | Compatível | Compatível |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de Título dos Formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/wizard/v1/wizard). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do assistente para visitantes com a caixa de diálogo de configuração. Você também pode definir as opções do assistente com facilidade para uma experiência de usuário perfeita.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/wizard-basic.png)

* **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

* **Título**: com o Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente.

* **Ocultar título**: selecione essa opção para ocultar o título do componente.

* **Agrupar dados em um objeto**: escolha “Agrupar dados em um objeto” para colocar os dados do campo do assistente dentro de um objeto JSON. Se isto não for definido, o JSON de envio de dados terá uma estrutura simples para os campos do assistente.

* **Layout**: o assistente pode ter um layout fixo (simples) ou um layout flexível (grade responsiva). O layout simples mantém tudo fixo no lugar, enquanto a grade responsiva permite que você ajuste a posição dos componentes para atender às suas necessidades. Por exemplo, use a grade responsiva para alinhar “Nome”, “Nome do meio” e “Sobrenome” em uma única linha do formulário.

* **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

* **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

* **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Repetir guia Assistente {#repeat-wizard-tab}

![Repetir Assistente](/help/adaptive-forms/assets/wizard-repeat.png)

É possível usar as opções de repetibilidade para duplicar o Assistente e seus componentes secundários, definir uma contagem de repetição mínima e máxima e facilitar a replicação de seções semelhantes em um formulário. Ao interagir com o componente Assistente e acessar suas configurações, as seguintes opções serão apresentadas:

* **Tornar o Assistente repetível**: um recurso que permite habilitar ou desabilitar a funcionalidade de repetibilidade.
* **Repetições mínimas**: estabelece o número mínimo de vezes que o painel Assistente pode ser repetido. O valor padrão é zero e ele indica que o painel Assistente não é repetido.
* **Máximo de repetições**: define o número máximo de vezes que o painel Assistente pode ser repetido. Por padrão, esse valor é ilimitado.

Para gerenciar com eficácia as seções repetíveis no Assistente, siga as etapas fornecidas no artigo [Criação de formulários com seções repetíveis](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=pt-BR).

### Guia Ajuda {#help-tab}

![Guia Ajuda](/help/adaptive-forms/assets/wizard-helpcontent.png)

* **Descrição curta**: uma breve descrição é uma concisa explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

* **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.


### Guia Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/wizard-accessibility.png)

* **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

* **Função de HTML para anúncio do leitor de tela**: a função HTML é um atributo usado para especificar a finalidade de um elemento HTML para tecnologias assistivas, como leitores de tela. O atributo de função é usado para fornecer contexto e significado semântico adicionais a um elemento, facilitando a interpretação e o anúncio do conteúdo pelos leitores de tela. Por exemplo, no AEM Forms, o rótulo de um campo de formulário pode ter a função de “rótulo” e seu campo de entrada pode ter a função de “caixa de texto”. Isso ajuda o leitor de tela a entender a relação entre o rótulo e o campo de entrada e anunciá-los corretamente ao usuário.


## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que os criadores de modelos controlem a exibição padrão dos elementos. Para o componente Assistente de Formulários adaptáveis, você pode definir o seguinte:

* Os componentes principais que um criador de formulário pode adicionar ao Assistente no editor de Formulários adaptáveis.
* Nomes simples para estilos (classes CSS) que podem ser aplicados na caixa de diálogo de propriedades do componente Assistente no editor de Formulários adaptáveis.

Isso ajuda a tornar o processo de criação e personalização de formulários mais simples e eficiente.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** permite que o editor de modelos defina os componentes que podem ser adicionados como itens aos painéis no componente Assistente no editor de Formulários adaptáveis.

### Guia Estilos {#styles-tab}

A caixa de diálogo de design é usada para definir e gerenciar os estilos CSS de um componente. O Componente principal do Assistente de Formulários adaptáveis é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) AEM.

**Classes CSS Padrão**: você pode fornecer uma classe CSS padrão para o componente Assistente.

**Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

>[!MORELIKETHIS]
>
>* [Acordeão](/help/adaptive-forms/components/accordion.md)
>* [Botão](/help/adaptive-forms/components/button.md)
>* [Grupo de Caixa de seleção](/help/adaptive-forms/components/checkbox-group.md)
>* [Seletor de data](/help/adaptive-forms/components/date-picker.md)
>* [Lista suspensa](/help/adaptive-forms/components/drop-down.md)
>* [Entrada de email](/help/adaptive-forms/components/email-input.md)
>* [Container de formulário](/help/adaptive-forms/components/form-container.md)
>* [Anexo de arquivo](/help/adaptive-forms/components/file-attachment.md)
>* [Rodapé](/help/adaptive-forms/components/footer.md)
>* [Cabeçalho](/help/adaptive-forms/components/header.md)
>* [Guias horizontais](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Imagem](/help/adaptive-forms/components/image.md)
>* [Entrada de número](/help/adaptive-forms/components/number-input.md)
>* [Container do painel](/help/adaptive-forms/components/panel-container.md)
>* [Botão de opção](/help/adaptive-forms/components/radio-button.md)
>* [Botão Redefinir](/help/adaptive-forms/components/reset-button.md)
>* [Botão Enviar](/help/adaptive-forms/components/submit-button.md)
>* [Entrada de telefone](/help/adaptive-forms/components/telephone-input.md)
>* [Entrada de texto](/help/adaptive-forms/components/text-input.md)
>* [Texto](/help/adaptive-forms/components/text.md)
>* [Título](/help/adaptive-forms/components/title.md)

## Consulte também {#see-also}

{{see-also}}
