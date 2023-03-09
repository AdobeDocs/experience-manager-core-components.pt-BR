---
title: Componente Acordeão
description: O componente Acordeão, dos Componentes principais, permite a criação de uma coleção de painéis organizados em acordeão em uma página.
role: Architect, Developer, Admin, User
exl-id: 1deb570a-3d8d-409e-805f-8460c49cf9bb
source-git-commit: e8b3e55a42b6be6262d6f51b9569c0be3e8ce6c3
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 98%

---

# Componente Acordeão{#accordion-component}

O componente Acordeão, dos Componentes principais, permite a criação de uma coleção de painéis organizados em acordeão em uma página.

## Uso {#usage}

O componente Acordeão, dos Componentes principais, permite a criação de uma coleção de componentes, composta como painéis, e organizada em acordeão em uma página, semelhante ao [componente de Guias](tabs.md), mas permite expandir e recolher os painéis.

* As propriedades do acordeão podem ser definidas na [caixa de diálogo de configuração](#configure-dialog).
* A ordem dos painéis do acordeão pode ser definida na caixa de diálogo de configuração, bem como no [popover Selecionar painel](#select-panel-popover).
* Os padrões do componente Acordeão, ao adicioná-lo a uma página, podem ser definidos na [caixa de diálogo de design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente Acordeão é v1, que foi introduzida com a versão 2.5.0 dos Componentes principais em junho de 2019, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível  com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Acordeão, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_accordion_br).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Acordeão [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_accordion_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Deep linking para um painel {#deep-linking}

O Acordeão, [Carrossel,](carousel.md) e [Componentes de guias](tabs.md) suporte à vinculação diretamente a um painel dentro do componente.

Para fazer isso:

1. Visualize a página com o componente usando a opção **[Exibir como publicada](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR#view-as-published)** no editor de páginas.
1. Inspecione o conteúdo da página e identifique o ID do painel.
   * Por exemplo `id="accordion-86196c94d3-item-ca319dbb0b"`
1. O ID se torna a âncora que pode ser anexada ao URL usando um hash (`#`).
   * Por exemplo `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Ao navegar até o URL com o ID do painel como âncora, o navegador rolará diretamente para o componente específico e exibirá o painel especificado. Se o painel estiver configurado para não ser expandido por padrão, ele será expandido automaticamente.

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o item do Acordeão, seus painéis e como ele se comportará e aparecerá para um visitante da página.

### Guia Itens {#items-tab}

![Guia Itens, da caixa de diálogo de edição do componente Acordeão](/help/assets/accordion-edit-items.png)

Use o botão **Adicionar** para abrir o seletor de componentes e escolher qual componente adicionar como painel. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:

* **Ícone** - O ícone do tipo de componente do painel para facilitar a identificação na lista. Passe o mouse sobre o ícone para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição** - A descrição usada como o texto do painel, padronizando o nome do componente selecionado para o painel.
* **Excluir** - Toque ou clique para excluir o painel do componente Acordeão.
* **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem dos painéis.

>[!TIP]
>
>Se a janela de visualização da página for reduzida para que a caixa de diálogo de edição se torne tela cheia, o botão **Adicionar** ficará oculto. Os componentes ainda podem ser adicionados ao componente Acordeão [arrastando do navegador de componentes e soltando no componente Acordeão no editor de páginas](https://helpx.adobe.com/br/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponen).

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do componente Acordeão](/help/assets/accordion-edit-properties.png)

* **Expansão de um único item** - Quando selecionada, essa opção força um único item do acordeão a ser expandido de cada vez. Expandir um item recolherá todos os outros.
* **Itens expandidos** - Essa opção define os itens que são expandidos por padrão quando a página é carregada.
   * Quando a opção **Expansão de item único** é selecionada, um painel deve ser selecionado. Por padrão, o primeiro painel é selecionado.
   * Quando **Expansão de item único** não é selecionada, esta opção é de seleção múltipla e é facultativa.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

## Selecionar Popover de painel {#select-panel-popover}

O autor de conteúdo pode usar a opção **Selecionar painel** na barra de ferramentas do componente para alterar para um painel diferente para edição, e também para reorganizar facilmente a ordem dos painéis dentro do acordeão.

![Ícone Selecionar painel](/help/assets/select-panel-icon.png)

Depois de escolher a opção **Selecionar painel** na barra de ferramentas do componente, os painéis do acordeão configurados são exibidos como uma lista suspensa.

![Selecionar popover de painel](/help/assets/select-panel-popover.png)

* A lista é ordenada pela organização atribuída dos painéis e é refletida na numeração.
* O tipo de componente do painel é exibido primeiro, seguido pela descrição do painel em fonte mais clara.
* Tocar ou clicar em uma entrada na lista suspensa altera a exibição do editor para esse painel.
* Os painéis podem ser reorganizados no local usando as alças de arrastar.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o componente Acordeão e os padrões definidos ao colocar o componente Acordeão.

### Guia Propriedades {#properties-tab-design}

![Guia de propriedades da caixa de diálogo de Design](/help/assets/accordion-design-properties.png)

* **Elementos de cabeçalho permitidos** - Essa lista suspensa de várias seleções define os elementos HTML do cabeçalho do item de acordeão que podem ser selecionados por um autor.
* **Elemento de cabeçalho padrão** - Essa lista suspensa define o elemento HTML do cabeçalho de itens do acordeão padrão.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** é usada para definir quais componentes podem ser adicionados como itens aos painéis no componente Acordeão pelo autor de conteúdo.

Ela funciona da mesma maneira que a guia de mesmo nome ao [definir a política e as propriedades de um Contêiner de layout no Editor de modelo.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR#editing-a-template-layout-template-author)

### Guia Estilos {#styles-tab}

O componente Acordeão é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente Acordeão é compatível com a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
