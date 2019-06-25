---
title: Componente do contêiner
seo-title: Componente do contêiner
description: 'null'
seo-description: O componente do Contêiner de componentes principais permite a criação de um contêiner para vários componentes adicionais em uma página.
uuid: ec 807 de 9-f 76 c -4850-9 ece-c 3 e 439 a 1 d 626
contentOwner: Usuário
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: f 093 f 58 e -9755-4 a 4 f -803 a-ab 93 a 50 e 6870
translation-type: tm+mt
source-git-commit: 3e2e7a297c6ee1d6c8d092c619df8febdc900e25

---


# Container Component{#container-component}

O componente do Contêiner de componentes principais permite a criação de um contêiner para vários componentes adicionais em uma página.

## Uso {#usage}

O componente do Contêiner de componentes principais permite a criação de um contêiner para vários componentes adicionais em uma página e pode ser usado para agrupar outros componentes e aplicar um estilo ou layout comum.

* The container&#39;s properties can be selected in the [configure dialog](#configure-dialog).
* Defaults for the Container Component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

A versão atual do componente do contêiner é v 1, que foi introduzida com a versão 2.5.0 dos Componentes principais em junho de 2019 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Container Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/container.html).

## Technical Details {#technical-details}

The latest technical documentation about the Container Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/container/v1/container).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo defina o item do contêiner e como ele se comportará e aparecerá para um visitante da página.

![](assets/screen-shot-2019-06-21-13.59.26.png)

* **Layout** - Essa opção define o comportamento ou o comportamento de layout do componente do contêiner.
   * **Simples** - define um contêiner como uma coleção simples de componentes
   * **Grade responsiva** - define um contêiner como uma grade responsiva [AEM](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)
* **ID** - Use essa opção para definir o atributo de ID HTML a ser aplicado ao componente.
* **Cor do plano de fundo** - Como valores RGB de forma livre ou usando o seletor de cores, [dependendo da configuração](#background-tab)
* **Imagem de fundo** - define uma cor de plano de fundo para o contêiner [, dependendo da configuração](#background-tab)

## Design Dialog {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor do conteúdo que usa o componente do contêiner.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to the Container Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Default Components Tab {#default-components-tab}

The Default Components tab is used to define which component is added to the component when a particular asset type is dropped on the container, similar to [how default components are defined on the page template](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html#EditingTemplatesTemplateAuthors).

### Responsive Settings Tab {#responsive-settings-tab}

![](assets/screen-shot-2019-06-21-09.33.03.png)

* **Colunas** - define o número de colunas na grade do contêiner resultante.

### Background Tab {#background-tab}

![](assets/screen-shot-2019-06-21-09.42.42.png)

* **Imagem de plano de fundo**
   * **Ativar imagem de plano de fundo** - Selecione esta opção para permitir que o autor do conteúdo defina uma imagem de plano de fundo para o contêiner.
* **Cor do Plano de Fundo**
   * **Ativar a cor do plano de fundo** - Selecione esta opção para permitir que o autor do conteúdo defina uma cor de plano de fundo para o contêiner.
   * **Apenas amostras** - Selecione essa opção para permitir que o autor do conteúdo selecione a partir de amostras de cores pré-definidas para a cor de fundo do contêiner.
      * Only available when **Enable background color** is selected
* **Amostras permitidas** - Define cores pré-definidas de onde o autor do conteúdo pode selecionar a cor de fundo do contêiner
   * Use the **Add** button to add a pre-defined color swatch. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:
   * **Valor** - Defina a cor manualmente por valores RGB
      * Toque ou clique no seletor de cores para selecionar uma cor com mais facilidade, ajustando valores RGB individuais ou definindo um valor hexadecimal.
   * **Excluir** - toque ou clique em para excluir uma amostra.
   * **Reorganizar** - toque ou clique e arraste para reorganizar a ordem das amostras.

### Styles Tab {#styles-tab}

The Container Component supports the AEM [Style System](authoring.md#component-styling).
