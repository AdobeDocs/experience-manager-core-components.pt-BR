---
title: Componente da lista de fragmentos do conteúdo
description: O componente Lista de fragmentos do conteúdo do componente principal permite a exibição de uma lista de fragmentos de conteúdo.
role: Arquiteto, Desenvolvedor, Administrador, Praticante de negócios
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 5%

---


# Componente da lista de fragmentos de conteúdo{#content-fragment-list-component}

O componente Lista de fragmentos do conteúdo do componente principal permite a exibição de uma lista de [fragmentos de conteúdo](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

## Uso {#usage}

O Componente de lista de fragmentos de conteúdo do componente principal permite a inclusão de uma lista de [fragmentos de conteúdo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) em uma página com base em um modelo de Fragmento de conteúdo. Isso pode ser especialmente útil para criar [conteúdo sem periféricos](https://helpx.adobe.com/br/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) que podem ser facilmente consumidos por outros aplicativos.

* A lista e suas propriedades podem ser selecionadas na caixa de diálogo [configurar](#configure-dialog).
* Os estilos podem ser aplicados ao componente na caixa de diálogo [design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do fragmento de conteúdo é a v1, que foi introduzida com a versão 2.4.0 dos Componentes principais em maio de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de lista de fragmentos de conteúdo, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_cflist).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente da lista de fragmentos de conteúdo [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo configurar permite que o autor de conteúdo defina os fragmentos de conteúdo que compõem a lista e os elementos desses fragmentos que serão incluídos.

### Guia Propriedades

A guia **Properties** define quais Fragmentos de conteúdo são incluídos na lista. Isso se baseia principalmente em um Modelo de fragmento de conteúdo selecionado, mas há outras opções de filtro disponíveis.

![Guia Propriedades da caixa de diálogo Editar do Componente da lista de fragmentos de conteúdo](/help/assets/content-fragment-list-properties.png)

* **Modelo**  - Caminho para o modelo do fragmento de conteúdo no qual a lista se baseia.
   * Por padrão, todos os fragmentos de conteúdo do modelo definidos como **Caminho do Modelo** são incluídos na lista.
* **Caminho pai**  - Caminho pai do qual a lista deve ser criada.
   * Os fragmentos de conteúdo com base no **Caminho do Modelo** selecionado serão filtrados para aqueles no **Caminho Pai** especificado.
      * Clique ou toque no botão **Abrir caixa de diálogo de seleção** no lado direito do campo para especificar o caminho.
* **Tags**  - somente os Fragmentos de conteúdo com as tags especificadas serão incluídos na lista.
   * Clique ou toque no botão **Abrir caixa de diálogo de seleção** no lado direito do campo para especificar as tags.
   * Clique ou toque no X ao lado das tags selecionadas para removê-las.
* **Ordenar por**  - Campo do modelo de fragmento de conteúdo pelo qual a lista será ordenada
   * Somente campos de texto (incluindo numérico, data e hora) são selecionáveis.
* **Ordem de Classificação**  - Como a lista será classificada pelo campo  **Byte do** Pedido
   * Crescente ou decrescente
* **Máximo de itens**  - Número máximo de itens a serem mostrados na lista
   * Nenhum valor retornará todos os itens.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

>[!NOTE]
>As opções **Order By**, **Sort Order** e **Max Items** foram introduzidas com a versão 2.7.0 dos Componentes principais.

### Guia Elementos

Por padrão, todos os elementos do Modelo de fragmento de conteúdo serão incluídos na lista (a menos que limitados pelo campo **Máximo de itens**). A guia **Elements** permite especificar apenas elementos específicos a serem incluídos.

![Guia Elementos da caixa de diálogo Editar do Componente da lista de fragmentos de conteúdo](/help/assets/content-fragment-list-elements.png)

* **Elementos**  - Somente os elementos dos fragmentos de conteúdo na lista especificada serão exibidos.
   * Clique ou toque no botão **Adicionar** para adicionar um novo elemento.
   * Clique ou toque no botão **Delete** para remover um elemento selecionado.
   * Arraste a alça **Order** para reorganizar a ordem dos elementos.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os estilos aplicados ao Componente de lista de fragmentos de conteúdo.
