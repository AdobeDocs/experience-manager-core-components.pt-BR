---
title: Componente Acordeão
description: O componente principal Acordeão de componentes permite a criação de uma coleção de painéis organizados em um acordeão em uma página.
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 1%

---


# Componente Acordeão{#accordion-component}

O componente principal Acordeão de componentes permite a criação de uma coleção de painéis organizados em um acordeão em uma página.

## Uso {#usage}

O componente principal Acordeão de componentes permite a criação de uma coleção de componentes, composta como painéis, e organizada em um acordeão em uma página, semelhante ao [Componente de guias](tabs.md), mas permite expandir e recolher os painéis.

* As propriedades do acordeão podem ser definidas na caixa de diálogo [configure](#configure-dialog).
* A ordem dos painéis do acordeão pode ser definida na caixa de diálogo de configuração, bem como no [pover do painel de seleção](#select-panel-popover).
* Os padrões do Componente Acordeão ao adicioná-lo a uma página podem ser definidos na caixa de diálogo [design](#design-dialog).

## Deep Linking to a Panel {#deep-linking}

Os componentes Acordeão e [Tabs](tabs.md) suportam a vinculação direta a um painel dentro do componente.

Para fazer isso:

1. Visualização a página com o componente usando a opção **[Visualização como Publicado](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** no editor de páginas.
1. Inspect o conteúdo da página e identifique a ID do painel.
   * Por exemplo `id="accordion-86196c94d3-item-ca319dbb0b"`
1. A ID se torna a âncora que você pode anexar ao URL usando um hash (`#`).
   * Por exemplo `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Ao navegar até o URL com a ID do painel como âncora, o navegador rolar diretamente para o componente específico e exibirá o painel especificado. Se o painel estiver configurado para não ser expandido por padrão, ele será expandido automaticamente.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente Acordeão é v1, que foi introduzida com a versão 2.5.0 dos Componentes Principais em junho de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente Acordeão e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_accordion).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente Acordeão [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_accordion_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o item acordeão, seus painéis e como ele se comportará e aparecerá para um visitante da página.

### Guia Itens {#items-tab}

![Guia Itens da caixa de diálogo de edição do Componente Acordeão](/help/assets/accordion-edit-items.png)

Use o botão **Adicionar** para abrir o seletor de componentes e escolher qual componente adicionar como painel. Depois de adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:

* **Ícone**  - o ícone do tipo de componente do painel para facilitar a identificação na lista. Passe o mouse sobre o mouse para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição**  - A descrição usada como o texto do painel, padronizando com o nome do componente selecionado para o painel.
* **Excluir**  - Toque ou clique para excluir o painel do componente acordeão.
* **Reorganizar**  - Toque ou clique e arraste para reorganizar a ordem dos painéis.

>[!TIP]
>
>Se o visor da página for reduzido para que a caixa de diálogo de edição se torne tela cheia, o botão **Adicionar** ficará oculto. Os componentes ainda podem ser adicionados ao Componente Acordeão ao [arrastar do navegador de componentes e soltar no Componente Acordeão no editor de página](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo Editar do Componente Acordeão](/help/assets/accordion-edit-properties.png)

* **Expansão**  de um único item - Quando selecionada, essa opção força um único item de acordeão a ser expandido de cada vez. Expandir um item recolherá todos os outros.
* **Itens**  expandidos - Essa opção define os itens que são expandidos por padrão quando a página é carregada.
   * Quando **Expansão de item único** é selecionado, um painel deve ser selecionado. Por padrão, o primeiro painel é selecionado.
   * Quando **Expansão de item único** não está selecionada, esta opção é de seleção múltipla e é opcional.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [ de ](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

## Selecione a janela do painel {#select-panel-popover}

O autor do conteúdo pode usar a opção **Selecionar painel** na barra de ferramentas do componente para mudar para um painel diferente para edição, bem como para reorganizar facilmente a ordem dos painéis dentro do acordeão.

![Selecionar ícone do painel](/help/assets/select-panel-icon.png)

Depois de selecionar a opção **Selecionar painel** na barra de ferramentas do componente, os painéis de acordeão configurados são exibidos como um menu suspenso.

![Selecionar o pod do painel](/help/assets/select-panel-popover.png)

* A lista é ordenada pela organização atribuída aos painéis e é refletida na numeração.
* O tipo de componente do painel é exibido primeiro, seguido pela descrição do painel em fonte mais clara.
* Ao tocar ou clicar em uma entrada na lista suspensa, a visualização do editor é alternada para esse painel.
* Os painéis podem ser reorganizados no local usando as alças de arrastar.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor do conteúdo que usa o Componente Acordeão e os padrões definidos ao colocar o Componente Acordeão.

### Guia Propriedades {#properties-tab-design}

![Guia de propriedades da caixa de diálogo Design](/help/assets/accordion-design-properties.png)

* **Elementos**  de cabeçalho permitidos - essa lista suspensa de seleção múltipla define o cabeçalho do item de acordeão elementos HTML que podem ser selecionados por um autor.
* **Elemento**  de cabeçalho padrão - Essa lista suspensa define o elemento HTML de cabeçalho do item de acordeão padrão.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** é usada para definir quais componentes podem ser adicionados como itens aos painéis no Componente Acordeão pelo autor do conteúdo.

A guia Componentes permitidos funciona da mesma maneira que a guia do mesmo nome quando [define a política e as propriedades de um Container de layout no Editor de modelos.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Guia Estilos {#styles-tab}

O Componente Acordeão suporta o AEM [Sistema de estilo](/help/get-started/authoring.md#component-styling).
