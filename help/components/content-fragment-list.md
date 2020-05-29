---
title: Componente de Lista do fragmento do conteúdo
description: O componente principal de Lista de fragmento de conteúdo do componente permite a exibição de uma lista de fragmentos de conteúdo.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 3%

---


# Componente de Lista do fragmento do conteúdo{#content-fragment-list-component}

O componente principal de Lista de fragmento de conteúdo do componente permite a exibição de uma lista de fragmentos [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)conteúdo.

## Uso {#usage}

O Componente principal de Lista de fragmento de conteúdo permite a inclusão de uma lista de fragmentos [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) conteúdo em uma página com base em um modelo de Fragmento de conteúdo. Isso pode ser especialmente útil para criar conteúdo [](https://helpx.adobe.com/br/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) sem cabeçalho que possa ser facilmente consumido por outros aplicativos.

* A lista e suas propriedades podem ser selecionadas na caixa de diálogo [](#configure-dialog)configurar.
* Os estilos podem ser aplicados ao componente na caixa de diálogo [de](#design-dialog)design.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de fragmento de conteúdo é a v1, que foi introduzida com a versão 2.4.0 dos Componentes principais em maio de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de Lista do fragmento de conteúdo, bem como ver exemplos de suas opções de configuração e saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_cflist)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de Lista do fragmento de conteúdo [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina os fragmentos de conteúdo que compõem a lista e os elementos desses fragmentos que serão incluídos.

### Guia Propriedades

A guia **Propriedades** define quais Fragmentos de conteúdo são incluídos na lista. Isso se baseia principalmente em um Modelo de fragmento de conteúdo selecionado, mas há outras opções de filtro disponíveis.

![Guia Propriedades da caixa de diálogo Editar do Componente de Lista do fragmento do conteúdo](/help/assets/content-fragment-list-properties.png)

* **Modelo** - Caminho para o modelo de fragmento do conteúdo no qual a lista se baseia.
   * Por padrão, todos os fragmentos de conteúdo do modelo definidos como Caminho **** modelo são incluídos na lista.
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
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

>[!NOTE]
>As opções **Pedido por**, **Ordem** de classificação e Itens **** máximos foram apresentadas com a versão 2.7.0 dos Componentes principais.

### Guia Elementos

Por padrão, todos os elementos do Modelo de fragmento de conteúdo serão incluídos na lista (a menos que limitado pelo campo Itens **** máximos). A guia **Elementos** permite que você especifique apenas elementos específicos a serem incluídos.

![Guia Elementos da caixa de diálogo Editar do Componente de Lista do fragmento do conteúdo](/help/assets/content-fragment-list-elements.png)

* **Elementos** - somente os elementos dos fragmentos de conteúdo na lista especificada serão exibidos.
   * Clique ou toque no botão **Adicionar** para adicionar um novo elemento.
   * Clique ou toque no botão **Excluir** para remover um elemento selecionado.
   * Arraste a alça **Ordem** para reorganizar a ordem dos elementos.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os estilos aplicados ao Componente de Lista do fragmento do conteúdo.
