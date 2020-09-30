---
title: Listar Componente
description: O componente principal de Lista do componente permite a fácil criação de listas dinâmicas e estáticas.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Listar Componente{#list-component}

O componente principal de Lista do componente permite a fácil criação de listas dinâmicas e estáticas.

## Uso {#usage}

O Componente de Lista pode ser usado para criar, por exemplo, uma lista dinâmica de páginas filhas ou uma lista estática de itens definidos arbitrariamente. O tipo de listas disponíveis e as opções de formatação podem ser definidas pelo autor do modelo na caixa de diálogo [de](#design-dialog)design. O editor de conteúdo pode selecionar entre os tipos de lista disponíveis e como formatar os elementos de lista na caixa de diálogo [de](#edit-dialog)edição.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de Lista é a v2, que foi introduzida com a versão 2.0.0 dos Componentes Principais em janeiro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](v1/list-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de Lista e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_list)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de Lista [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_list_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Edit Dialog {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo configure os itens de lista e lista.

### Guia Configurações de lista {#list-settings-tab}

A lista pode ser construída de maneiras diferentes.

* [Páginas secundárias](#child-pages)
* [Lista fixa](#fixed-list)
* [Pesquisar](#search-options)
* [Tags](#tags)

Independentemente de como a lista é criada, há opções [de](#sort-options) classificação e ID que podem ser sempre configuradas.

![Caixa de diálogo de edição do componente de lista](/help/assets/list-edit.png)

Dependendo de como o autor do conteúdo escolher criar a lista, as opções de configuração adicionais serão alteradas.

#### Páginas filhas {#child-pages}

A lista pode ser criada a partir das páginas secundárias da página atual ou de outra página.

![Opções de página filho](/help/assets/list-edit-child-pages.png)

* **Página primário**
   * A página cujas páginas secundárias devem fazer a lista
   * Deixe em branco para usar a página atual

* **Profundidade-filho** Quantos níveis abaixo na hierarquia devem ser usados

#### Fixed List {#fixed-list}

A lista pode ser construída usando uma lista fixa de itens.

![Opções de lista corrigidas](/help/assets/list-edit-fixed.png)

Toque ou clique no botão **Adicionar** para inserir um novo item na lista.

* Insira o texto do item na lista ou use a caixa de diálogo **** de seleção para escolher um item da AEM.
* Use a alça de arrastar para reorganizar os itens na lista.
* Use o ícone da lixeira para excluir itens na lista.

#### Pesquisar {#search-options}

A lista pode ser criada usando os resultados de uma pesquisa de conteúdo AEM.

![Opções de lista de pesquisa](/help/assets/list-edit-search.png)

* **Query** de pesquisa A string para a qual uma pesquisa de texto completo será executada para gerar os elementos de lista
* **Pesquisar** Onde a pesquisa deve ser executada
   * Use a caixa de diálogo **** de seleção para escolher o local no AEM
   * Usar página atual se deixado em branco

#### Tags {#tags}

A lista pode ser criada usando páginas que correspondem a determinadas tags em um local específico.

![Opções de lista de tags](/help/assets/list-edit-tags.png)

* **Página** principalOnde a correspondência de tags deve ser start
   * Use a caixa de diálogo **** de seleção para escolher o local no AEM
   * Usar página atual se deixado em branco
* **Tags** Quais tags devem ser correspondidas
   * Use a caixa de diálogo **Procurar** para selecionar as tags
* **Correspondência** Define que tipo de correspondência deve qualificar uma página a ser incluída na lista
   * **qualquer tag**
   * **todas as tags**

#### Opções de classificação {#sort-options}

Independentemente de como você escolher criar a lista, há certas opções de classificação que podem ser sempre definidas.

![Opções de classificação](/help/assets/list-edit-sort-options.png)

* **Ordenar por** Como os elementos devem ser ordenados
   * **Título**
   * **Última data de modificação**
* **Ordem de classificação** A ordem na qual os itens devem ser ordenados
   * **ascendente**
   * **descendente**
* **Máximo de itens** Número máximo de itens exibidos na lista.
   * Deixe em branco para retornar todos os itens.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

### Guia Configurações do item {#item-settings-tab}

Usando a guia Configurações do item, a formatação dos elementos de lista pode ser configurada.

![Configurações de item](/help/assets/list-edit-items.png)

* **Vincular itens** Vincular itens à página correspondente
* **Mostrar descrição** Mostrar descrições do item do link
* **Mostrar data** Mostrar data de modificação do item de link

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais tipos de listas devem ser permitidos para os autores do conteúdo, bem como as configurações de item disponíveis.

### Configurações da lista {#list-settings}

Na guia Configurações **de** Lista, o formato de data pode ser definido, bem como que tipo de listas deve estar disponível no componente para os autores de conteúdo.

![Configuração da lista da caixa de diálogo de design do componente de lista](/help/assets/list-design-list-settings.png)

* **Formato** de data a ser usado para a exibição da última data de modificação
* **Desativar filhos** Desativar o tipo de lista filho no componente
* **Desabilitar estático** Desabilite o tipo de lista estática no componente
* **Desabilitar pesquisa** Desabilitar o tipo de lista de pesquisa no componente
* **Desativar tags** Desativar o tipo de lista de tags no componente

### Configurações do item {#item-settings}

Na guia Configurações **de** item, as opções de formatação dos elementos de lista individuais que devem estar disponíveis no componente para os autores de conteúdo podem ser definidas.

![Configurações do item de diálogo de design do Componente de lista](/help/assets/list-design-item-settings.png)

* **Vincular itens** Ativar itens de link na caixa de diálogo [Editar](#edit-dialog)
* **Mostrar descrições** Ativar a opção Mostrar descrições na caixa de diálogo de [edição](#edit-dialog)
* **Mostrar a opção de data** Ativar Mostrar data na caixa de diálogo de [edição](#edit-dialog)

### Guia Estilos {#styles-tab}

O Componente de imagem suporta o Sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
