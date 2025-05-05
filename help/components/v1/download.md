---
title: Componente de download (v1)
description: O componente de Download, dos Componentes principais, permite a criação de uma opção de download em uma página.
role: Architect, Developer, Admin, User
exl-id: ebd63522-218d-4784-bea0-1627c64f5230
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 100%

---

# Componente de download (v1) {#download-component}

O componente de Download, dos Componentes principais, permite a criação de uma opção de download em uma página.

## Uso {#usage}

O componente de Download, dos Componente principais, permite a inclusão de uma opção de download e de seu ativo associado em uma página.

* As propriedades da opção de download podem ser selecionadas na [caixa de diálogo de configuração](#configure-dialog).
* Os padrões para o componente de Download podem ser definidos na [caixa de diálogo design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a versão v1 do componente de download, que foi introduzida com a versão 2.5.0 dos componentes principais em junho de 2019.

>[!CAUTION]
>
>Este documento descreve a versão v1 do componente de download.
>
>Para obter detalhes sobre a versão atual do componente de download, consulte o documento [Componente de download](/help/components/download.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Download, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_download_br).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Download [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_download_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o item de download e como ele se comportará e será exibido para um visitante da página.

![Guia Ativo, da caixa de diálogo de edição, do componente de download](/help/assets/download-edit-asset.png)

### Guia Ativo {#asset-tab}

A seleção de um ativo de download é muito semelhante à funcionalidade do [Componente de imagem](image-v1.md), aproveitando também o DAM do AEM.

* **Baixar ativo**
   * Solte um ativo do [navegador de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR) ou toque na opção **pesquisar** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=pt-BR) no editor de ativos.

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do componente de Download](/help/assets/download-edit-properties.png)

* **Título** - exibido como um título para o item de download
   * **Obter o título do ativo DAM** - Quando selecionado, o título é preenchido automaticamente com o título do ativo DAM.
* **Descrição** - É exibido como um subtítulo descritivo do item de download
   * **Obter a descrição do ativo DAM** - Quando selecionada, a descrição é preenchida automaticamente com a descrição do ativo DAM.
* **Texto de ação** - É exibido como texto de ação para o item de download
   * Esse campo é necessário ao fazer upload de um ativo do sistema de arquivos.
   * **Exibir em linha** - Quando selecionado, o **Texto de ação** fornecido será exibido em linha.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o componente de Download.

### Guia Propriedades {#properties-tab-design}

![Caixa de diálogo design do componente de Download](/help/assets/download-design.png)

* **Permitir o upload por meio do sistema de arquivos** - Permite que o autor de conteúdo faça upload de um ativo do sistema de arquivos local como o ativo de download.
   * O valor padrão não está selecionado.
* **Tipo de título** - O elemento HTML usado para o título do componente de Download.
   * Se nenhum valor for selecionado, o valor padrão será H3.
* **Tamanho do arquivo de exibição** - Quando selecionado, o tamanho do arquivo do ativo será exibido no componente de Download.
   * O valor padrão está selecionado.
* **Formato de arquivo de exibição** - Quando selecionado, o formato de arquivo do ativo será exibido no componente de Download.
   * O valor padrão está selecionado.
* **Exibir nome de arquivo** - Quando selecionado, o nome do arquivo do ativo será exibido no componente de Download.
   * O valor padrão está selecionado.

### Guia Estilos {#styles-tab}

O componente de Imagem é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
