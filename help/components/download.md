---
title: Baixar componente
description: O componente de download do componente principal permite a criação de uma opção de download em uma página.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 2%

---


# Baixar componente{#download-component}

O componente de download do componente principal permite a criação de uma opção de download em uma página.

## Uso {#usage}

O componente de download do componente principal permite a inclusão de uma opção de download e de seu ativo associado em uma página.

* As propriedades da opção de download podem ser selecionadas na caixa de diálogo [](#configure-dialog)configurar.
* Os padrões do componente de download podem ser definidos na caixa de diálogo [](#design-dialog)de design.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de download é a v1, que foi introduzida com a versão 2.5.0 dos Componentes principais em junho de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de download e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_download)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de download [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_download_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o item de download e como ele se comportará e aparecerá para um visitante da página.

![Guia Ativo da caixa de diálogo de edição do Componente de download](/help/assets/download-edit-asset.png)

### Guia Ativo {#asset-tab}

A seleção de um ativo de download é muito semelhante à funcionalidade do Componente [de](image.md) imagem e também aproveita o DAM do AEM.

* **Baixar ativo**
   * Solte um ativo do navegador [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) ativos ou toque na opção de **navegação** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) no editor de ativos.

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do Componente de download](/help/assets/download-edit-properties.png)

* **Título** - Exibe como um título para o item de download
   * **Obter título do ativo** DAM - quando selecionado, o título é preenchido automaticamente com o título do ativo DAM.
* **Descrição** - Exibe como um subtítulo descritivo do item de download
   * **Obter descrição do ativo** DAM - quando selecionada, a descrição é preenchida automaticamente com a descrição do ativo DAM.
* **Texto** de ação - exibido como texto de ação para o item de download
   * Esse campo é necessário ao fazer upload de um ativo do sistema de arquivos.
   * **Exibir em linha** - quando selecionado, o Texto **de** ação fornecido será exibido em linha.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor do conteúdo que usa o Componente de download.

### Guia Propriedades {#properties-tab-design}

![Caixa de diálogo Design do Componente de download](/help/assets/download-design.png)

* **Permitir upload do sistema** de arquivos - permite que o autor do conteúdo carregue um ativo do sistema de arquivos local como o ativo de download.
   * O valor padrão não está selecionado.
* **Tipo** de título - O elemento HTML usado para o título do Componente de download.
   * Se nenhum valor for selecionado, o valor padrão será H3.
* **Exibir tamanho** do arquivo - quando selecionado, o tamanho do arquivo do ativo será exibido no componente de download.
   * O valor padrão é selecionado.
* **Exibir formato** de arquivo - quando selecionado, o formato de arquivo do ativo será exibido no componente de download.
   * O valor padrão é selecionado.
* **Exibir nome de arquivo** - quando selecionado, o nome de arquivo do ativo será exibido no componente de download.
   * O valor padrão é selecionado.

### Guia Estilos {#styles-tab}

O componente de imagem suporta o sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
