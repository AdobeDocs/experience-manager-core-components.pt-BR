---
title: Componente do acordeão
seo-title: Componente do acordeão
description: 'null'
seo-description: O componente de Acordeão do componente principal permite a criação de uma coleção de painéis organizados em um acordeão em uma página.
uuid: ec 807 de 9-f 76 c -4850-9 ece-c 3 e 439 a 1 d 626
contentOwner: Usuário
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: f 093 f 58 e -9755-4 a 4 f -803 a-ab 93 a 50 e 6870
translation-type: tm+mt
source-git-commit: bbd54d433cbeee5395dc8b90bc47f9b44747e25b

---


# Accordion Component{#accordion-component}

O componente de Acordeão do componente principal permite a criação de uma coleção de painéis organizados em um acordeão em uma página.

## Uso {#usage}

The Core Component Accordion component allows for the creation of a collection of components, composed as panels, and arranged in an accordion on a page, similar to the [Tabs Component](tabs.md), but allows for expanding and collapsing of the panels.

* The accordion&#39;s properties can be defined in the [configure dialog](#configure-dialog).
* The order of the panels of the accordion can be defined in the configure dialog as well as the [select panel popover](#select-planel.md).
* Defaults for the Accordion Component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

A versão atual do componente de ion ion é v 1, que foi introduzida com a versão 2.5.0 dos Componentes principais em junho de 2019 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/accordion.html).

## Technical Details {#technical-details}

The latest technical documentation about the Accordion Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/accordion/v1/accordion).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo defina o item de acordeão, seus painéis e como ele se comportará e será exibido para um visitante na página.

### Items Tab {#items-tab}

![](assets/screen-shot-2019-06-21-08.26.38.png)

Use the **Add** button to open the component selector to choose which component to add as a panel. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:

* **Ícone** - O ícone do tipo de componente do painel para fácil identificação na lista. Passe o mouse sobre o nome completo do componente como uma dica de ferramenta.
* **Descrição** - A descrição usada como o texto do painel, padrão do nome do componente selecionado para o painel.
* **Excluir** - toque ou clique em para excluir o painel do componente acordeão.
* **Reorganizar** - toque ou clique e arraste para reorganizar a ordem dos painéis.

### Properties Tab {#properties-tab}

![](assets/screen-shot-2019-06-21-08.26.53.png)

* **Expansão de item único** - quando selecionada, essa opção força um único item de acordeão a ser expandido por vez. Expandir um item recolhe todos os outros.
* **Itens ampliados** - Essa opção define os itens que são expandidos por padrão quando a página é carregada.
   * When **Single item expansion** is selected, one panel must be selected. Por padrão, o primeiro painel é selecionado.
   * When **Single item expansion** is not selected, this option is a multi-select and is optional.

## Select Panel Popover {#seelct-panel-popover}

The content author can use the **Select Panel** option on the component toolbar to change to a different panel for editing as well as to easily rearrange the order of the panels within the accordion.

![](assets/screen-shot-2019-06-21-08.49.36.png)

Once selecting the **Select Panel** option in the component toolbar, the configured accordion panels are displayed as a drop-down.

![](assets/screen-shot-2019-06-21-08.52.14.png)

* A lista é ordenada pela disposição atribuída dos painéis e refletida na numeração.
* O tipo de componente do painel é exibido primeiro, seguido pela descrição do painel na fonte mais leve.
* Tocar ou clicar em uma entrada na lista suspensa, alterna a exibição no editor para esse painel.
* Os painéis podem ser reorganizados no local usando as alças de arrastar.

## Design Dialog {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor do conteúdo que usa o componente de Ion Ion Component e os padrões definidos ao posicionar o componente de Ion Ion.

### Properties Tab {#properties-tab-design}

![](assets/screen-shot-2019-06-21-08.58.11.png)

* **Elementos de cabeçalho permitidos** - Esse menu suspenso de várias seleções define o cabeçalho do cabeçalho em HTML que tem permissão para ser selecionado por um autor.
* **Elemento de cabeçalho padrão** - Esse menu suspenso define o cabeçalho do cabeçalho padrão do item HTML.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to panels in the Accordion Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Styles Tab {#styles-tab}

The Accordion Component supports the AEM [Style System](authoring.md#component-styling).
