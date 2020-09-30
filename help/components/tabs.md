---
title: Componente Tabulações
description: O componente Tabulações permite a criação de várias guias para organizar o conteúdo em uma página.
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 2%

---


# Componente Tabulações {#tabs-component}

O Componente principal de guias de componentes permite a organização de conteúdo em várias guias.

## Uso {#usage}

O componente Guias permite que o autor do conteúdo organize o conteúdo da página em várias guias.

A caixa de diálogo [de](#edit-dialog) edição permite que o autor do conteúdo defina várias guias, bem como defina a guia ativa. Usando a caixa de diálogo [de](#design-dialog)design, o autor do modelo pode definir quais componentes podem ser adicionados às guias e personalizar os estilos.

>[!TIP]
>
>Os componentes de guia aninhados (guias dentro de guias) são suportados.
>
>Componentes de guia simples (não aninhados) podem ser localizados/selecionados usando a árvore [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree)conteúdo, no entanto, guias aninhadas não podem ser.

## Deep links para um painel {#deep-linking}

Os Componentes [Tabulações e](accordion.md) Acordeão suportam a vinculação direta a um painel dentro do componente.

Para fazer isso:

1. Visualização a página com o componente usando a opção **[Visualização como publicada](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** no editor de páginas.
1. Inspect o conteúdo da página e identifique a ID do painel.
   * Por exemplo `id="accordion-86196c94d3-item-ca319dbb0b"`
1. A ID se torna a âncora que você pode anexar ao URL usando um hash (`#`).
   * Por exemplo `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Ao navegar até o URL com a ID do painel como âncora, o navegador rolar diretamente para o componente específico e exibirá o painel especificado. Se o painel estiver configurado para não ser expandido por padrão, ele será expandido automaticamente.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de guias é v1, que foi introduzida com a versão 2.2.0 dos Componentes principais em outubro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o componente Tabs e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_tabs)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Tabs [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Edit Dialog {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo crie, renomeie e reorganize guias, bem como defina a guia ativa.

### Guia Itens {#items-tab}

![Guia de itens da caixa de diálogo de edição do Componente de guias](/help/assets/tabs-edit-items.png)

Use o botão **Adicionar** para abrir o seletor de componentes e escolher qual componente adicionar como guia. Depois de adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:

* **Ícone** - o ícone do tipo de componente da guia para facilitar a identificação na lista. Passe o mouse sobre o mouse para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição** - A descrição usada como o texto da guia, padronizando com o nome do componente selecionado para a guia.
* **Excluir** - Toque ou clique para excluir a guia do componente de guia.
* **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem das guias.

>[!TIP]
>
>Se o visor da página for reduzido para que a caixa de diálogo de edição se torne tela cheia, o botão **Adicionar** ficará oculto. Os componentes ainda podem ser adicionados ao Componente de guias ao [arrastar do navegador de componentes e soltar no Componente de guias no editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component)de páginas.

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do Componente de guias](/help/assets/tabs-edit-properties.png)

* **Item** ativo - o autor do conteúdo pode definir qual guia está ativa quando a página é carregada.
   * Com a opção **Padrão** , a primeira guia será selecionada.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

### Guia Acessibilidade {#accessibility-tab}

![Guia de acessibilidade da caixa de diálogo de edição do Componente de guias](/help/assets/tabs-edit-accessibility.png)

Na guia **Acessibilidade** , os valores podem ser definidos para rótulos de acessibilidade [](https://www.w3.org/WAI/standards-guidelines/aria/) ARIA para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

## Select Panel {#select-panel}

O autor do conteúdo pode usar a opção **Selecionar painel** na barra de ferramentas do componente para mudar para um painel diferente para edição, bem como para reorganizar facilmente a ordem das guias.

![Selecionar ícone do painel](/help/assets/select-panel-icon.png)

Depois de selecionar a opção **Selecionar painel** na barra de ferramentas do componente, as guias configuradas são exibidas como uma lista suspensa.

* A lista é ordenada pela organização atribuída das guias e é refletida na numeração.
* O tipo de componente da guia é exibido primeiro, seguido pela descrição da guia em uma fonte mais leve.

![Selecionar o pod do painel](/help/assets/select-panel-popover.png)

* Tocar ou clicar em uma entrada na lista suspensa alterna a visualização no editor para essa guia.
* As guias podem ser reorganizadas no local usando as alças de arrastar.

>[!NOTE]
>
>As guias não podem ser selecionadas pelo autor quando estiverem no modo **Editar** . Use o modo **[Pré-visualização](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)** ou a opção **[Visualização como publicada](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** para interagir com as guias como um leitor do conteúdo publicado faria.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais componentes podem ser adicionados como itens ao componente de guias, bem como defina quais estilos personalizados estão disponíveis para o autor do conteúdo.

### Allowed Components Tab {#allowed-components-tab}

A guia Componentes **** permitidos é usada para definir quais componentes podem ser adicionados como itens ao componente de guias pelo autor do conteúdo.

A guia Componentes permitidos funciona da mesma maneira que a guia do mesmo nome ao [definir a política e as propriedades de um Container de layout no Editor de modelos.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Guia Estilos {#styles-tab}

O componente Tabs suporta o sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
