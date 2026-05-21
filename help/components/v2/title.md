---
title: Componente de título (v2)
description: O componente de Título, dos Componentes principais, é um componente de cabeçalho de seção que apresenta edição no local.
role: Developer, Admin, User
exl-id: f853ec46-19fd-4569-a9d3-5c376d2a2101
index: false
TQID: https://experienceleague.adobe.com/DcglSBQ4f6RGtvjHGT92l6WpLP080yUeGsWXF20gTWI
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 529
ht-degree: 100%

---

# Componente de título (v2) {#title-component}

O componente de Título, dos Componentes principais, é um componente de cabeçalho de seção que apresenta edição no local.

## Uso {#usage}

O componente de Título deve ser usado como o título ou cabeçalho de uma seção de conteúdo. Os níveis de cabeçalho disponíveis podem ser definidos pelo autor do modelo na [caixa de diálogo design](#design-dialog). O editor de conteúdo pode selecionar a partir dos níveis de cabeçalho disponíveis na [caixa de diálogo de edição](#edit-dialog). Para maior conveniência, a edição simples no local do texto do cabeçalho também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a versão v2 do componente de título, que foi introduzida com a versão 2.0.0 dos componentes principais em janeiro de 2018.

>[!CAUTION]
>
>Este documento descreve a versão v2 do componente de título.
>
>Para detalhes sobre a versão atual do componente de Título, consulte o documento [Componente de Título](/help/components/title.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Título, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_title_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Título [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_title_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo defina o texto do título, e selecione o nível do cabeçalho.

* **Título** - Se estiver vazio, o título da página será usado
* **Tipo / Tamanho** - Define o nível de cabeçalho do título
* **Link** - Define o conteúdo ao qual o título será vinculado. Pode ser um caminho para uma página de conteúdo, um URL externo ou uma âncora de página.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

![Caixa de diálogo de edição do componente de Título](/help/assets/title-edit.png)

>[!NOTE]
>
>A capacidade de definir um link para o título foi introduzida com a versão 2.2.0 dos Componentes principais.

O editor local também pode ser usado para editar o texto do componente de Título.

![Edição no local do componente de Título](/help/assets/title-edit-inline.png)

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o nível de cabeçalho padrão que os componentes de título terão quando criados pelos autores de conteúdo.

### Guia Tamanhos {#sizes-tab}

![Caixa de diálogo de design do componente de Título](/help/assets/title-design.png)

* **Tipos / tamanhos permitidos para editores** - Ativa ou desativa tipos de cabeçalho que estarão disponíveis para autores de conteúdo quando eles usarem o componente de Título.
* **Tipo / Tamanho padrão** - Define o tipo de cabeçalho que será atribuído automaticamente quando um autor de conteúdo adicionar o componente de Título a uma página.
* **Desabilitar link** - Desativa o suporte para links no componente de título para impedir que os autores de conteúdo vinculem de títulos.

>[!NOTE]
>
>A capacidade de definir um link para o título foi introduzida com a versão 2.2.0 dos Componentes principais.

### Guia Estilos {#styles-tab}

O componente de Título é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Título oferece suporte à [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
