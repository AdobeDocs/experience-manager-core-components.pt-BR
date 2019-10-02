---
title: Embed Component
seo-title: Embed Component
description: The Embed Component enables embedding external content in an AEM content page.
seo-description: O componente incorporado permite a incorporação de conteúdo externo em uma página de conteúdo do AEM.
content-type: referência
topic-tags: componentes principais
translation-type: tm+mt
source-git-commit: d748bf211ec36d12cac016ca9bf707f24db1ce48

---


# Componente incorporado{#embed-component}

O componente incorporado dos componentes principais permite a incorporação de conteúdo externo em uma página de conteúdo do AEM.

## Uso {#usage}

The Core Component Embed Component allows the content author to define selected external content to be embedded within an AEM content page. Além disso, há uma opção para definir o HTML de forma livre a ser incorporado também.

* As propriedades do componente podem ser definidas na caixa de diálogo [](#configure-dialog)configurar.
* Defaults for the component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente incorporado é a v1, que foi introduzida com a versão 2.7.0 dos Componentes principais em setembro de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente incorporado e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library/embed.html)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente incorporado [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o recurso externo a ser incorporado na página. Primeiro escolha qual tipo de recurso deve ser incorporado: **URL**, **Incorporável** ou **HTML**.

### URL {#url}

A incorporação mais simples é o URL. Basta colar o URL do recurso que deseja incorporar no campo **URL** . O componente tentará acessar o recurso e, se ele puder ser renderizado por um dos processadores, exibirá uma mensagem de confirmação abaixo do campo **URL** . Caso contrário, o campo será marcado com erro.

O Componente incorporado é fornecido com processadores para os seguintes tipos de recursos:

* Recursos compatíveis com o padrão [oEmbed](https://oembed.com/) , incluindo publicação do Facebook, Instagram, SoundCloud, Twitter e YouTube
* Pinterest

Os desenvolvedores podem adicionar outros processadores de URL, [seguindo a documentação do desenvolvedor do Componente incorporado.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.08.29.png)

### Incorporável {#embeddable}

Os incorporados permitem mais personalização do recurso incorporado, que pode ser parametrizado e incluir informações adicionais. Um autor é capaz de selecionar entre os materiais incorporados confiáveis pré-configurados e o componente é fornecido com um anúncio pronto para uso no Youtube.

O campo **Incorporável** define o tipo de processador que você deseja usar. No caso do YouTube incorporável, é possível definir:

* **Video ID - The unique video ID from YouTube of the resource you want to embed**
* **Width** - The width of the embedded video
* **Height - The height of the embedded video**

Other embeddables would offer similar fields and can be defined by a developer by [following the developer documentation of the Embed Component.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.15.00.png)

>[!NOTE]
>Embeddables must be enabled at the template level via the Design Dialog to be available to the page author.[](#design-dialog)

### HTML {#html}

You can add free-form HTML to your page using the Embed Component.

![](assets/screen-shot-2019-09-25-10.20.00.png)

>[!NOTE]
>Any unsafe tags such as scripts will be filtered from the entered HTML and will not be rendered on the resulting page.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Embed Component and the defaults set when placing the Embed Component.

![](assets/screen-shot-2019-09-25-10.25.28.png)

* **Disable URL - Disables the URL option for the content author when selected******
* **Disable Embeddables - Disables the Embeddable option for the content author when selected, regardless of which embeddable processors are allowed.******
* **Disable HTML - Disables the HTML option for the content author when selected.******
* **Allowed Embeddables - Multislect that defines which embeddable processors are available to the content author, provided that the Embeddable option is active.******
