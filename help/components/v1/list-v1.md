---
title: Componente de lista (v1)
description: O Componente de lista de componentes principais permite a criação fácil de listas dinâmicas e estáticas.
index: n
role: Arquiteto, Desenvolvedor, Administrador, Praticante de negócios
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 4%

---


# Componente de lista (v1) {#list-component-v}

O Componente de lista de componentes principais permite a criação fácil de listas dinâmicas e estáticas.

## Uso {#usage}

O Componente de lista pode ser usado para criar, por exemplo, uma lista dinâmica de páginas filhas ou uma lista estática de itens definidos arbitrariamente.

O tipo de listas disponíveis e as opções de formatação podem ser definidas pelo autor do modelo na caixa de diálogo [design](#design-dialog). O editor de conteúdo pode selecionar entre os tipos de lista disponíveis e como formatar os elementos da lista no [diálogo de edição](#edit-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente de lista, introduzido originalmente com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do Componente de lista.

| Versão do AEM | Componente de lista v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve v1 do Componente de lista.
>
>Para obter detalhes sobre a versão atual do Componente de lista, consulte o documento [Componente de lista](/help/components/list.md).

## Saída de componente de exemplo {#sample-component-output}

A amostra a seguir é retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](/help/assets/chlimage_1-47.png)

### HTML {#html}

```
<div class="cmp cmp-list aem-GridColumn aem-GridColumn--default--12">

<ul>
    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/arctic-surfing-in-lofoten.html">
            <span class="cmp-list--item-title">Arctic Surfing In Lofoten</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/summit-success-in-the-himalayas.html">
            <span class="cmp-list--item-title">Summit Success in the Himalayas</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-on-kalymnos-island--greece.html">
            <span class="cmp-list--item-title">Climbing on Kalymnos Island, Greece</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/running-at-the-great-wall-marathon.html">
            <span class="cmp-list--item-title">Running at the Great Wall Marathon</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/skiing-deep-powder-in-siberia.html">
            <span class="cmp-list--item-title">Skiing deep powder in Siberia</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-in-the-massif-du-mont-blanc.html">
            <span class="cmp-list--item-title">Climbing in the Massif du Mont Blanc</span>
            
        </a>
        
    </article>
</li>
</ul>

</div>
```

### JSON {#json}

```
"articles_list": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/articleslist",
              "tagsMatch": "any",
              "displayAs": "teaser",
              "feedEnabled": "true",
              "listFrom": "children",
              "limit": "0",
              "orderBy": "cq:lastModified",
              "pageMax": "0"
            }
```

>[!NOTE]
>
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Editar Caixa de Diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo configure a lista e os elementos da lista.

### Configurações da lista {#list-settings}

A lista pode ser criada de maneiras diferentes.

* [Páginas secundárias](#child-pages)
* [Lista fixa](#fixed-list)
* [Pesquisar](#search-list)
* [Tags](#tags)

Independentemente de como a lista é criada, há [Opções de Classificação](#sort-options) que podem ser sempre configuradas.

![](/help/assets/chlimage_1-38.png)

Dependendo de como o autor de conteúdo optar por criar a lista, as opções de configuração adicionais serão alteradas.

#### Páginas filhas {#child-pages}

A lista pode ser criada das páginas filhas da página atual ou de outra página.

![](/help/assets/chlimage_1-39.png)

* **Página primário**
   * A página cujas páginas secundárias devem fazer a lista
   * Deixe em branco para usar a página atual
* **Profundidade do filho**  - Quantos níveis abaixo na hierarquia devem ser usados

#### Lista fixa {#fixed-list}

A lista pode ser criada usando uma lista fixa de itens.

![](/help/assets/chlimage_1-40.png)

Toque ou clique no botão **Add** para inserir um novo item à lista.

* Insira o texto para o item na lista ou use a **Caixa de Diálogo de Seleção** para escolher um item do AEM.
* Use a alça de arrastar para reorganizar os itens na lista.
* Use o ícone da lixeira para excluir itens na lista.

#### Pesquisar {#search-list}

A lista pode ser criada usando os resultados de uma pesquisa de conteúdo AEM.

![](/help/assets/chlimage_1-41.png)

* **Consulta de pesquisa**  - a sequência de caracteres para a qual uma pesquisa de texto completo será executada para gerar os elementos da lista
* **Pesquisar no**  - Onde a pesquisa deve ser executada
   * Use a caixa de diálogo **Seleção** para escolher o local no AEM
   * Usar página atual se deixado em branco

#### Tags {#tags}

A lista pode ser criada usando páginas que correspondem a determinadas tags em um determinado local.

![](/help/assets/chlimage_1-42.png)

* **Página principal**  - Onde a correspondência de tags deve começar
   * Use a caixa de diálogo **Seleção** para escolher o local no AEM
   * Usar página atual se deixado em branco
* **Tags**  - Quais tags devem ser correspondidas
   * Use a caixa de diálogo **Procurar** para selecionar as tags
* **Correspondência**  - Defina que tipo de correspondência deve qualificar uma página para ser incluída na lista
   * **qualquer tag**
   * **todas as tags**

#### Opções de classificação {#sort-options}

Independentemente de como você optar por criar a lista, há certas opções de classificação que podem sempre ser definidas.

![](/help/assets/chlimage_1-43.png)

* **Ordenar por**  - Como os elementos devem ser ordenados
   * **Título**
   * **Última data de modificação**
* **Ordem de Classificação**  - A ordem na qual os itens devem ser ordenados
   * **ascendente**
   * **descendente**
* **Máximo de itens**  - Número máximo de itens exibidos na lista.
   * Deixe em branco para retornar todos os itens.

### Configurações do item {#item-settings}

Usando a guia **Item Settings**, a formatação dos elementos da lista pode ser configurada.

![](/help/assets/chlimage_1-44.png)

* **Vincular**
itensVincular itens à página correspondente
* **Mostrar**
DescriçãoMostrar descrições do item de link
* **Mostrar**
DataMostrar data de modificação do item de link

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais tipos de listas devem ser permitidos para os autores de conteúdo, bem como as configurações de item disponíveis.

### Configurações da lista {#list-settings-1}

Na guia **List Settings** , o formato de data pode ser definido, bem como que tipo de lista deve estar disponível no componente para os autores de conteúdo.

![](/help/assets/chlimage_1-45.png)

* **Formato de data**  - Formato a ser usado para a exibição da última data de modificação
* **Desativar filhos**  - Desative o tipo de lista de filhos no componente
* **Desativar estático**  - Desative o tipo de lista estática no componente
* **Desativar pesquisa**  - Desative o tipo de lista de pesquisa no componente
* **Desativar tags**  - Desativar o tipo de lista de tags no componente

### Configurações do item {#item-settings-1}

Na guia **Configurações do item**, as opções de formatação para os elementos da lista individual que devem estar disponíveis no componente para os autores de conteúdo podem ser definidas.

![](/help/assets/chlimage_1-46.png)

* **Itens de link**  - opção Habilitar itens de link na caixa de diálogo de  [edição](#edit-dialog)
* **Mostrar descrições**  - Habilite a opção Mostrar descrições na caixa de diálogo de  [edição](#edit-dialog)
* **Mostrar data**  - Ativar a opção Mostrar data na caixa de diálogo de  [edição](#edit-dialog)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de lista [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

O projeto de componentes principais inteiro pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
