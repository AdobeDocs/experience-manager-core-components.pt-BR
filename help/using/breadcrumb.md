---
title: Componente de trilha de navegação
seo-title: Componente de trilha de navegação
description: 'null'
seo-description: O componente de navegação estrutural do componente principal é um componente de navegação que cria uma navegação estrutural de links com base no local da página na hierarquia de conteúdo.
uuid: 13 e 858 d 5-24 ad -4144-adc 4-0 fa 1 ffd 257 c 1
contentOwner: Usuário
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: asu 237 df -08 b 8-4 deb -9881-66 a 1 f 0 d 65 ef 3
modalsize: 426x240
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Breadcrumb Component{#breadcrumb-component}

O componente de navegação estrutural do componente principal é um componente de navegação que cria uma navegação estrutural de links com base no local da página na hierarquia de conteúdo.

## Uso {#usage}

O componente de navegação estrutural exibe a posição da página atual na hierarquia do site, permitindo que os visitantes da página naveguem pela hierarquia da página a partir do seu local atual. Isso é frequentemente integrado aos cabeçalhos de página ou rodapés.

Available options, such as the default navigation level and the ability to show the current page or hidden pages, can be defined by the template author in the [design dialog](#design-dialog). The content editor can then choose if hidden pages should be shown or not and the actual navigation level for the component in the [edit dialog](#edit-dialog).

## Version and Compatibility {#version-and-compatibility}

A versão atual do componente de navegação estrutural é v 2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatível | Compatível | Compatível |
| [v1](breadcrumb-v1.md) | Compatível | Compatível | Compatível |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Breadcrumb Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/breadcrumb/hidden/level-1/level-2/breadcrumb.html).

>[!NOTE]
>
>As of Core Components release 2.1.0, the Breadcrumb Component supports [schema.org microdata](https://schema.org/BreadcrumbList).

## Technical Details {#technical-details}

The latest technical documentation about the Breadcrumb Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

A caixa de diálogo Editar permite que o autor do conteúdo exclua páginas ocultas e ativas nas navegações estruturais, bem como a profundidade na hierarquia que ela deve ser exibida.

![](assets/screen_shot_2018-01-12at124250.png)

* **Nível de início de navegação** - Onde na hierarquia o componente da trilha de navegação deve começar para percorrer a página atual. Por exemplo, em We. Retail:

   * 0 starts at `/content`

   * 1 starts at `/content/we-retail`
   * 2 starts at `/content/we-retail/<country>`

* **Mostrar itens de navegação ocultos** - Mostrar páginas marcadas como ocultas na navegação estrutural (por padrão, eles não serão exibidos)
* **Ocultar a página** atual - Suprimir a página atual na navegação estrutural (por padrão, ela será exibida)

## Design Dialog {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o que os valores padrão são para as opções de suprimir páginas ocultas e ativas nas navegações estruturais, bem como a profundidade na hierarquia que ela deve ser exibida.

### Main Tab {#main-tab}

![](assets/screen_shot_2018-01-12at124437.png)

* **Nível de início de navegação** - define o valor padrão para onde, na hierarquia, o componente da trilha de navegação deve começar para se movimentar até a página atual quando o componente da navegação estrutural for adicionado a uma página.
* **Mostrar itens de navegação ocultos** - Define o valor padrão da opção **Mostrar itens** de navegação ocultos quando o componente de navegação estrutural é adicionado a uma página.

   * Isso não ativa ou desativa a opção para o autor. Ela apenas define o valor padrão.

* **Ocultar página** atual - Define o valor padrão da opção **Ocultar página** atual quando o componente de navegação estrutural é adicionado a uma página.

   * Isso não ativa ou desativa a opção para o autor. Ela apenas define o valor padrão.

### Styles Tab {#styles-tab}

The Breadcrumb Component supports the AEM [Style System](authoring.md#component-styling).