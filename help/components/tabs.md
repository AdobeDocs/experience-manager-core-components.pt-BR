---
title: Componente de Guias
description: O componente de Guias permite a criação de várias guias para organizar o conteúdo em uma página.
role: Architect, Developer, Admin, User
exl-id: 0031c5f3-447c-4932-898f-2f453801e492
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 99%

---

# Componente de Guias {#tabs-component}

O componente de Guias, dos Componente principais, permite a organização do conteúdo em várias guias.

## Uso {#usage}

O componente de Guias permite que o autor de conteúdo organize o conteúdo da página em várias guias.

A [caixa de diálogo de edição](#edit-dialog) permite que o autor de conteúdo defina várias guias, bem como defina a guia ativa. Usando a [caixa de diálogo de design](#design-dialog), o autor do modelo pode definir quais componentes podem ser adicionados às guias e personalizar os estilos.

>[!TIP]
>
>Os componentes de guia aninhados (guias dentro de guias) são compatíveis.
>
>Componentes de guia simples (não aninhados) podem ser localizados/selecionados usando a [árvore de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR#content-tree), no entanto, guias aninhadas não podem ser localizadas/selecionadas.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Guias é a v1, introduzida com a versão 2.2.0 dos Componentes principais em outubro de 2018, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível com<br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Guias, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_tabs_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Guias [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Deep linking para um painel {#deep-linking}

Os [componentes Acordeão](accordion.md) e de Guias suportam a vinculação diretamente a um painel dentro do componente.

Para fazer isso:

1. Visualize a página com o componente usando a opção **[Exibir como publicada](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR#view-as-published)** no editor de páginas.
1. Inspecione o conteúdo da página e identifique o ID do painel.
   * Por exemplo `id="accordion-86196c94d3-item-ca319dbb0b"`
1. O ID se torna a âncora que pode ser anexada ao URL usando um hash (`#`).
   * Por exemplo `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Ao navegar até o URL com o ID do painel como âncora, o navegador rolará diretamente para o componente específico e exibirá o painel especificado. Se o painel estiver configurado para não ser expandido por padrão, ele será expandido automaticamente.

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo crie, renomeie e reorganize as guias, e defina a guia ativa.

### Guia Itens {#items-tab}

![Guia Itens da caixa de diálogo de edição do componente de Guias](/help/assets/tabs-edit-items.png)

Use o botão **Adicionar** para abrir o seletor de componentes e escolher que componente adicionar como guia. Uma vez adicionado, uma entrada é adicionada à lista, contendo as seguintes colunas:

* **Ícone** - O ícone do tipo de componente da guia para facilitar a identificação na lista. Passe o mouse sobre o ícone para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição** - A descrição usada como o texto da guia, padronizando o nome do componente selecionado para a guia.
* **Excluir** - Toque ou clique para excluir a guia do componente de guia.
* **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem das guias.

>[!TIP]
>
>Se a janela de visualização da página for reduzida para que a caixa de diálogo de edição se torne tela cheia, o botão **Adicionar** ficará oculto. Os componentes ainda podem ser adicionados ao componente de Guias ao [arrastar do navegador de componentes e soltar no componente de Guias no editor de páginas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR#inserting-a-component).

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do componente de Guias](/help/assets/tabs-edit-properties.png)

* **Item ativo** - O autor de conteúdo pode definir qual guia está ativa quando a página é carregada.
   * Com a opção **Padrão**, a primeira guia será selecionada.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade da caixa de diálogo de edição do componente de Guias](/help/assets/tabs-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

## Selecionar painel {#select-panel}

O autor de conteúdo pode usar a opção **Selecionar painel** na barra de ferramentas do componente para alterar para um painel diferente para edição, bem como para reorganizar facilmente a ordem das guias.

![Ícone Selecionar painel](/help/assets/select-panel-icon.png)

Depois de escolher a opção **Selecionar painel** na barra de ferramentas do componente, as guias configuradas são exibidas como uma lista suspensa.

* A lista é ordenada pela disposição atribuída das guias e é refletida na numeração.
* O tipo de componente da guia é exibido primeiro, seguido pela descrição da guia em fonte mais clara.

![Selecionar popover de painel](/help/assets/select-panel-popover.png)

* Tocar ou clicar em uma entrada na lista suspensa altera a exibição do editor para essa guia.
* As guias podem ser reorganizadas no local usando as alças de arrastar.

>[!NOTE]
>
>As guias não podem ser selecionadas pelo autor quando estiverem no modo **Editar**. Use o modo de **[Visualização](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR#preview-mode)** ou a opção **[Visualizar como publicado](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** para interagir com as guias como um leitor do conteúdo publicado.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais componentes podem ser adicionados como itens ao componente de guias, e define quais estilos personalizados estão disponíveis para o autor de conteúdo.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** é usada para definir quais componentes podem ser adicionados como itens ao componente de guias pelo autor de conteúdo.

Ela funciona da mesma maneira que a guia de mesmo nome ao [definir a política e as propriedades de um Contêiner de layout no Editor de modelo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR).

### Guia Estilos {#styles-tab}

O componente de Guias é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Guias oferece suporte à [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
