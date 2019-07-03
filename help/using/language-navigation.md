---
title: Componente de navegação de idioma
seo-title: Componente de navegação de idioma
description: 'null'
seo-description: O componente de navegação de idioma fornece uma navegação de idioma/país para um site, para que os visitantes possam navegar até a mesma página em uma localidade diferente.
uuid: ce 736458-9 cdf -4 bc 2-b 90 f -9 c 5 a 62 fe 1 ca 0
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 8 f 232 eb 0-65 d 5-4075-8668-75 f 1366882 c 8
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


# Language Navigation Component{#language-navigation-component}

O componente de navegação de idioma fornece uma navegação de idioma/país para um site, para que os visitantes possam navegar até a mesma página em uma localidade diferente.

## Uso {#usage}

Geralmente, os sites são fornecidos em vários idiomas para diferentes regiões. O componente de navegação de idioma permite que um visitante visualize a mesma página em idiomas/localidades diferentes.

The [edit dialog](#edit-dialog) allows the definition of the global site navigation root as well as how deep into the structure the navigation should go. Using the [design dialog](#design-dialog), the template author can set the default values for the same options.

## Version and Compatibility {#version-and-compatibility}

A versão atual do Componente de navegação de idioma é v 1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatível | Compatível | Compatível |


For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Language Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/language-navigation/language-structure/us/en/language-navigation.html).

## Technical Details {#technical-details}

The latest technical documentation about the Language Navigation Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

A caixa de diálogo Editar permite a definição da raiz de navegação do site global, bem como a profundidade da estrutura que a navegação deve ir.

![](assets/screen_shot_2018-01-12at133353.png)

* **Raiz
de navegação** Define a página raiz da estrutura de navegação.
   * Use the **Open Selection Dialog** button to easily navigate the content structure and select the root.
* **Profundidade de profundidade**
da estrutura do idioma da estrutura de idioma global relativa à raiz de navegação.

## Design Dialog {#design-dialog}

Usando a caixa de diálogo de design, o autor do modelo pode definir os valores padrão para as mesmas opções disponíveis na janela de edição.

### Properties Tab {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Valor padrão de**navegação da
raiz de navegação quando um autor de conteúdo posiciona o componente Alternador de idiomas em uma página de conteúdo
* **Valor padrão de Profundidade**
da estrutura de idioma da profundidade da estrutura de idioma quando um autor de conteúdo posiciona o Componente Alternador de idiomas em uma página de conteúdo

### Styles Tab {#styles-tab}

The Language Navigation Component supports the AEM [Style System](authoring.md#component-styling).