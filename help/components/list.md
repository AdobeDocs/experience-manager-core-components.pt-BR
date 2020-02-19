---
title: Listar Componente
description: O Componente principal de lista de componentes permite a fácil criação de listas dinâmicas e estáticas.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Listar Componente{#list-component}

O Componente principal de lista de componentes permite a fácil criação de listas dinâmicas e estáticas.

## Uso {#usage}

O Componente de lista pode ser usado para criar, por exemplo, uma lista dinâmica de páginas secundárias ou uma lista estática de itens definidos arbitrariamente. O tipo de listas disponíveis e as opções de formatação podem ser definidas pelo autor do modelo na caixa de diálogo [de](#design-dialog)design. O editor de conteúdo pode selecionar entre os tipos de lista disponíveis e como formatar os elementos da lista na caixa de diálogo [de](#edit-dialog)edição.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de lista é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível | Compatível |
| [v1](v1/list-v1.md) | Compatível | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](/help/versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o componente de lista e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_list)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de lista [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_list_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Edit Dialog {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo configure a lista e os itens da lista.

### Guia Configurações de lista {#list-settings-tab}

A lista pode ser criada de diferentes maneiras.

* [Páginas secundárias](#child-pages)
* [Lista fixa](#fixed-list)
* [Pesquisar](#search-options)
* [Tags](#tags)

Independentemente de como a lista é criada, há opções [de](#sort-options) classificação que podem ser sempre configuradas.

![](/help/assets/chlimage_1-38.png)

Dependendo de como o autor do conteúdo escolher criar a lista, as opções de configuração adicionais serão alteradas.

#### Páginas filhas {#child-pages}

A lista pode ser criada a partir das páginas secundárias da página atual ou de outra página.

![](/help/assets/chlimage_1-39.png)

* **Página primário**
   * A página cujas páginas secundárias devem fazer a lista
   * Deixe em branco para usar a página atual

* **Profundidade-filho** Quantos níveis abaixo na hierarquia devem ser usados

#### Fixed List {#fixed-list}

A lista pode ser criada usando uma lista fixa de itens.

![](/help/assets/chlimage_1-40.png)

Toque ou clique no botão **Adicionar** para inserir um novo item na lista.

* Digite o texto do item na lista ou use a caixa de diálogo **** de seleção para escolher um item do AEM.
* Use a alça de arrastar para reorganizar os itens na lista.
* Use o ícone da lixeira para excluir itens na lista.

#### Pesquisar {#search-options}

A lista pode ser criada usando os resultados de uma pesquisa de conteúdo do AEM.

![](/help/assets/chlimage_1-41.png)

* **Consulta** de pesquisa A string para a qual uma pesquisa de texto completo será executada para gerar os elementos de lista
* **Pesquisar** Onde a pesquisa deve ser executada
   * Use a caixa de diálogo **** de seleção para escolher o local no AEM
   * Usar página atual se deixado em branco

#### Tags {#tags}

A lista pode ser criada usando páginas que correspondem a determinadas tags em um local específico.

![](/help/assets/chlimage_1-42.png)

* **Página** principalOnde a correspondência de tags deve começar
   * Use a caixa de diálogo **** de seleção para escolher o local no AEM
   * Usar página atual se deixado em branco
* **Tags** Quais tags devem ser correspondidas
   * Use a caixa de diálogo **Procurar** para selecionar as tags
* **Correspondência** Define que tipo de correspondência deve qualificar uma página a ser incluída na lista
   * **qualquer tag**
   * **todas as tags**

#### Opções de classificação {#sort-options}

Independentemente de como você escolher criar a lista, há certas opções de classificação que podem ser sempre definidas.

![](/help/assets/chlimage_1-43.png)

* **Ordenar por** Como os elementos devem ser ordenados
   * **Título**
   * **Última data de modificação**
* **Ordem de classificação** A ordem na qual os itens devem ser ordenados
   * **ascendente**
   * **descendente**
* **Máximo de itens** Número máximo de itens exibidos na lista.
   * Deixe em branco para retornar todos os itens.

### Guia Configurações do item {#item-settings-tab}

Usando a guia Configurações do item, a formatação dos elementos da lista pode ser configurada.

![](/help/assets/chlimage_1-44.png)

* **Vincular itens** Vincular itens à página correspondente
* **Mostrar descrição** Mostrar descrições do item do link
* **Mostrar data** Mostrar data de modificação do item de link

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais tipos de listas devem ser permitidos para os autores do conteúdo, bem como as configurações de item disponíveis.

### Configurações da lista {#list-settings}

Na guia Configurações **da** lista, o formato de data pode ser definido, bem como que tipo de listas deve estar disponível no componente para os autores de conteúdo.

![](/help/assets/chlimage_1-45.png)

* **Formato** de data a ser usado para a exibição da última data de modificação
* **Desativar filhos** Desativar o tipo de lista de filhos no componente
* **Desativar estática** Desativar o tipo de lista estática no componente
* **Desabilitar pesquisa** Desabilitar o tipo de lista de pesquisa no componente
* **Desativar tags** Desativar o tipo de lista de tags no componente

### Configurações do item {#item-settings}

Na guia Configurações **de** item, as opções de formatação dos elementos de lista individuais que devem estar disponíveis no componente para os autores de conteúdo podem ser definidas.

![](/help/assets/chlimage_1-46.png)

* **opção Vincular itens** Ativar itens de link na caixa de diálogo [Editar](#edit-dialog)
* **Mostrar descrições** Ativar a opção Mostrar descrições na caixa de diálogo [editar](#edit-dialog)
* **Mostrar a opção Data** para mostrar data na caixa de diálogo [editar](#edit-dialog)

### Guia Estilos {#styles-tab}

O componente de imagem suporta o sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
