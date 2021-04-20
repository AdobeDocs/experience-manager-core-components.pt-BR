---
title: Componente do título
description: O Componente principal de título do componente é um componente de cabeçalho de seção que apresenta edição no local.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 3%

---


# Componente do título{#title-component}

O Componente principal de título do componente é um componente de cabeçalho de seção que apresenta edição no local.

## Uso {#usage}

O Componente de título deve ser usado como o título ou cabeçalho de uma seção de conteúdo. Os níveis de cabeçalho disponíveis podem ser definidos pelo autor do modelo na caixa de diálogo [design](#design-dialog). O editor de conteúdo pode selecionar a partir dos níveis de cabeçalho disponíveis no [diálogo de edição](#edit-dialog). Para maior conveniência, a edição simples no local do texto do cabeçalho também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de título é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | Compatível | Compatível | Compatível |
| [v1](v1/title-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de título e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_title).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de título [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_title_v2).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Editar Caixa de Diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo defina o texto do título, bem como selecione o nível do cabeçalho.

* **Título**  - Se estiver vazio, o título da página será usado
* **Tipo/tamanho**  - Define o nível de cabeçalho do título
* **Link**  - Define o conteúdo ao qual o título será vinculado. Pode ser um caminho para uma página de conteúdo, um URL externo ou uma âncora de página.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

![Caixa de diálogo de edição do componente de título](/help/assets/title-edit.png)

>[!NOTE]
>
>A capacidade de definir um link para o título foi introduzida com a versão 2.2.0 dos Componentes principais.

O editor local também pode ser usado para editar o texto do componente de título.

![Edição no local do Componente de título](/help/assets/title-edit-inline.png)

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o nível de cabeçalho padrão que os componentes de título terão quando criados pelos autores de conteúdo.

### Guia Tamanhos {#sizes-tab}

![Caixa de diálogo de design do componente de título](/help/assets/title-design.png)

* **Tipos/tamanhos permitidos para autores**  - ative ou desative tipos de cabeçalho que estarão disponíveis para autores de conteúdo quando usarem o Componente de título.
* **Tipo/tamanho padrão** - defina o tipo de cabeçalho que será atribuído automaticamente quando um autor de conteúdo adicionar o Componente de título a uma página.
* **Desativar link** - Desative o suporte para links no componente de título para impedir que os autores de conteúdo vinculem de títulos.

>[!NOTE]
>
>A capacidade de definir um link para o título foi introduzida com a versão 2.2.0 dos Componentes principais.

### Guia Estilos {#styles-tab}

O Componente de título suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

## Camada de dados do cliente Adobe {#data-layer}

O Componente de título oferece suporte à Camada de dados do cliente do Adobe.](/help/developing/data-layer/overview.md)[
