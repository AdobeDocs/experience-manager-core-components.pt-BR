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
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Listar Componente{#list-component}

O Componente de lista de componentes principais permite a fácil criação de listas dinâmicas e estáticas.

## Uso {#usage}

O componente de lista pode ser usado para criar, por exemplo, uma lista dinâmica de páginas filhas ou uma lista estática de itens arbitrários. O tipo de lista disponível e as opções de formatação podem ser definidas pelo autor do modelo na caixa de diálogo [de design](#design-dialog). O editor de conteúdo pode selecionar entre tipos de lista disponíveis e como formatar os elementos da lista na janela de [edição](#edit-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de lista é v 2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatível | Compatível | Compatível |
| [v1](list-v1.md) | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/screen_shot_2018-01-12at105924.png)

### Biblioteca de componentes

Para experimentar o Componente de lista, bem como ver exemplos de suas opções de configuração, além de HTML e saída JSON, visite a Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/list.html).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de lista [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo Editar permite que o autor do conteúdo configure a lista e os itens da lista.

### Guia Configurações da lista {#list-settings-tab}

A lista pode ser criada de maneiras diferentes.

* [Páginas secundárias](#child-pages)
* [Lista fixa](#fixed-list)
* [Pesquisar](#search-options)
* [Tags](#tags)

Independentemente de como a lista é construída, há Opções [de classificação](#sort-options) que podem sempre ser configuradas.

![](assets/chlimage_1-38.png)

Dependendo de como o autor do conteúdo decide criar a lista, as opções de configuração adicionais serão alteradas.

#### Páginas filhas {#child-pages}

A lista pode ser criada das páginas secundárias da página atual ou de outra página.

![](assets/chlimage_1-39.png)

* **Página primário**
   * A página cujas páginas secundárias devem fazer a lista
   * Deixe em branco para usar a página atual

* **Profundidade secundária** Quantos níveis na hierarquia devem ser usados

#### Lista fixa {#fixed-list}

A lista pode ser criada usando uma lista fixa de itens.

![](assets/chlimage_1-40.png)

Toque ou clique no **botão Adicionar** para inserir um novo item na lista.

* Digite o texto para o item na lista ou use a caixa de diálogo **de Seleção** para escolher um item do AEM.
* Use a alça de arrastar para reorganizar os itens na lista.
* Use o ícone de lixeira para excluir itens na lista.

#### Pesquisar {#search-options}

A lista pode ser criada usando os resultados da pesquisa de conteúdo AEM.

![](assets/chlimage_1-41.png)

* **Pesquisar consulta**
A cadeia de caracteres para a qual uma pesquisa de texto completa será executada para gerar os elementos da lista
* **Pesquisar em**
onde a pesquisa deve ser executada
   * Usar a caixa de diálogo **de seleção** para escolher o local no AEM
   * Usar a página atual se deixado em branco

#### Tags {#tags}

A lista pode ser criada usando páginas que correspondem a determinadas tags em um determinado local.

![](assets/chlimage_1-42.png)

* **Página
principal** Onde a correspondência da tag deve ser iniciada
   * Usar a caixa de diálogo **de seleção** para escolher o local no AEM
   * Usar a página atual se deixado em branco
* **Tags**
que devem ser correspondidas
   * Usar a caixa de diálogo **Procurar** para selecionar as tags
* **Corresponder**
define que tipo de correspondência deve qualificar uma página a ser incluída na lista
   * **qualquer tag**
   * **todas as tags**

#### Opções de classificação {#sort-options}

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

### Guia Configurações de item {#item-settings-tab}

Usando a guia Configurações do item, é possível configurar a formatação dos elementos da lista.

![](assets/chlimage_1-44.png)

* **Itens do link Vincular itens**
à página correspondente
* **Mostrar descrição**
Exibir descrições do item do link
* **Mostrar data de modificação**Mostrar data
do item do link

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais tipos de listas devem ser permitidas aos autores de conteúdo, bem como as configurações de item disponíveis.

### Configurações da lista {#list-settings}

Na guia **Configurações** da lista, o formato de data pode ser definido, bem como que tipo de lista deve estar disponível no componente para os autores de conteúdo.

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

Na guia **Configurações** do item, as opções de formatação para os elementos de lista individuais que devem estar disponíveis no componente para os autores de conteúdo podem ser definidas.

![](assets/chlimage_1-46.png)

* **Itens do link**
Ativar itens do link na caixa de diálogo [Editar](#edit-dialog)
* **Mostrar descrição**
ativar a opção Exibir descrições na janela [de edição](#edit-dialog)
* **Mostrar a**
opção Ativar data mostrar data na janela [de edição](#edit-dialog)

### Guia Estilos {#styles-tab}

O componente de imagem é compatível com o Sistema [de estilo AEM](authoring.md#component-styling).