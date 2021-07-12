---
title: Baixar componente
description: O componente Download do componente principal permite a criação de uma opção de download em uma página.
role: Architect, Developer, Admin, User
exl-id: 48e7ade0-b849-4d1f-b836-51196e5ac507
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 2%

---

# Baixar componente{#download-component}

O componente Download do componente principal permite a criação de uma opção de download em uma página.

## Uso {#usage}

O componente Baixamento do componente principal permite a inclusão de uma opção de download e de seu ativo associado em uma página.

* As propriedades da opção de download podem ser selecionadas na caixa de diálogo [configurar](#configure-dialog).
* Os padrões do componente de download podem ser definidos na caixa de diálogo [design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de download é a v1, que foi introduzida com a versão 2.5.0 dos Componentes principais em junho de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de download, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_download).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de download [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_download_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o item de download e como ele se comportará e será exibido para um visitante da página.

![Guia Ativo da caixa de diálogo de edição do Componente de download](/help/assets/download-edit-asset.png)

### Guia Ativo {#asset-tab}

A seleção de um ativo de download é muito semelhante à funcionalidade do [Componente de imagem](image.md) e também aproveita AEM DAM.

* **Baixar ativo**
   * Solte um ativo do [navegador de ativos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) ou toque na opção **browse** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) no editor de ativos.

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do Componente de download](/help/assets/download-edit-properties.png)

* **Título**  - é exibido como um título para o item de download
   * **Obter título do ativo DAM**  - Quando selecionado, o título é preenchido automaticamente com o título do ativo DAM.
* **Descrição**  - É exibido como um subtítulo descritivo do item de download
   * **Obter descrição do ativo DAM**  - Quando selecionada, a descrição é preenchida automaticamente com a descrição do ativo DAM.
* **Texto de ação**  - é exibido como texto de ação para o item de download
   * Esse campo é necessário ao fazer upload de um ativo do sistema de arquivos.
   * **Exibir em linha**  - Quando selecionado, o  **Texto** de ação fornecido será exibido em linha.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o Componente de download.

### Guia Propriedades {#properties-tab-design}

![Caixa de diálogo Design do componente de download](/help/assets/download-design.png)

* **Permitir upload do sistema de arquivos**  - Permite que o autor de conteúdo faça upload de um ativo do sistema de arquivos local como o ativo de download.
   * O valor padrão está desmarcado.
* **Tipo de título**  - O elemento HTML usado para o título do Componente de download.
   * Se nenhum valor for selecionado, o valor padrão será H3.
* **Exibir tamanho do arquivo**  - quando selecionado, o tamanho do arquivo do ativo será exibido no componente de download.
   * O valor padrão está selecionado.
* **Exibir formato de arquivo**  - quando selecionado, o formato de arquivo do ativo será exibido no componente de download.
   * O valor padrão está selecionado.
* **Exibir nome de arquivo**  - quando selecionado, o nome do arquivo do ativo será exibido no componente de download.
   * O valor padrão está selecionado.

### Guia Estilos {#styles-tab}

O Componente de imagem suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).
