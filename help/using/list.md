---
title: Listar Componente
seo-title: Listar Componente
description: 'null'
seo-description: O Componente de lista de componentes principais permite a fácil criação de listas dinâmicas e estáticas.
uuid: 50 a 572 e 8-b 444-4 f 7 d -82 bc -5 a 93 ebb 4 be 95
contentOwner: Usuário
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 89053323-6221-46 ed -896 a -31 a 42 c 55282 e
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


# Listar Componente{#list-component}

O Componente de lista de componentes principais permite a fácil criação de listas dinâmicas e estáticas.

## Uso {#usage}

O componente de lista pode ser usado para criar, por exemplo, uma lista dinâmica de páginas filhas ou uma lista estática de itens arbitrários. The type of lists available and formatting options can be defined by the template author in the [design dialog](#design-dialog). The content editor can select from available list types and how to format the list elements in the [edit dialog](#edit-dialog).

## Version and Compatibility {#version-and-compatibility}

A versão atual do Componente de lista é v 2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatível | Compatível | Compatível |
| [v1](list-v1.md) | Compatível | Compatível | Compatível |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the List Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/list.html).

### Technical Details {#technical-details}

The latest technical documentation about the List Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

A caixa de diálogo Editar permite que o autor do conteúdo configure a lista e os itens da lista.

### List Settings Tab {#list-settings-tab}

A lista pode ser criada de maneiras diferentes.

* [Páginas secundárias](#child-pages)
* [Lista fixa](#fixed-list)
* [Pesquisar](#search-options)
* [Tags](#tags)

Regardless of how the list is built, there are [Sort Options](#sort-options) that can always be configured.

![](assets/chlimage_1-38.png)

Dependendo de como o autor do conteúdo decide criar a lista, as opções de configuração adicionais serão alteradas.

#### Páginas filhas {#child-pages}

A lista pode ser criada das páginas secundárias da página atual ou de outra página.

![](assets/chlimage_1-39.png)

* **Página primário**
   * A página cujas páginas secundárias devem fazer a lista
   * Deixe em branco para usar a página atual

* **Profundidade secundária** Quantos níveis na hierarquia devem ser usados

#### Fixed List {#fixed-list}

A lista pode ser criada usando uma lista fixa de itens.

![](assets/chlimage_1-40.png)

Tap or click the **Add** button to inset a new item to the list.

* Enter text for the item in the list or use the **Selection Dialog** to choose an item from AEM.
* Use a alça de arrastar para reorganizar os itens na lista.
* Use o ícone de lixeira para excluir itens na lista.

#### Pesquisar {#search-options}

A lista pode ser criada usando os resultados da pesquisa de conteúdo AEM.

![](assets/chlimage_1-41.png)

* **Pesquisar consulta**
A cadeia de caracteres para a qual uma pesquisa de texto completa será executada para gerar os elementos da lista
* **Pesquisar em**
onde a pesquisa deve ser executada
   * Use the **Selection Dialog** to choose the location in AEM
   * Usar a página atual se deixado em branco

#### Tags {#tags}

A lista pode ser criada usando páginas que correspondem a determinadas tags em um determinado local.

![](assets/chlimage_1-42.png)

* **Página
principal** Onde a correspondência da tag deve ser iniciada
   * Use the **Selection Dialog** to choose the location in AEM
   * Usar a página atual se deixado em branco
* **Tags**
que devem ser correspondidas
   * Use the **Browse** dialog to select the tags
* **Corresponder**
define que tipo de correspondência deve qualificar uma página a ser incluída na lista
   * **qualquer tag**
   * **todas as tags**

#### Sort Options {#sort-options}

Independentemente de como você escolher criar a lista, há algumas opções de classificação que podem ser sempre definidas.

![](assets/chlimage_1-43.png)

* **Ordenar por**
como os elementos devem ser ordenados
   * **Título**
   * **Última data de modificação**
* **Ordem de classificação** A ordem em que os itens devem ser ordenados
   * **ascendente**
   * **descendente**
* **Número**máximo de
itens exibidos na lista.
   * Deixe em branco para retornar todos os itens.

### Item Settings Tab {#item-settings-tab}

Usando a guia Configurações do item, é possível configurar a formatação dos elementos da lista.

![](assets/chlimage_1-44.png)

* **Itens do link Vincular itens**
à página correspondente
* **Mostrar descrição**
Exibir descrições do item do link
* **Mostrar data de modificação**Mostrar data
do item do link

## Design Dialog {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais tipos de listas devem ser permitidas aos autores de conteúdo, bem como as configurações de item disponíveis.

### Configurações da lista {#list-settings}

On the **List Settings** tab, the date format can be defined as well as what type of lists should be available in the component to the content authors.

![](assets/chlimage_1-45.png)

* **Formato de formato**
de data a ser usado para a exibição da última data de modificação
* **Desativar os filhos**
desabilitar o tipo de lista infantil no componente
* **Desativar estático**
desativar o tipo de lista estática no componente
* **Desativar a pesquisa**
desativar o tipo de lista de pesquisa no componente
* **Desativar tags**
desativar o tipo de lista de tags no componente

### Configurações do item {#item-settings}

On the **Item Settings** tab, the formatting options for the individual list elements that should be available in the component for the content authors can be defined.

![](assets/chlimage_1-46.png)

* **Itens do link**
Ativar itens do link na caixa de diálogo [Editar](#edit-dialog)
* **Mostrar descrição**
ativar a opção Exibir descrições na janela [de edição](#edit-dialog)
* **Mostrar a**
opção Ativar data mostrar data na janela [de edição](#edit-dialog)

### Styles Tab {#styles-tab}

The Image Component supports the AEM [Style System](authoring.md#component-styling).