---
title: Componente de navegação
seo-title: Componente de navegação
description: 'null'
seo-description: O componente de navegação permite que os usuários naveguem facilmente em uma estrutura de site globalizada.
uuid: 616 c 03 fb -39 b 3-402 a-b 990-f 56 c 87 bc 6 df 4
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: da 8 d 67 d 7-b 65 e -4041-bc 0 e-e 998 f 24 a 68 f 9
disttype: dist5
gnavtheme: light
groupsectionnavitems: não
hidemerchandisingbar: herdar
hidepromocomponent: herdar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Navigation Component{#navigation-component}

O componente de navegação permite que os usuários naveguem facilmente em uma estrutura de site globalizada.

## Uso {#usage}

O componente de navegação permite qualquer hierarquia de navegação que pode ser criada a partir das cópias online de um blueprint, a partir das cópias de idioma de um idioma principal ou de uma árvore simples de páginas. Isso permite que os usuários da página naveguem facilmente em uma estrutura do site.

The [edit dialog](#edit-dialog) allows the content author to define the navigation root page along with the depth of navigation. The [design dialog](#design-dialog) allows the template author to define default values for the navigation root and depth.

## Version and Compatibility {#version-and-compatibility}

A versão atual do Componente de navegação é v 1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatível | Compatível | Compatível |


For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/navigation.html).

## Technical Details {#technical-details}

The latest technical documentation about the Navigation Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

>[!NOTE]
>
>As of Core Components release 2.1.0, the Navigation Component supports [schema.org microdata](https://schema.org).

## Edit Dialog {#edit-dialog}

Na caixa de diálogo Editar, o autor do conteúdo pode definir a página raiz para navegação e a profundidade da estrutura de navegação.

![](assets/screen_shot_2018-04-03at112055.png)

* **Raiz
da navegação** A página raiz, que será usada para gerar a árvore de navegação.
* **Excluir raiz
de navegação** Excluir a raiz de navegação na árvore resultante, incluir apenas seus descendentes.
* **Coletar todas as páginas**
secundárias Colete todas as páginas que são descendentes da raiz de navegação.
* **Profundidade
da estrutura de navegação** Define quantos níveis abaixo da árvore de navegação o componente deve ser exibido relativo à raiz de navegação (disponível apenas quando **a opção Coletar todas as páginas filhas não** está selecionada).

## Design Dialog {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os valores padrão para a página raiz de navegação e a profundidade de navegação que são apresentados aos autores de conteúdo.

### Properties Tab {#properties-tab}

![](assets/screen_shot_2018-04-03at112357.png)

* **Raiz
de navegação** O valor padrão da página raiz da estrutura de navegação, que será usado para gerar a árvore de navegação e padrão quando o autor do conteúdo adiciona o componente à página.
* **Excluir raiz
de navegação** O valor padrão da opção para excluir a raiz de navegação na árvore resultante.
* **Coletar todas as páginas**
secundárias O valor padrão da opção para coletar todas as páginas descendentes da raiz de navegação.
* **Profundidade
da estrutura de navegação** O valor padrão da profundidade da estrutura de navegação.

### Styles Tab {#styles-tab}

The Navigation Component supports the AEM [Style System](authoring.md#component-styling).