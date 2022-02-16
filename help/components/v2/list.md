---
title: Componente de Lista (v2)
description: O componente de Lista, dos Componentes principais, permite criar com facilidade listas dinâmicas e estáticas.
role: Architect, Developer, Admin, User
source-git-commit: e5251010ca41025eb2bb56b66164ecf4cc0145c8
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 98%

---


# Componente de Lista (v2) {#list-component}

O componente de Lista, dos Componentes principais, permite criar com facilidade listas dinâmicas e estáticas.

## Uso {#usage}

O componente de Lista pode ser usado para criar, por exemplo, uma lista dinâmica de páginas secundárias ou uma lista estática de itens definidos arbitrariamente. O tipo de listas disponíveis e as opções de formatação podem ser definidas pelo autor do modelo na [caixa de diálogo de design](#design-dialog). O editor de conteúdo pode selecionar dentre os tipos de lista disponíveis e escolher como formatar os elementos da lista na [caixa de diálogo de edição](#edit-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente de lista, que foi introduzido com a versão 2.0.0 dos Componentes principais em janeiro de 2018.

>[!CAUTION]
>
>Este documento descreve a versão v2 do componente de Lista.
>
>Para obter detalhes sobre a versão atual do componente de Lista, consulte o documento [Componente de Lista](/help/components/list.md).

## Redirecionamentos em listas {#redirects}

Quando uma página tem um destino de redirecionamento (independentemente de estar apontando para um URL externo ou para outra página do AEM), uma lista que contém links para ele, aponta diretamente para o URL do destino de redirecionamento.

### Exemplo {#redirect-example}

* Crie uma página A que redirecione para a página B.
* Crie uma página C que redireciona para `https://aemcomponents.dev`
* Em uma página D, insira um componente de lista que contenha as páginas A e C
* Os respectivos links que são gerados, apontam diretamente para a página B e `https://aemcomponents.dev`

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Lista, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_list_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de Lista [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_list_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo configure a lista e os itens da lista.

### Guia Configurações de lista {#list-settings-tab}

A lista pode ser criada de maneiras diferentes.

* [Páginas secundárias](#child-pages)
* [Lista fixa](#fixed-list)
* [Pesquisar](#search-options)
* [Tags](#tags)

Independentemente de como a lista seja criada, há [Opções de Classificação e ID](#sort-options) que sempre podem ser configuradas.

![Caixa de diálogo de edição do componente de Lista](/help/assets/list-edit.png)

Dependendo de como o autor de conteúdo optar por criar a lista, as opções de configuração adicionais serão alteradas.

#### Páginas secundárias {#child-pages}

A lista pode ser criada das páginas secundárias da página atual ou de outra página.

![Opções de páginas secundárias](/help/assets/list-edit-child-pages.png)

* **Página primária**
   * A página cujas páginas secundárias devem fazer a lista
   * Deixe em branco para utilizar a página atual

* **Profundidade-secundária**
Quantos níveis abaixo da hierarquia devem ser usados

#### Lista fixa {#fixed-list}

A lista pode ser criada usando uma lista fixa de itens.

![Opções de lista fixa](/help/assets/list-edit-fixed.png)

Toque ou clique no botão **Adicionar** para inserir um novo item à lista.

* Insira o texto para o item na lista ou use a **caixa de diálogo de Seleção** para escolher um item do AEM.
* Use a alça de arrastar para reorganizar os itens na lista.
* Use o ícone da lixeira para excluir itens na lista.

#### Pesquisar {#search-options}

A lista pode ser criada usando os resultados de uma pesquisa de conteúdo AEM.

![Pesquisar opções de listas](/help/assets/list-edit-search.png)

* **Pesquisar consulta**
A sequência de caracteres para a qual uma pesquisa de texto completo será executada para gerar os elementos da lista
* **Pesquisar em**
Onde a pesquisa deve ser executada
   * Use a **caixa de diálogo de seleção** para escolher o local no AEM
   * Use página atual se deixado em branco

#### Tags {#tags}

A lista pode ser criada usando páginas que correspondem a determinadas tags em um determinado local.

![Opções da lista de tags](/help/assets/list-edit-tags.png)

* **Página principal**
Onde a correspondência de tags deve começar
   * Use a **caixa de diálogo de seleção** para escolher o local no AEM
   * Use página atual se deixado em branco
* **Tags**
Quais tags devem ser correspondidas
   * Use a caixa de diálogo **Procurar** para selecionar as tags
* **Correspondência**
Define que tipo de correspondência deve qualificar uma página a ser incluída na lista
   * **qualquer tag**
   * **todas as tags**

#### Opções de classificação {#sort-options}

Independentemente de como você optar por criar a lista, há certas opções de classificação que sempre podem ser definidas.

![Opções de classificação](/help/assets/list-edit-sort-options.png)

* **Ordenar por**
Como os elementos devem ser ordenados
   * **Título**
   * **Última data de modificação**
* **Ordem de classificação**
A ordem na qual os itens devem ser ordenados
   * **ascendente**
   * **descendente**
* **Número máximo de itens** - Número máximo de itens exibidos na lista.
   * Deixe em branco para retornar todos os itens.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Guia Configurações de itens {#item-settings-tab}

Usando a guia Configurações de item, a formatação dos elementos da lista pode ser configurada.

![Configurações do item](/help/assets/list-edit-items.png)

* **Vincular itens**
Vincula itens à página correspondente.
* **Mostrar descrição**
Mostra descrições do item de link
* **Mostrar data**
Mostra a data de modificação do item de link.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais tipos de listas devem ser liberadas para os autores de conteúdo, bem como as configurações de item disponíveis.

### Configurações da lista {#list-settings}

Na guia **Configurações da lista**, o formato da data pode ser definido, bem como o tipo de listas que deve estar disponível no componente para os autores de conteúdo.

![Configuração da lista da caixa de diálogo de design do componente de Lista](/help/assets/list-design-list-settings.png)

* **Formato da data** - Formato a ser usado na exibição da última data de modificação.
* **Desativar secundárias**
Desativa o tipo de listas secundárias no componente.
* **Desativar estática**
Desativa o tipo de lista estática no componente.
* **Desativar pesquisa**
Desativa o tipo de lista de pesquisa no componente.
* **Desativar tags**
Desativa o tipo de lista de tags no componente.

### Configurações do item {#item-settings}

Na guia **Configurações do item**, as opções de formatação para os elementos da lista individual que devem estar disponíveis no componente para os autores de conteúdo podem ser definidas.

![Configuração da lista da caixa de diálogo de design do componente de Lista](/help/assets/list-design-item-settings.png)

* **Vincular itens**
Habilita a opção Vincular itens na [caixa de diálogo de edição](#edit-dialog).
* **Mostrar descrições**
Habilita a opção Mostrar descrições na [caixa de diálogo de edição](#edit-dialog).
* **Mostrar data**
Habilita a opção Mostrar data na [caixa de diálogo de edição](#edit-dialog).

### Guia Estilos {#styles-tab}

O componente de Imagem é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de lista oferece suporte à [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
