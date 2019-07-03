---
title: Componente do carrossel
seo-title: Componente do carrossel
description: 'null'
seo-description: O componente carrossel permite que o autor do conteúdo apresente conteúdo em um carrossel giratório.
uuid: 34934491-bd 85-4 f 1 e-ae 22-bb 48 ed 4 dbd 5 c
content-type: referência
topic-tags: componentes principais
discoiquuid: 3510812 b -9 d 3 e -40 fe-b 986-0 f 15 d 40 b 42
disttype: dist5
gnavtheme: light
groupsectionnavitems: não
hidemerchandisingbar: herdar
hidepromocomponent: herdar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Carousel Component{#carousel-component}

O componente do carrossel principal permite que o autor do conteúdo apresente conteúdo em um carrossel navegável.

## Uso {#usage}

Usando o componente do carrossel, o autor do conteúdo para organizar o conteúdo em um carrossel giratório de slides.

The [edit dialog](#edit-dialog) allows the content author to create, name, and order multiple slides as well as enable auto-transition with delay. Using the [design dialog](#design-dialog), the template author can define which components can be added to the carousel, enable or disable automatic transitions, and customize the styles.

## Version and Compatibility {#version-and-compatibility}

A versão atual do componente carrossel é v 1, que foi introduzida com a versão 2.2.0 dos Componentes principais em outubro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatível | Compatível | Compatível |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Carousel Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/carousel.html).

### Technical Details {#technical-details}

The latest technical documentation about the Carousel Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

A caixa de diálogo Editar permite que o autor do conteúdo adicione, renomeie e reorganize slides, bem como defina as configurações de transição automática.

### Items Tab {#items-tab}

![](assets/screenshot_2018-10-12at102451.png)

Use the **Add** button to open the component selector to choose which component to add as a tab. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:

* **Ícone** - O ícone do tipo de componente da guia para fácil identificação na lista. Passe o mouse sobre o nome completo do componente como uma dica de ferramenta.
* **Descrição** - A descrição usada como o texto da guia, padrão do nome do componente selecionado para a guia.
* **Excluir** - toque ou clique para excluir a guia do componente tabulações.
* **Reordenar** - toque ou clique e arraste para ordenar as guias.

### Properties Tab {#properties-tab}

![](assets/screenshot_2018-11-28at141054.png)

On the **Properties** tab, the content author can set the slides to automatically transition.

* **Slides de transição automaticamente** - quando ativo, o componente avança automaticamente para o próximo slide após um atraso especificado.
* **Atraso de transição** - Quando os slides de transição automaticamente são selecionados, esse valor é usado para definir o atraso entre as transições (em milissegundos).
* **Desativar pausa automática ao passar o mouse** - quando **os slides de transição automaticamente** são selecionados, a transição do carrossel automaticamente pausa sempre que o cursor passa sobre o carrossel. Selecione esta opção para que a transição não pause.

>[!NOTE]
>
>The slide advance controls are not enabled when in **Edit** mode. Use [**Preview** mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) or the **[View as Published](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** option to interact with the carousel as a reader of the published content would.
>
>The auto-advance feature is not enabled when in **Edit** mode. Use **[View as Published](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** option to see the auto-advance feature as a reader of the published content would.

## Select Panel {#select-panel}

The content author can use the **Select Panel** option on the component toolbar to change to a different slide for editing as well as to easily rearrange the order of the slides.

![](assets/screenshot_2018-10-11at165417.png)

Once selecting the **Select Panel** option in the component toolbar, the configured slides are displayed as a drop-down.

* A lista é ordenada pela disposição atribuída dos slides e refletida na numeração.
* O tipo de componente do slide é exibido primeiro, seguido pela descrição do slide na fonte mais leve.

![](assets/opera_snapshot_2018-11-28141537localhost.png)

* Tocar ou clicar em uma entrada na lista suspensa, alterna a exibição no editor para esse slide.
* O slide pode ser reordenado no local usando as alças de arrastar.

## Design Dialog {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais componentes podem ser adicionados como slides para o componente do carrossel, bem como definir padrões de transição automática e quais estilos personalizados estão disponíveis para o autor do conteúdo.

### Properties Tab {#properties-tab-1}

The **Properties** tab is used to define the default settings for the slide transitions when a content author adds the carousel component to a page.

![](assets/screenshot_2018-11-28at141824.png)

* **Automaticamente de transição** - define se, por padrão, a opção para mover automaticamente o carrossel para o próximo slide é ativada quando o autor do conteúdo adiciona o componente de carrossel a uma página.
* **Atraso de transição** - define o valor padrão do atraso de transição entre slides (em milissegundos) quando um autor de conteúdo adiciona o componente de carrossel a uma página.
* **Desativar pausa automática ao passar o mouse** - define se por padrão a opção para desativar a pausa automática de slide está ativada quando **os slides de transição automática** são selecionados pelo autor do conteúdo.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as slides to the Carousel Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Styles Tab {#styles-tab}

The Carousel Component supports the AEM [Style System](authoring.md#component-styling).