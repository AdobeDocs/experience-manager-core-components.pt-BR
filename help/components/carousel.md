---
title: Componente carrossel
description: O componente carrossel permite que o autor de conteúdo apresente conteúdo em um carrossel giratório.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 1%

---


# Componente carrossel{#carousel-component}

O componente principal carrossel permite que o autor do conteúdo apresente conteúdo em um carrossel navegável.

## Uso {#usage}

Usando o componente Carrossel, o autor do conteúdo para organizar o conteúdo em um carrossel giratório de slides.

A [caixa de diálogo de edição](#edit-dialog) permite que o autor de conteúdo crie, nomeie e ordene vários slides, bem como habilite a transição automática com atraso. Usando a caixa de diálogo [design](#design-dialog), o autor do modelo pode definir quais componentes podem ser adicionados ao carrossel, ativar ou desativar transições automáticas e personalizar os estilos.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente carrossel é a v1, que foi introduzida com a versão 2.2.0 dos Componentes principais em outubro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o componente carrossel e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_carousel).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente carrossel [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Editar Caixa de Diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo adicione, renomeie e reorganize os slides, bem como definir as configurações de transição automática.

### Guia Itens {#items-tab}

![Guia Itens da caixa de diálogo Editar do componente carrossel](/help/assets/carousel-edit-items.png)

Use o botão **Adicionar** para abrir o seletor de componentes e escolher qual componente adicionar como guia. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:

* **Ícone**  - O ícone do tipo de componente da guia para facilitar a identificação na lista. Passe o mouse sobre o para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição**  - A descrição usada como o texto da guia, padronizando o nome do componente selecionado para a guia.
* **Excluir**  - Toque ou clique para excluir a guia do componente de guias.
* **Reordenar**  - Toque ou clique e arraste para ordenar as guias.

>[!TIP]
>
>Se a janela de visualização da página for reduzida para que a caixa de diálogo de edição se torne tela cheia, o botão **Add** ficará oculto. Os componentes ainda podem ser adicionados ao componente Carrossel ao [arrastar do navegador de componentes e soltar no componente Carrossel no editor de páginas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component-from-the-components-browser).

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo Editar do componente carrossel](/help/assets/carousel-edit-properties.png)

Na guia **Properties**, o autor de conteúdo pode definir os slides para fazer a transição automática.

* **Fazer a transição automática de slides**  - Quando ativo, o componente avança automaticamente para o próximo slide após um atraso especificado.
* **Atraso de transição**  - Quando os slides de transição automática são selecionados, esse valor é usado para definir o atraso entre as transições (em milissegundos).
* **Desativar a pausa automática ao passar o mouse**  - Quando a opção Fazer a transição  **automática de** slidesis estiver selecionada, a transição do carrossel será automaticamente pausada sempre que o cursor passar o cursor sobre o carrossel. Selecione essa opção para que a transição não seja pausada.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

>[!NOTE]
>
>Os controles de avanço de slide não são ativados quando estão no modo **Editar**. Use o modo [**Visualização**](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode) ou a opção **[Visualizar como publicado](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** para interagir com o carrossel como um leitor do conteúdo publicado.
>
>O recurso de avanço automático não é ativado quando está no modo **Editar**. Use a opção **[Exibir como publicado](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** para ver o recurso de avanço automático como um leitor do conteúdo publicado.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade da caixa de diálogo Editar do componente carrossel](/help/assets/carousel-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para os rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo**  - Valor de um atributo de rótulo ARIA para o componente

## Selecionar Painel {#select-panel}

O autor de conteúdo pode usar a opção **Selecionar painel** na barra de ferramentas do componente para alterar para um slide diferente para edição, bem como para reorganizar facilmente a ordem dos slides.

![Ícone Selecionar painel](/help/assets/select-panel-icon.png)

Depois de selecionar a opção **Selecionar painel** na barra de ferramentas do componente, os slides configurados são exibidos como uma lista suspensa.

* A lista é ordenada pela disposição atribuída dos slides e é refletida na numeração.
* O tipo de componente do slide é exibido primeiro, seguido pela descrição do slide com fonte mais clara.

![Selecionar painel](/help/assets/select-panel-popover.png)

* Tocar ou clicar em uma entrada na lista suspensa altera a exibição do editor para esse slide.
* O slide pode ser reordenado no local usando as alças de arrastar.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais componentes podem ser adicionados como slides ao componente do carrossel, bem como definir padrões de transição automática e quais estilos personalizados estão disponíveis para o autor de conteúdo.

### Guia Propriedades {#properties-tab-1}

A guia **Properties** é usada para definir as configurações padrão para as transições de slide quando um autor de conteúdo adiciona o componente de carrossel a uma página.

![Caixa de diálogo Design do componente carrossel](/help/assets/carousel-design.png)

* **Fazer a transição automática de slides**  - Define se, por padrão, a opção de avançar automaticamente o carrossel para o próximo slide é ativada quando o autor de conteúdo adiciona o componente do carrossel a uma página.
* **Atraso de transição**  - Define o valor padrão do atraso de transição entre os slides (em milissegundos) quando um autor de conteúdo adiciona o componente de carrossel a uma página.
* **Desativar a pausa automática ao passar o mouse**  - Define se, por padrão, a opção para desativar a pausa automática de slide é ativada quando a opção Fazer a transição  **automática de** slidesis é selecionada pelo autor de conteúdo.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** é usada para definir quais componentes podem ser adicionados como slides ao Componente de carrossel pelo autor de conteúdo.

A guia Componentes permitidos funciona da mesma maneira que a guia do mesmo nome ao [definir a política e as propriedades de um Contêiner de layout no Editor de modelo.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Guia Estilos {#styles-tab}

O componente carrossel suporta o AEM [Style System](/help/get-started/authoring.md#component-styling).

## Camada de dados do cliente Adobe {#data-layer}

O componente carrossel suporta a [Camada de Dados do Cliente Adobe.](/help/developing/data-layer/overview.md)
