---
title: Componente de pesquisa rápida
description: O Componente de pesquisa rápida fornece recursos de pesquisa para um site e apresenta resultados de pesquisa para que os visitantes possam pesquisar no site e filtrar os resultados.
translation-type: tm+mt
source-git-commit: 65f900ad6759206a13f2bda6169900f62d968d8d

---


# Componente de pesquisa rápida {#quick-search-component}

O Componente de pesquisa rápida fornece recursos de pesquisa para um site e apresenta resultados de pesquisa para que os visitantes possam encontrar facilmente o conteúdo correspondente e visualizar os resultados.

## Uso {#usage}

O componente de Pesquisa rápida oferece aos visitantes do site a capacidade de pesquisar por conteúdo, exibir os resultados no local e navegar facilmente para as páginas correspondentes. Os novos resultados são obtidos dinamicamente à medida que o usuário rola os resultados da pesquisa.

A caixa de diálogo [de](#edit-dialog) edição permite que o autor do conteúdo defina onde a pesquisa deve iniciar na árvore de conteúdo. Usando a caixa de diálogo [de](#design-dialog)design, o autor do modelo pode definir o valor padrão para onde a pesquisa deve começar na árvore de conteúdo, bem como o tamanho máximo do conjunto de resultados e a duração mínima do termo de pesquisa.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de pesquisa rápida é v1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como um serviço em nuvem |
|--- |--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

A seguir está uma amostra retirada de [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

### Captura de tela {#screenshot}

![](assets/screen_shot_2018-01-19at094248.png)

### HTML {#html}

```
<section class="cmp-search" role="search" data-cmp-is="search" data-cmp-min-length="3" data-cmp-results-size="10">
    <form class="cmp-search__form" data-cmp-hook-search="form" method="get" action="/content/we-retail/us/en/equipment.searchresults.json/_jcr_content/root/responsivegrid/search" autocomplete="off">
        <div class="cmp-search__field">
            <i class="cmp-search__icon" data-cmp-hook-search="icon"></i>
            <span class="cmp-search__loading-indicator" data-cmp-hook-search="loadingIndicator"></span>
            <input class="cmp-search__input" data-cmp-hook-search="input" type="text" name="fulltext" placeholder="Search" role="combobox" aria-autocomplete="list" aria-haspopup="true" aria-invalid="false">
            <button class="cmp-search__clear" data-cmp-hook-search="clear">
                <i class="cmp-search__clear-icon"></i>
            </button>
        </div>
    </form>
    <div class="cmp-search__results" data-cmp-hook-search="results" role="listbox" aria-multiselectable="false"></div>
    
<script data-cmp-hook-search="itemTemplate" type="x-template">
    <a class="cmp-search__item" data-cmp-hook-search="item">
        <span class="cmp-search__item-title" data-cmp-hook-search="itemTitle"></span>
    </a>
</script>
</section>
```

### JSON {#json}

```
"search":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "relativePath":"/jcr:content/root/responsivegrid/search",
                     "resultsSize":10,
                     "searchTermMinimumLength":3,
                     ":type":"core/wcm/components/search/v1/search"
                  }
```

### Detalhes técnicos {#technical-details}

>[!NOTE]
>
>A proteção do componente de pesquisa ou de qualquer aplicativo baseado em AEM contra ataques de DOS deve ser implementada em um nível mais alto, por exemplo, usando `mod_security` o dispatcher.

A documentação técnica mais recente sobre o Componente de pesquisa rápida [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_search_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

## Edit Dialog {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo defina onde a pesquisa deve iniciar na árvore de conteúdo.

![](assets/screen_shot_2018-04-03at120132.png)

**Raiz** de pesquisa - a página raiz de onde iniciar a pesquisa. A Raiz de pesquisa pode ser uma página mestre de blueprint, mestre de idioma ou regular.

## Caixa de diálogo Design {#design-dialog}

Usando a caixa de diálogo de design, o autor do modelo pode definir o valor padrão para onde a pesquisa deve começar na árvore de conteúdo, bem como o tamanho máximo do conjunto de resultados e a duração mínima do termo de pesquisa. A caixa de diálogo de design permite que o autor do modelo defina quais opções de formatação de texto estão disponíveis para os autores do conteúdo.

### Guia Propriedades {#properties-tab}

![](assets/screen_shot_2018-04-03at120028.png)

* **Raiz** de pesquisa O valor padrão da raiz de pesquisa quando um autor de conteúdo coloca o Componente de pesquisa rápida em uma página de conteúdo
* **Tamanho** dos resultados O número máximo de resultados obtidos por uma solicitação de pesquisa
* **Duração** mínima do termo de pesquisa para iniciar a pesquisa

>[!NOTE]
>
>**Tamanho** dos resultados e Comprimento **mínimo do termo de** pesquisa podem ser definidos somente no modo de design e, portanto, somente no nível do modelo, o que significa que os autores de conteúdo não podem modificar esses valores.

>[!CAUTION]
>
>**O Tamanho** dos resultados e o Comprimento **mínimo do termo de** pesquisa podem ter impacto no desempenho se estiverem definidos muito altos ou muito baixos, respectivamente.

### Guia Estilos {#styles-tab}

O componente de pesquisa rápida suporta o AEM [Style System](authoring.md#component-styling).
