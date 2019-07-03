---
title: Componente de tabulações
seo-title: Componente de tabulações
description: O componente de tabulações permite a criação de várias guias para organizar o conteúdo em uma página.
seo-description: O componente de tabulações permite a criação de várias guias para organizar o conteúdo em uma página.
uuid: 46 f 71233-8 b 12-4887-a 0 c 6-ad 24 dc 469 cb 1
content-type: referência
topic-tags: componentes principais
discoiquuid: 966 d 47 fb-d 35 d -4103-b 29 d -4 ef 0 aa 739 f 24
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Componente de tabulações

O componente de tabulações do componente principal permite a organização do conteúdo em várias guias.

## Uso {#usage}

O componente de tabulações permite que o autor do conteúdo organize o conteúdo da página em várias guias.

The [edit dialog](#edit-dialog) allows the content author to define multiple tabs as well as set the active tab. Using the [design dialog](#design-dialog), the template author can define which components can be added to tabs and customize the styles.

>[!NOTE]
>
>Os componentes da guia aninhados (guias nas guias) são suportados.
>
>Simple (non-nested) tab components can be located/selected using the [content tree](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html), however nested tabs can not be.

## Version and Compatibility {#version-and-compatibility}

A versão atual do componente de tabulações é v 1, que foi introduzida com a versão 2.2.0 dos Componentes principais em outubro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatível | Compatível | Compatível |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Tabs Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/tabs.html).

### Technical Details {#technical-details}

The latest technical documentation about the Tabs Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

A caixa de diálogo Editar permite que o autor do conteúdo crie, renomeie e reorganize guias, bem como defina a guia ativa.

### Items Tab {#items-tab}

![](assets/screenshot_2018-10-11at153557.png)

Use the **Add** button to open the component selector to choose which component to add as a tab. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:

* **Ícone** - O ícone do tipo de componente da guia para fácil identificação na lista. Passe o mouse sobre o nome completo do componente como uma dica de ferramenta.
* **Descrição** - A descrição usada como o texto da guia, padrão do nome do componente selecionado para a guia.
* **Excluir** - toque ou clique para excluir a guia do componente da guia.
* **Reorganizar** - toque ou clique e arraste para reorganizar a ordem das guias.

### Properties Tab {#properties-tab}

![](assets/screenshot_2018-10-19at140646.png)

On the **Properties** tab, the content author can define which tab is active when the page is loaded. With the **Default** option, the first tab will be selected.

## Select Panel {#select-panel}

The content author can use the **Select Panel** option on the component toolbar to change to a different panel for editing as well as to easily rearrange the order of the tabs.

![](assets/screenshot_2018-10-11at165417.png)

Once selecting the **Select Panel** option in the component toolbar, the configured tabs are displayed as a drop-down.

* A lista é ordenada pela disposição atribuída das guias e refletida na numeração.
* O tipo de componente da guia é exibido primeiro, seguido pela descrição da guia na fonte mais leve.

![](assets/screenshot_2018-10-11at165154.png)

* Tocar ou clicar em uma entrada na lista suspensa, alterna a exibição no editor para essa guia.
* As guias podem ser reorganizadas no local usando as alças de arrastar.

>[!NOTE]
>
>Tabs are not selectable by the author when in **Edit** mode. Use [**Preview** mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) or the **[View as Published](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** option to interact with the tabs as a reader of the published content would.

## Design Dialog {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais componentes podem ser adicionados como itens ao componente tabulações, bem como definir quais estilos personalizados estão disponíveis para o autor do conteúdo.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to the tabs component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Styles Tab {#styles-tab}

The Tabs Component supports the AEM [Style System](authoring.md#component-styling).