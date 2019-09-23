---
title: Baixar componente
seo-title: Baixar componente
description: 'null'
seo-description: O componente de download do componente principal permite a criação de uma opção de download em uma página.
uuid: ec807de9-f76c-4850-9ece-c3e439a1d626
contentOwner: Usuário
content-type: referência
topic-tags: autoria
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: f093f58e-9755-4a4f-803a-ab93a50e6870
translation-type: tm+mt
source-git-commit: 88bc68b60e5de247fe800ac041ffefdf9238cce1

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

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de download e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library/download.html)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de download [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/download/v1/download).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o item de download e como ele se comportará e aparecerá para um visitante da página.

![](assets/screen-shot-2019-06-17-09.49.14.png)

### Guia Ativo {#asset-tab}

A seleção de um ativo de download é muito semelhante à funcionalidade do Componente [de](image.md) imagem e também aproveita o DAM do AEM.

* **Baixar ativo**
   * Solte um ativo do navegador [de](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) ativos ou toque na opção de **navegação** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) no editor de ativos.

### Guia Propriedades {#properties-tab}

![](assets/screen-shot-2019-06-17-09.49.51.png)

* **Título** - Exibe como título do item de download
   * **Obter título do ativo** DAM - quando selecionado, o título é preenchido automaticamente com o título do ativo DAM.
* **Descrição** - Exibe como um subtítulo descritivo do item de download
   * **Obter descrição do ativo** DAM - quando selecionada, a descrição é preenchida automaticamente com a descrição do ativo DAM.
* **Texto** de ação - exibido como texto de ação para o item de download
   * Esse campo é necessário ao fazer upload de um ativo do sistema de arquivos.
   * **Exibir em linha** - quando selecionado, o Texto **de** ação fornecido será exibido em linha.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor do conteúdo que usa o Componente de download.

### Guia Propriedades {#properties-tab-design}

![](assets/screen-shot-2019-06-17-10.04.31.png)

* **Texto** de ação padrão - Define o texto **de** ação padrão fornecido quando um autor adiciona o componente de download a uma página.
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

O componente de imagem suporta o sistema [de](authoring.md#component-styling)estilo AEM.
