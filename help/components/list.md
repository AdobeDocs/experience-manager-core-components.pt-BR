---
title: Listar Componente
description: O Componente de lista de componentes principais permite a criação fácil de listas dinâmicas e estáticas.
role: Arquiteto, Desenvolvedor, Administrador, Praticante de negócios
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '984'
ht-degree: 4%

---


# Listar Componente{#list-component}

O Componente de lista de componentes principais permite a criação fácil de listas dinâmicas e estáticas.

## Uso {#usage}

O Componente de lista pode ser usado para criar, por exemplo, uma lista dinâmica de páginas filhas ou uma lista estática de itens definidos arbitrariamente. O tipo de listas disponíveis e as opções de formatação podem ser definidas pelo autor do modelo na caixa de diálogo [design](#design-dialog). O editor de conteúdo pode selecionar entre os tipos de lista disponíveis e como formatar os elementos da lista no [diálogo de edição](#edit-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de lista é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](v1/list-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de lista e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_list).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de lista [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_list_v2).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Editar Caixa de Diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo configure a lista e os itens da lista.

### Guia Configurações de Lista {#list-settings-tab}

A lista pode ser criada de maneiras diferentes.

* [Páginas secundárias](#child-pages)
* [Lista fixa](#fixed-list)
* [Pesquisar](#search-options)
* [Tags](#tags)

Independentemente de como a lista é criada, há [Opções de Classificação e ID](#sort-options) que podem ser sempre configuradas.

![Caixa de diálogo de edição do componente de lista](/help/assets/list-edit.png)

Dependendo de como o autor de conteúdo optar por criar a lista, as opções de configuração adicionais serão alteradas.

#### Páginas filhas {#child-pages}

A lista pode ser criada das páginas filhas da página atual ou de outra página.

![Opções de página filho](/help/assets/list-edit-child-pages.png)

* **Página primário**
   * A página cujas páginas secundárias devem fazer a lista
   * Deixe em branco para usar a página atual

* **Profundidade-**
filhoQuantos níveis abaixo da hierarquia devem ser usados

#### Lista fixa {#fixed-list}

A lista pode ser criada usando uma lista fixa de itens.

![Opções de lista fixa](/help/assets/list-edit-fixed.png)

Toque ou clique no botão **Add** para inserir um novo item à lista.

* Insira o texto para o item na lista ou use a **Caixa de Diálogo de Seleção** para escolher um item do AEM.
* Use a alça de arrastar para reorganizar os itens na lista.
* Use o ícone da lixeira para excluir itens na lista.

#### Pesquisar {#search-options}

A lista pode ser criada usando os resultados de uma pesquisa de conteúdo AEM.

![Opções da lista de pesquisa](/help/assets/list-edit-search.png)

* **Pesquisar**
consultaA sequência de caracteres para a qual uma pesquisa de texto completo será executada para gerar os elementos da lista
* **Pesquisar**
noOnde a pesquisa deve ser executada
   * Use a caixa de diálogo **Seleção** para escolher o local no AEM
   * Usar página atual se deixado em branco

#### Tags {#tags}

A lista pode ser criada usando páginas que correspondem a determinadas tags em um determinado local.

![Opções da lista de tags](/help/assets/list-edit-tags.png)

* **Página principal**
Onde a correspondência de tags deve começar
   * Use a caixa de diálogo **Seleção** para escolher o local no AEM
   * Usar página atual se deixado em branco
* ****
TagsQuais tags devem ser correspondidas
   * Use a caixa de diálogo **Procurar** para selecionar as tags
* ****
MatchDefine que tipo de correspondência deve qualificar uma página a ser incluída na lista
   * **qualquer tag**
   * **todas as tags**

#### Opções de classificação {#sort-options}

Independentemente de como você optar por criar a lista, há certas opções de classificação que podem sempre ser definidas.

![Opções de classificação](/help/assets/list-edit-sort-options.png)

* **Ordenar**
por Como os elementos devem ser ordenados
   * **Título**
   * **Última data de modificação**
* **Ordenação**
A ordem na qual os itens devem ser ordenados
   * **ascendente**
   * **descendente**
* **Máximo de**
itensNúmero máximo de itens exibidos na lista.
   * Deixe em branco para retornar todos os itens.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

### Guia Configurações do Item {#item-settings-tab}

Usando a guia Configurações de item , a formatação dos elementos da lista pode ser configurada.

![Configurações de item](/help/assets/list-edit-items.png)

* **Vincular**
itensVincular itens à página correspondente
* **Mostrar**
DescriçãoMostrar descrições do item de link
* **Mostrar**
DataMostrar data de modificação do item de link

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais tipos de listas devem ser permitidos para os autores de conteúdo, bem como as configurações de item disponíveis.

### Configurações da lista {#list-settings}

Na guia **List Settings** , o formato de data pode ser definido, bem como que tipo de lista deve estar disponível no componente para os autores de conteúdo.

![Configuração da lista de diálogo de design do componente de lista](/help/assets/list-design-list-settings.png)

* **Date**
FormatFormat a ser usado para a exibição da última data de modificação
* **Desativar**
filhosDesativar o tipo de lista de filhos no componente
* **Desativar**
estáticoDesative o tipo de lista estática no componente
* **Desativar**
pesquisaDesativar o tipo de lista de pesquisa no componente
* **Desativar**
tagsDesativar o tipo de lista de tags no componente

### Configurações do item {#item-settings}

Na guia **Configurações do item**, as opções de formatação para os elementos da lista individual que devem estar disponíveis no componente para os autores de conteúdo podem ser definidas.

![Listar configurações do item de diálogo de design do componente](/help/assets/list-design-item-settings.png)

* **Vincular**
itensHabilitar itens de link na caixa de diálogo de  [edição](#edit-dialog)
* **Mostrar**
descriçõesHabilite a opção Mostrar descrições na caixa de diálogo de  [edição](#edit-dialog)
* **Mostrar**
dataHabilitar opção Mostrar data na caixa de diálogo de  [edição](#edit-dialog)

### Guia Estilos {#styles-tab}

O Componente de imagem suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

## Camada de dados do cliente Adobe {#data-layer}

O Componente de lista oferece suporte à Camada de Dados do Cliente do Adobe.](/help/developing/data-layer/overview.md)[
