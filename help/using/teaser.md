---
title: Componente de Teaser
seo-title: Componente de Teaser
description: O componente de teaser pode mostrar uma imagem, um título, rich text e, opcionalmente, um link para outro conteúdo.
seo-description: O componente de teaser pode mostrar uma imagem, um título, rich text e, opcionalmente, um link para outro conteúdo.
uuid: 46989314-df 37-448 b -8562-c 707043 f 2160
contentOwner: bohnert
content-type: referência
topic-tags: componentes principais
discoiquuid: e 597 c 18 e -3643-41 be -9878-4 a 7872 f 1 ab 90
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Teaser Component{#teaser-component}

O componente de Teaser principal do componente pode mostrar uma imagem, um título, rich text e, opcionalmente, um link para outro conteúdo.

## Uso {#usage}

O Componente de Teaser permite que o autor do conteúdo crie facilmente um teaser para mais conteúdo usando uma imagem, um título ou texto formatado e links para mais conteúdo ou outras ações.

The template author can use the [design dialog](#design-dialog) to define if the options to create call-to-actions and add links are available as well as disabling various display options. The content author can use the [configure dialog](#configure-dialog) to set an image, define CTAs, set titles and descriptions, and configure links to the individual teaser. The [edit dialog](image.md#edit-dialog) of the [Image Component](image.md) can be accessed to modify the teaser image.

## Version and Compatibility {#version-and-compatibility}

A versão atual do componente Teaser é v 1, que foi introduzida com a versão 2.1.0 dos Componentes principais em julho de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v1 | Compatível | Compatível | Compatível |

## Sample Component Output {#sample-component-output}

To experience the Teaser Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/teaser.html).

### Technical Details {#technical-details}

The latest technical documentation about the Teaser Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

O autor do conteúdo pode usar a caixa de diálogo Configurar para definir as propriedades do teaser individual. There is also an [edit dialog](#edit-dialog) to modify the teaser image if one is selected.

### Imagem {#image}

![](assets/screen_shot_2018-07-03at104125.png)

* **Ativos da imagem**
   * Drop an asset from the [asset browser](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) or tap the **browse** option to upload from a local file system.
   * Tap or click **Clear** to de-select the currently selected image.
   * Tap or click **Edit** to [mange the renditions of the asset](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) in the asset editor.

### Text {#text}

![](assets/screen_shot_2018-07-03at104138.png)

* **Título**
Define um título para exibir como o cabeçalho do teaser.
* **Obter título de página
vinculada** Quando marcado, o título será preenchido com o título da página vinculada.
* **Descrição**
Define uma descrição a ser exibida como o artigo do teaser.
* **Obter descrição de página
vinculada** quando marcada, a descrição será preenchida com a descrição da página vinculada.

### Links &amp; Actions {#links-actions}

![](assets/screen_shot_2018-07-03at104146.png)

* **Link Link**
aplicado ao teaser. Use o navegador de caminho para selecionar o destino do link.
* **Ativar chamadas de chamada** quando marcadas, permite a definição de chamada de ações. O primeiro link de Chamada de ação na lista é usado como link para outros elementos de teaser.

## Edit Dialog {#edit-dialog}

The Teaser Component delegates image rendering to the [Image Component](image.md). Therefore the [edit dialog](image.md#edit-dialog of the Image Component is available to the content author to manipulate the teaser image.

## Design Dialog {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de teaser que o autor do conteúdo tem ao usar este componente.

### Teaser Tab {#teaser-tab}

![](assets/screen_shot_2018-07-03at105958.png)

* **Frases de chamariz**
   * **Desativar chamadas de chamada** para ocultar a **opção** de chamada para autores de conteúdo
* **Elementos**
   * **Ocultar título**
      * Hides the **Title** option for content authors
      * When selected the **Title Type** is hidden
   * **Ocultar descrição**
Oculta a opção **Descrição** para autores de conteúdo
* **Tipo
de título** Define a tag H a ser usada pelo título do teaser.
* **Links**
   * **Não vincular a imagem**
Quando selecionada, a imagem de teaser não é vinculada
   * **Não vincular o título**
Quando selecionado, o título de teaser não é vinculado

### Styles Tab {#styles-tab}

The Teaser Component supports the AEM [Style System](authoring.md#component-styling).
