---
title: Componente de lista do fragmento do conteúdo
seo-title: Componente de lista do fragmento do conteúdo
description: 'null'
seo-description: O componente de Lista de fragmentos do conteúdo do componente principal permite a exibição de uma lista de fragmentos de conteúdo.
contentOwner: bohnert
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
translation-type: tm+mt
source-git-commit: d683f8110b514860bba11e08e6923be49e92652f

---


# Componente de lista do fragmento do conteúdo{#content-fragment-list-component}

O componente de Lista de fragmentos do conteúdo do componente principal permite a exibição de uma lista de [fragmentos de conteúdo](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html).

## Uso {#usage}

O componente de lista do fragmento do conteúdo principal do componente permite a inclusão de uma lista de fragmentos [de conteúdo](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html) em uma página com base em um modelo de fragmento do conteúdo. Isso pode ser especialmente útil para criar [conteúdo sem título](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) que pode ser facilmente consumido por outros aplicativos.

* A lista e suas propriedades podem ser selecionadas na caixa de diálogo [Configurar](#configure-dialog).
* Estilos podem ser aplicados ao componente na caixa de diálogo [de design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do fragmento do conteúdo é v 1, que foi introduzida com a versão 2.4.0 dos Componentes principais em maio de 2019 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente de lista de fragmentos do conteúdo, bem como ver exemplos de suas opções de configuração, além de HTML e saída JSON, visite a Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment-list.html).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente da lista de fragmentos do conteúdo [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/contentfragmentlist/v1/contentfragmentlist).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo defina a lista que os fragmentos do conteúdo contêm e os elementos desses fragmentos a serem incluídos.

### Guia Propriedades

A guia **Propriedades** define quais Fragmentos de conteúdo são incluídos na lista. Isso se baseia principalmente em um Modelo de fragmento de conteúdo selecionado, mas há outras opções de filtro disponíveis.

![](assets/screen-shot-2019-05-08-10.47.19.png)

* **Modelo** - Caminho para o Modelo de fragmento do conteúdo no qual a lista se baseia.
   * Por padrão, todos os fragmentos de conteúdo do modelo definido como **Caminho** do modelo são incluídos na lista.
* **Caminho pai** - caminho pai do qual a lista deve ser criada.
   * Os fragmentos de conteúdo baseados no Caminho **de modelo selecionado** serão filtrados para aqueles no Caminho **pai especificado**.
   * Clique ou toque no **botão Abrir caixa de diálogo** de seleção no lado direito do campo para especificar o caminho.
* **Tags** - somente os Fragmentos de conteúdo com as tags especificadas serão incluídos na lista.
   * Clique ou toque no **botão Abrir caixa de diálogo** de seleção no lado direito do campo para especificar as tags.
   * Clique ou toque no X ao lado das tags selecionadas para removê-las.


### Guia Elementos

Por padrão, todos os elementos do Modelo de fragmento do conteúdo serão incluídos na lista. Os **Elementos** permitem especificar somente elementos específicos a serem incluídos.

![](assets/screen-shot-2019-05-08-10.47.34.png)

* **Elementos** - somente os elementos dos fragmentos do conteúdo na lista especificada serão exibidos.
   * Clique ou toque no botão **Adicionar** para adicionar um novo elemento
   * Clique ou toque no **botão Excluir** para remover um elemento selecionado
   * Arraste a **alça Ordem** para reorganizar a ordem dos elementos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os estilos aplicados ao Componente da lista de fragmentos do conteúdo.