---
title: Componente de Lista de fragmentos de conteúdo
description: O componente de Lista de fragmentos de conteúdo, dos Componentes principais, permite a exibição de uma lista de fragmentos de conteúdo.
role: Architect, Developer, Admin, User
exl-id: 0f2295b1-d287-4f72-8ee4-fa98c4850e53
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '806'
ht-degree: 100%

---


# Componente de Lista de fragmentos de conteúdo{#content-fragment-list-component}

O componente de Lista de fragmentos de conteúdo, dos Componentes principais, permite a exibição de uma lista de [fragmentos de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=pt-BR).

{{traditional-aem}}

## Uso {#usage}

O componente de Lista de fragmentos de conteúdo, dos Componentes principais, permite a inclusão de uma lista de [fragmentos de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=pt-BR) em uma página com base em um modelo de Fragmento de conteúdo. Isso pode ser especialmente útil para criar [conteúdo sem periféricos](https://helpx.adobe.com/br/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) que podem ser facilmente consumidos por outros aplicativos.

* A lista e suas propriedades podem ser selecionadas na [caixa de diálogo de configuração](#configure-dialog).
* Os estilos podem ser aplicados ao componente na [caixa de diálogo de design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de fragmento de conteúdo é a v2, introduzida com a versão 2.18.0 dos componentes principais em fevereiro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|----|---|---|---|
| v2 | - | Compatível | Compatível | Compatível |
| [v1](v1/content-fragment-list.md) | Compatível | Compatível | - | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Lista de fragmentos de conteúdo, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_cflist_br).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Lista de fragmentos de conteúdo [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina os fragmentos de conteúdo que compõem a lista e os elementos desses fragmentos que serão incluídos.

### Guia Propriedades

A guia **Propriedade** define quais Fragmentos de conteúdo são incluídos na lista. Isso se baseia principalmente em um Modelo de fragmento de conteúdo selecionado, mas há outras opções de filtro disponíveis.

![Guia Propriedades da caixa de diálogo de edição do componente de Lista de fragmentos de conteúdo](/help/assets/content-fragment-list-properties.png)

* **Modelo** - Caminho para o Modelo do fragmento de conteúdo no qual a lista se baseia.
   * Por padrão, todos os fragmentos de conteúdo do modelo definidos como **Caminho do modelo** são incluídos na lista.
* **Caminho principal** - O caminho principal do qual a lista deve ser criada.
   * Os fragmentos de conteúdo com base no **Caminho do modelo** selecionado serão filtrados para aqueles no **Caminho principal** especificado.
      * Clique ou toque no botão **Abrir caixa de diálogo de seleção** no lado direito do campo para especificar o caminho.
* **Tags** - Somente os Fragmentos de conteúdo com as tags especificadas serão incluídos na lista.
   * Clique ou toque no botão **Abrir caixa de diálogo de seleção** no lado direito do campo para especificar as tags.
   * Clique ou toque no X ao lado das tags selecionadas para removê-las.
* **Ordenar por** - O campo do modelo de fragmento de conteúdo pelo qual a lista será ordenada.
   * Somente campos de texto (incluindo numérico, data e hora) são selecionáveis.
* **Ordem de classificação** - Como a lista será classificada pelo campo **Ordenar por**
   * Crescente ou decrescente
* **Número máximo de itens** - Número máximo de itens a serem mostrados na lista
   * Nenhum valor retornará todos os itens.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

>[!NOTE]
>As opções **Ordenar por**, **Ordem de classificação** e **Número máximo de itens** foram introduzidas com a versão 2.7.0 dos Componentes principais.

### Guia Elementos

Por padrão, todos os elementos do Modelo de fragmento de conteúdo serão incluídos na lista (a menos que limitados pelo campo **Número máximo de itens**). A guia **Elementos** permite especificar apenas elementos específicos a serem incluídos.

![Guia Elementos da caixa de diálogo de edição do componente de Lista de fragmentos de conteúdo](/help/assets/content-fragment-list-elements.png)

* **Elementos** - Somente os elementos dos fragmentos de conteúdo na lista especificada serão exibidos.
   * Clique ou toque no botão **Adicionar** para adicionar um novo elemento.
   * Clique ou toque no botão **Excluir** para remover um elemento selecionado.
   * Arraste a alça **Ordenar** para reorganizar a ordem dos elementos.

### Guia Estilos {#styles-tab-edit}

![Guia Estilos da caixa de diálogo de edição do componente de lista do fragmento de conteúdo](/help/assets/content-fragment-list-styles.png)

O componente de lista do fragmento de conteúdo é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que o menu suspenso fique disponível.

## Caixa de diálogo de design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente de lista do fragmento de conteúdo é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.
