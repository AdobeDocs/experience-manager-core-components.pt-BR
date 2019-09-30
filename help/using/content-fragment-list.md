---
title: Componente da lista de fragmentos do conteúdo
seo-title: Componente da lista de fragmentos do conteúdo
description: 'null'
seo-description: O componente principal Lista de fragmentos de conteúdo do componente permite a exibição de uma lista de fragmentos de conteúdo.
contentOwner: bohnerd
content-type: referência
topic-tags: autoria
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
translation-type: tm+mt
source-git-commit: 6882a0d8247328c403dc11a25ed9d079aefede69

---


# Componente da lista de fragmentos do conteúdo{#content-fragment-list-component}

O componente principal Lista de fragmentos de conteúdo do componente permite a exibição de uma lista de fragmentos [de](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html)conteúdo.

## Uso {#usage}

O componente principal da lista de fragmentos de conteúdo do componente permite a inclusão de uma lista de fragmentos [de](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html) conteúdo em uma página com base em um modelo de fragmento de conteúdo. Isso pode ser especialmente útil para criar conteúdo [](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) sem cabeçalho que possa ser facilmente consumido por outros aplicativos.

* A lista e suas propriedades podem ser selecionadas na caixa de diálogo [](#configure-dialog)configurar.
* Os estilos podem ser aplicados ao componente na caixa de diálogo [de](#design-dialog)design.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de fragmento de conteúdo é a v1, que foi introduzida com a versão 2.4.0 dos Componentes principais em maio de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de lista de fragmentos de conteúdo e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment-list.html)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente da lista de fragmentos de conteúdo [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/contentfragmentlist/v1/contentfragmentlist).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina os fragmentos de conteúdo que compõem a lista e os elementos desses fragmentos que serão incluídos.

### Guia Propriedades

A guia **Propriedades** define quais Fragmentos de conteúdo são incluídos na lista. Isso se baseia principalmente em um Modelo de fragmento de conteúdo selecionado, mas há outras opções de filtro disponíveis.

![](assets/screen-shot-2019-09-25-10.32.10.png)

* **Modelo** - Caminho para o modelo de fragmento do conteúdo no qual a lista se baseia.
   * Por padrão, todos os fragmentos de conteúdo do modelo definidos como Caminho **** do modelo são incluídos na lista.
* **Caminho** principal - Caminho principal a partir do qual a lista deve ser criada.
   * Os fragmentos de conteúdo com base no Caminho **do** modelo selecionado serão filtrados para os do Caminho **** principal especificado.
      * Clique ou toque no botão **Abrir caixa de diálogo** de seleção no lado direito do campo para especificar o caminho.
* **Tags** - somente os Fragmentos de conteúdo com as tags especificadas serão incluídos na lista.
   * Clique ou toque no botão **Abrir caixa de diálogo** de seleção no lado direito do campo para especificar as tags.
   * Clique ou toque no X ao lado das tags selecionadas para removê-las.
* **Ordenar por** - Campo do modelo de fragmento de conteúdo pelo qual a lista será ordenada
   * Somente os campos de texto (incluindo numérico, data e hora) são selecionáveis.
* **Ordem** de classificação - Como a lista será classificada pelo campo **Ordenar por**
   * Crescente ou decrescente
* **Máximo de itens** - Número máximo de itens a serem exibidos na lista
   * Nenhum valor retornará todos os itens.

>[!NOTE]
>As opções **Pedido por**, **Ordem** de classificação e Itens **** máximos foram apresentadas com a versão 2.7.0 dos Componentes principais.

### Guia Elementos

Por padrão, todos os elementos do Modelo de fragmento de conteúdo serão incluídos na lista (a menos que limitado pelo campo Itens **** máximos). A guia **Elementos** permite que você especifique apenas elementos específicos a serem incluídos.

![](assets/screen-shot-2019-05-08-10.47.34.png)

* **Elementos** - somente os elementos dos fragmentos de conteúdo na lista especificada serão exibidos.
   * Clique ou toque no botão **Adicionar** para adicionar um novo elemento.
   * Clique ou toque no botão **Excluir** para remover um elemento selecionado.
   * Arraste a alça **Ordem** para reorganizar a ordem dos elementos.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os estilos aplicados ao Componente de lista de fragmentos do conteúdo.
