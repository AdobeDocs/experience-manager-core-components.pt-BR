---
title: Componente acordeão
description: O componente Acordo do componente principal permite a criação de uma coleção de painéis organizados de acordo com uma opção em uma página.
role: Arquiteto, Desenvolvedor, Administrador, Praticante de negócios
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 1%

---


# Componente acordeão{#accordion-component}

O componente Acordo do componente principal permite a criação de uma coleção de painéis organizados de acordo com uma opção em uma página.

## Uso {#usage}

O componente Principal de Acordo de Componente permite a criação de uma coleção de componentes, composta como painéis, e organizada de uma forma em uma página, semelhante ao [Componente de Guias](tabs.md), mas permite expandir e recolher os painéis.

* As propriedades da opção podem ser definidas na caixa de diálogo [configurar](#configure-dialog).
* A ordem dos painéis da opção pode ser definida na caixa de diálogo de configuração, bem como no [pover de painel selecionado](#select-panel-popover).
* Os padrões do Componente Acordeão ao adicioná-lo a uma página podem ser definidos na caixa de diálogo [design](#design-dialog).

## Deep Linking to a Panel {#deep-linking}

Os Componentes Acordeão e [Tabs](tabs.md) suportam a vinculação diretamente a um painel dentro do componente.

Para fazer isso:

1. Visualize a página com o componente usando a opção **[Exibir como publicada](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** no editor de páginas.
1. Inspect o conteúdo da página e identifica a ID do painel.
   * Por exemplo `id="accordion-86196c94d3-item-ca319dbb0b"`
1. A ID se torna a âncora que pode ser anexada ao URL usando um hash (`#`).
   * Por exemplo `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Ao navegar até o URL com a ID do painel como âncora, o navegador rolar diretamente para o componente específico e exibir o painel especificado. Se o painel estiver configurado para não ser expandido por padrão, ele será expandido automaticamente.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente Acordeão é v1, que foi introduzida com a versão 2.5.0 dos Componentes principais em junho de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente acordeão, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_accordion).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente acordeão [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_accordion_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o item da opção, seus painéis e como ele se comportará e aparecerá para um visitante da página.

### Guia Itens {#items-tab}

![Guia Itens da caixa de diálogo Editar do Componente Acordeão](/help/assets/accordion-edit-items.png)

Use o botão **Adicionar** para abrir o seletor de componentes e escolher qual componente adicionar como painel. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:

* **Ícone**  - O ícone do tipo de componente do painel para facilitar a identificação na lista. Passe o mouse sobre o para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição**  - A descrição usada como o texto do painel, padronizando o nome do componente selecionado para o painel.
* **Excluir**  - Toque ou clique para excluir o painel do componente do acordeão.
* **Reorganizar**  - Toque ou clique e arraste para reorganizar a ordem dos painéis.

>[!TIP]
>
>Se a janela de visualização da página for reduzida para que a caixa de diálogo de edição se torne tela cheia, o botão **Add** ficará oculto. Os componentes ainda podem ser adicionados ao Componente de acordeão [arrastando do navegador de componentes e soltando no Componente de acordeão no editor de páginas](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo Editar do Componente de Acordo](/help/assets/accordion-edit-properties.png)

* **Expansão de um único item**  - Quando selecionada, essa opção força um único item de opção a ser expandido de cada vez. Expandir um item recolherá todos os outros.
* **Itens expandidos**  - essa opção define os itens que são expandidos por padrão quando a página é carregada.
   * Quando **Expansão de item único** é selecionada, um painel deve ser selecionado. Por padrão, o primeiro painel é selecionado.
   * Quando **Expansão de item único** não está selecionada, esta opção é de seleção múltipla e é opcional.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

## Selecione Pasta do painel {#select-panel-popover}

O autor de conteúdo pode usar a opção **Selecionar painel** na barra de ferramentas do componente para alterar para um painel diferente para edição, bem como para reorganizar facilmente a ordem dos painéis dentro da opção .

![Ícone Selecionar painel](/help/assets/select-panel-icon.png)

Depois de selecionar a opção **Selecionar painel** na barra de ferramentas do componente, os painéis de opções configurados são exibidos como uma lista suspensa.

![Selecionar o volume do painel](/help/assets/select-panel-popover.png)

* A lista é ordenada pela organização atribuída dos painéis e é refletida na numeração.
* O tipo de componente do painel é exibido primeiro, seguido pela descrição do painel em fonte mais clara.
* Tocar ou clicar em uma entrada na lista suspensa altera a exibição do editor para esse painel.
* Os painéis podem ser reorganizados no local usando as alças de arrastar.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o Componente de acordeão e os padrões definidos ao colocar o Componente de acordeão.

### Guia Propriedades {#properties-tab-design}

![Guia de propriedades da caixa de diálogo Design](/help/assets/accordion-design-properties.png)

* **Elementos de cabeçalho permitidos**  - Essa lista suspensa de várias seleções define os elementos HTML do cabeçalho do item de opção que podem ser selecionados por um autor.
* **Elemento de cabeçalho padrão**  - Essa lista suspensa define o elemento HTML do cabeçalho do item de opção padrão.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** é usada para definir quais componentes podem ser adicionados como itens aos painéis no Componente de acordeão pelo autor de conteúdo.

A guia Componentes permitidos funciona da mesma maneira que a guia do mesmo nome ao [definir a política e as propriedades de um Contêiner de layout no Editor de modelo.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Guia Estilos {#styles-tab}

O Componente Acordeão suporta o AEM [Sistema de Estilos](/help/get-started/authoring.md#component-styling).

## Camada de dados do cliente Adobe {#data-layer}

O Componente Acordeão suporta a [Camada de Dados do Cliente Adobe.](/help/developing/data-layer/overview.md)
