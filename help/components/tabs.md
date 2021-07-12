---
title: Componente Guias
description: O Componente de guias permite a criação de várias guias para organizar o conteúdo em uma página.
role: Architect, Developer, Admin, User
exl-id: 0031c5f3-447c-4932-898f-2f453801e492
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 2%

---

# Componente Guias {#tabs-component}

O Componente de guias do componente principal permite a organização do conteúdo em várias guias.

## Uso {#usage}

O Componente de guias permite que o autor de conteúdo organize o conteúdo da página em várias guias.

A [caixa de diálogo de edição](#edit-dialog) permite que o autor de conteúdo defina várias guias, bem como defina a guia ativa. Usando a caixa de diálogo [design](#design-dialog), o autor do modelo pode definir quais componentes podem ser adicionados a guias e personalizar os estilos.

>[!TIP]
>
>Os componentes de guia aninhados (guias dentro de guias) são compatíveis.
>
>Componentes de guia simples (não aninhados) podem ser localizados/selecionados usando a [árvore de conteúdo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree), no entanto, guias aninhadas não podem ser.

## Deep Linking to a Panel {#deep-linking}

As guias e os [Componentes de acordeão](accordion.md) suportam a vinculação diretamente a um painel dentro do componente.

Para fazer isso:

1. Visualize a página com o componente usando a opção **[Exibir como publicada](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** no editor de páginas.
1. Inspect o conteúdo da página e identifica a ID do painel.
   * Por exemplo `id="accordion-86196c94d3-item-ca319dbb0b"`
1. A ID se torna a âncora que pode ser anexada ao URL usando um hash (`#`).
   * Por exemplo `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Ao navegar até o URL com a ID do painel como âncora, o navegador rolar diretamente para o componente específico e exibir o painel especificado. Se o painel estiver configurado para não ser expandido por padrão, ele será expandido automaticamente.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de guias é a v1, que foi introduzida com a versão 2.2.0 dos Componentes principais em outubro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de guias e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_tabs).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de guias [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo crie, renomeie e reorganize as guias, bem como definir a guia ativa.

### Guia Itens {#items-tab}

![Guia Itens de diálogo de edição do Componente de Guias](/help/assets/tabs-edit-items.png)

Use o botão **Adicionar** para abrir o seletor de componentes e escolher qual componente adicionar como guia. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:

* **Ícone**  - O ícone do tipo de componente da guia para facilitar a identificação na lista. Passe o mouse sobre o para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição**  - A descrição usada como o texto da guia, padronizando o nome do componente selecionado para a guia.
* **Excluir**  - Toque ou clique para excluir a guia do componente da guia.
* **Reorganizar**  - Toque ou clique e arraste para reorganizar a ordem das guias.

>[!TIP]
>
>Se a janela de visualização da página for reduzida para que a caixa de diálogo de edição se torne tela cheia, o botão **Add** ficará oculto. Os componentes ainda podem ser adicionados ao Componente de guias ao [arrastar do navegador de componentes e soltar no Componente de guias no editor de páginas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component).

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo Editar do Componente de Guias](/help/assets/tabs-edit-properties.png)

* **Item ativo**  - O autor de conteúdo pode definir qual guia está ativa quando a página é carregada.
   * Com a opção **Default**, a primeira guia será selecionada.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

### Guia Acessibilidade {#accessibility-tab}

![Guia de acessibilidade da caixa de diálogo de edição do componente Guias](/help/assets/tabs-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para os rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo**  - Valor de um atributo de rótulo ARIA para o componente

## Selecionar painel {#select-panel}

O autor de conteúdo pode usar a opção **Selecionar painel** na barra de ferramentas do componente para alterar para um painel diferente para edição, bem como para reorganizar facilmente a ordem das guias.

![Ícone Selecionar painel](/help/assets/select-panel-icon.png)

Depois de selecionar a opção **Selecionar painel** na barra de ferramentas do componente, as guias configuradas são exibidas como uma lista suspensa.

* A lista é ordenada pela disposição atribuída das guias e é refletida na numeração.
* O tipo de componente da guia é exibido primeiro, seguido pela descrição da guia em fonte mais clara.

![Selecionar o volume do painel](/help/assets/select-panel-popover.png)

* Tocar ou clicar em uma entrada na lista suspensa altera a exibição do editor para essa guia.
* As guias podem ser reorganizadas no local usando as alças de arrastar.

>[!NOTE]
>
>As guias não podem ser selecionadas pelo autor quando estiverem no modo **Editar**. Use o modo **[Visualização](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)** ou a opção **[Visualizar como publicado](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** para interagir com as guias como um leitor do conteúdo publicado.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais componentes podem ser adicionados como itens ao componente de guias, bem como defina quais estilos personalizados estão disponíveis para o autor de conteúdo.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** é usada para definir quais componentes podem ser adicionados como itens ao componente de guias pelo autor de conteúdo.

A guia Componentes permitidos funciona da mesma maneira que a guia do mesmo nome ao [definir a política e as propriedades de um Contêiner de layout no Editor de modelo.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Guia Estilos {#styles-tab}

O Componente de guias oferece suporte ao AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

## Camada de dados do cliente Adobe {#data-layer}

O Componente de Guias oferece suporte à Camada de Dados do Cliente do Adobe [.](/help/developing/data-layer/overview.md)
