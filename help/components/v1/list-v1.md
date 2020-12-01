---
title: Componente de lista (v1)
description: O componente principal de Lista do componente permite a fácil criação de listas dinâmicas e estáticas.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 4%

---


# Componente de lista (v1) {#list-component-v}

O componente principal de Lista do componente permite a fácil criação de listas dinâmicas e estáticas.

## Uso {#usage}

O Componente de Lista pode ser usado para criar, por exemplo, uma lista dinâmica de páginas filhas ou uma lista estática de itens definidos arbitrariamente.

O tipo de listas disponíveis e as opções de formatação podem ser definidas pelo autor do modelo na caixa de diálogo [design](#design-dialog). O editor de conteúdo pode selecionar entre os tipos de lista disponíveis e como formatar os elementos de lista na caixa de diálogo [edit](#edit-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente da Lista, originalmente introduzido com a versão 1.0.0 dos Componentes principais com a AEM 6.3.

A tabela a seguir lista a compatibilidade de v1 do Componente de Lista.

| Versão do AEM | Componente de lista v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do Componente de Lista.
>
>Para obter detalhes sobre a versão atual do Componente de Lista, consulte o documento [Componente de Lista](/help/components/list.md).

## Exemplo de saída do componente {#sample-component-output}

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
>A exportação JSON dos Componentes principais exige a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo configure os elementos de lista e lista.

### Configurações da lista {#list-settings}

A lista pode ser construída de maneiras diferentes.

* [Páginas secundárias](#child-pages)
* [Lista fixa](#fixed-list)
* [Pesquisar](#search-list)
* [Tags](#tags)

Independentemente de como a lista é criada, há [Opções de classificação](#sort-options) que podem ser sempre configuradas.

![](/help/assets/chlimage_1-38.png)

Dependendo de como o autor do conteúdo escolher criar a lista, as opções de configuração adicionais serão alteradas.

#### Páginas filhas {#child-pages}

A lista pode ser criada a partir das páginas secundárias da página atual ou de outra página.

![](/help/assets/chlimage_1-39.png)

* **Página primário**
   * A página cujas páginas secundárias devem fazer a lista
   * Deixe em branco para usar a página atual
* **Profundidade** -filho - Quantos níveis abaixo na hierarquia devem ser usados

#### Lista fixa {#fixed-list}

A lista pode ser construída usando uma lista fixa de itens.

![](/help/assets/chlimage_1-40.png)

Toque ou clique no botão **Adicionar** para inserir um novo item na lista.

* Insira o texto do item na lista ou use a **Caixa de diálogo de seleção** para escolher um item da AEM.
* Use a alça de arrastar para reorganizar os itens na lista.
* Use o ícone da lixeira para excluir itens na lista.

#### Pesquisar {#search-list}

A lista pode ser criada usando os resultados de uma pesquisa de conteúdo AEM.

![](/help/assets/chlimage_1-41.png)

* **Query**  de pesquisa - a string para a qual uma pesquisa de texto completo será executada para gerar os elementos de lista
* **Pesquisar**  - Onde a pesquisa deve ser executada
   * Use a caixa de diálogo **Seleção** para escolher o local no AEM
   * Usar página atual se deixado em branco

#### Tags {#tags}

A lista pode ser criada usando páginas que correspondem a determinadas tags em um local específico.

![](/help/assets/chlimage_1-42.png)

* **Página**  principal - Onde a correspondência de tags deve ser start
   * Use a caixa de diálogo **Seleção** para escolher o local no AEM
   * Usar página atual se deixado em branco
* **Tags**  - Quais tags devem ser correspondidas
   * Use a caixa de diálogo **Procurar** para selecionar as tags
* **Correspondência**  - Defina o tipo de correspondência que deve qualificar uma página a ser incluída na lista
   * **qualquer tag**
   * **todas as tags**

#### Opções de classificação {#sort-options}

Independentemente de como você escolher criar a lista, há certas opções de classificação que podem ser sempre definidas.

![](/help/assets/chlimage_1-43.png)

* **Ordenar por** - Como os elementos devem ser ordenados
   * **Título**
   * **Última data de modificação**
* **Ordem**  de Classificação - A ordem na qual os itens devem ser ordenados
   * **ascendente**
   * **descendente**
* **Máximo de itens**  - Número máximo de itens exibidos na lista.
   * Deixe em branco para retornar todos os itens.

### Configurações do item {#item-settings}

Usando a guia **Configurações do item**, a formatação dos elementos de lista pode ser configurada.

![](/help/assets/chlimage_1-44.png)

* **Vincular**
itensVincular itens à página correspondente
* **Mostrar**
descriçãoMostrar descrições do item do link
* **Mostrar**
dataMostrar data de modificação do item de link

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais tipos de listas devem ser permitidos para os autores do conteúdo, bem como as configurações de item disponíveis.

### Configurações da lista {#list-settings-1}

Na guia **Configurações de Lista**, o formato de data pode ser definido, bem como o tipo de listas que deve estar disponível no componente para os autores de conteúdo.

![](/help/assets/chlimage_1-45.png)

* **Formato**  de data - Formato a ser usado para a exibição da última data de modificação
* **Desativar filhos**  - Desabilitar o tipo de lista filho no componente
* **Disable Static (Desativar estático** ) - Desative o tipo de lista estática no componente
* **Desabilitar pesquisa**  - Desabilitar o tipo de lista de pesquisa no componente
* **Desativar tags**  - Desativar o tipo de lista de tags no componente

### Configurações do item {#item-settings-1}

Na guia **Configurações do item**, as opções de formatação dos elementos de lista individuais que devem estar disponíveis no componente para os autores do conteúdo podem ser definidas.

![](/help/assets/chlimage_1-46.png)

* **Itens**  de link - opção Ativar itens de link na caixa de diálogo  [de edição](#edit-dialog)
* **Mostrar descrições**  - Ativar a opção Mostrar descrições na caixa de diálogo  [editar](#edit-dialog)
* **Mostrar data**  - Ativar a opção Mostrar data na caixa de diálogo  [editar](#edit-dialog)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de Lista [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

Todo o projeto de componentes principais pode ser baixado do GitHub.

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
