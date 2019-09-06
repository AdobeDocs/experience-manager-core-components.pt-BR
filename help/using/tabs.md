---
title: Componente de tabulações
seo-title: Componente de tabulações
description: O componente de tabulações permite a criação de várias guias para organizar o conteúdo em uma página.
seo-description: O componente de tabulações permite a criação de várias guias para organizar o conteúdo em uma página.
uuid: 46 f 71233-8 b 12-4887-a 0 c 6-ad 24 dc 469 cb 1
content-type: referência
topic-tags: componentes principais
discoiquuid: 966 d 47 fb-d 35 d -4103-b 29 d -4 ef 0 aa 739 f 24
translation-type: tm+mt
source-git-commit: 48d23edbcdf4c4ed70d590cf6c6e4ac1db14f852

---


# Componente de tabulações

O componente de tabulações do componente principal permite a organização do conteúdo em várias guias.

## Uso {#usage}

O componente de tabulações permite que o autor do conteúdo organize o conteúdo da página em várias guias.

A caixa de diálogo [Editar](#edit-dialog) permite que o autor do conteúdo defina várias guias e defina a guia ativa. Usando a caixa [de diálogo de design](#design-dialog), o autor do modelo pode definir quais componentes podem ser adicionados a guias e personalizar os estilos.

>[!NOTE]
>
>Os componentes da guia aninhados (guias nas guias) são suportados.
>
>Componentes simples da guia (não aninhados) podem ser localizados/selecionados usando a árvore [de conteúdo](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html), no entanto, as guias aninhadas não podem ser.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de tabulações é v 1, que foi introduzida com a versão 2.2.0 dos Componentes principais em outubro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de tabulações, bem como ver exemplos de suas opções de configuração, além de HTML e saída JSON, visite a Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/tabs.html).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de tabulações [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Edit Dialog {#edit-dialog}

A caixa de diálogo Editar permite que o autor do conteúdo crie, renomeie e reorganize guias, bem como defina a guia ativa.

### Guia Itens {#items-tab}

![](assets/screen-shot-2019-08-29-12.28.16.png)

Use o botão **Adicionar** para abrir o seletor de componentes para escolher qual componente adicionar como uma guia. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:

* **Ícone** - O ícone do tipo de componente da guia para fácil identificação na lista. Passe o mouse sobre o nome completo do componente como uma dica de ferramenta.
* **Descrição** - A descrição usada como o texto da guia, padrão do nome do componente selecionado para a guia.
* **Excluir** - toque ou clique para excluir a guia do componente da guia.
* **Reorganizar** - toque ou clique e arraste para reorganizar a ordem das guias.

### Guia Propriedades {#properties-tab}

![](assets/screen-shot-2019-08-29-12.28.32.png)

Na guia **Propriedades** , o autor do conteúdo pode definir qual guia está ativa quando a página é carregada. Com a **opção Padrão** , a primeira guia será selecionada.

### Guia Acessibilidade {#accessibility-tab}

![](assets/screen-shot-2019-08-29-12.28.40.png)

Na guia **Acessibilidade** , os valores podem ser definidos para [rótulos de acessibilidade](https://www.w3.org/WAI/standards-guidelines/aria/) da ARIA para o componente.

* **Rótulo** - Valor de um atributo de rótulo da JAR para o componente

## Select Panel {#select-panel}

O autor do conteúdo pode usar a **opção Selecionar painel** na barra de ferramentas do componente para mudar para um painel diferente para edição, bem como para reorganizar a ordem das guias facilmente.

![](assets/screenshot_2018-10-11at165417.png)

Depois de selecionar a **opção Selecionar painel** na barra de ferramentas do componente, as guias configuradas são exibidas como uma lista suspensa.

* A lista é ordenada pela disposição atribuída das guias e refletida na numeração.
* O tipo de componente da guia é exibido primeiro, seguido pela descrição da guia na fonte mais leve.

![](assets/screenshot_2018-10-11at165154.png)

* Tocar ou clicar em uma entrada na lista suspensa, alterna a exibição no editor para essa guia.
* As guias podem ser reorganizadas no local usando as alças de arrastar.

>[!NOTE]
>
>As guias não são selecionadas pelo autor quando no **modo Editar** . Use [**o modo de Visualização**](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) ou **[a](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** opção Exibir como publicada para interagir com as guias como um leitor do conteúdo publicado.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais componentes podem ser adicionados como itens ao componente tabulações, bem como definir quais estilos personalizados estão disponíveis para o autor do conteúdo.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes** permitidos é usada para definir quais componentes podem ser adicionados como itens ao componente tabulações pelo autor do conteúdo.

As funções de guia Componentes permitidos da mesma forma que a guia com o mesmo nome ao [definir a política e as propriedades de um Contêiner de layout no Editor de modelos.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Guia Estilos {#styles-tab}

O componente de tabulações é compatível com o Sistema [de estilo AEM](authoring.md#component-styling).
