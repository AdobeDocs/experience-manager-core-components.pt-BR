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
source-git-commit: 8a34ecc432e489b8dc025aeda29d8eba9c788861

---


# Language Navigation Component{#language-navigation-component}

O componente de navegação de idioma fornece uma navegação de idioma/país para um site, para que os visitantes possam navegar até a mesma página em uma localidade diferente.

## Uso {#usage}

Os sites são geralmente fornecidos em vários idiomas para diferentes regiões. O componente de navegação de idioma permite que um visitante visualize a mesma página em idiomas/localidades diferentes. Assim, se você for um leitor na versão em alemão suíço do site, poderá alternar facilmente para a versão em inglês dos EUA da mesma página. O componente de Navegação de idioma trata da compreensão do idioma do site e encontra a página correspondente de forma automática.

A caixa de diálogo [Editar](#edit-dialog) permite a definição da raiz de navegação do site global, bem como a profundidade da estrutura que a navegação deve ir. Usando a [caixa de diálogo de design](#design-dialog), o autor do modelo pode definir os valores padrão para as mesmas opções.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de navegação de idioma é v 1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de navegação de idioma, bem como ver exemplos de suas opções de configuração, além de HTML e saída JSON, visite a Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/language-navigation/language-structure/us/en/language-navigation.html).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de navegação de idioma [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Editar permite a definição da raiz de navegação do site global, bem como a profundidade da estrutura que a navegação deve ir.

Normalmente, essas configurações só precisam ser feitas no modelo de página. No entanto, elas podem ser alteradas no nível da página por meio da [caixa](#edit-dialog)de diálogo de edição.

### Guia Propriedades {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Raiz da navegação**
   * É aqui que a navegação do idioma do site deve ser iniciada.
   * A estrutura de idioma do site começa no próximo nível abaixo desta raiz.
* **Profundidade da estrutura do idioma**
   * A árvore de conteúdo abaixo da Raiz **de navegação** representa a estrutura de idioma do site. Exemplos:
      * `1` geralmente significa que você tem apenas a opção de idioma.
      * `2` significa que você tem uma escolha de idioma e país.
      * `3` geralmente significa que você tem uma escolha de idioma, país e região.

#### Exemplo {#example}

Considere que o conteúdo é parecido com:

```
/content
+-- we-retail
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      +-- it
+-- wknd-events
\-- wknd-shop
```

Para o site We. Retail, você provavelmente desejaria colocar o componente Navegação de idioma em um modelo de página como parte do cabeçalho. Uma vez que parte do modelo é possível definir a Raiz **de navegação** do componente para `/content/we-retail` , uma vez que o conteúdo localizado para o site começa. Você também deve definir a Profundidade da estrutura **do idioma** como se `2` fosse uma estrutura de dois níveis (país em seguida, laguage).

Com o valor **Raiz** de navegação, o Componente de idioma sabe que depois `/content/we-retail` da navegação começa e pode gerar opções de navegação de idioma reconhecendo os próximos dois níveis na árvore de conteúdo como a estrutura de navegação do idioma do site (conforme definido pelo **valor Profundidade da** estrutura do idioma).

Não importa qual página um usuário está visualizando, o componente Navegação de idioma pode encontrar a página correspondente em outro idioma, ao saber o local da página atual e trabalhar de volta à raiz e encaminhar para a página correspondente.

### Guia Estilos {#styles-tab}

O componente de navegação de idioma é compatível com o sistema [de estilo do AEM](authoring.md#component-styling).

## Edit Dialog {#edit-dialog}

Normalmente, o componente de Navegação do Langauge precisa apenas ser adicionado e configurado nos modelos de página de um site. Entretanto, se o componente de Navegação de idioma precisar ser adicionado a uma página de conteúdo individual, a caixa de diálogo de edição permitirá que um autor de conteúdo configure os mesmos valores descritos na [caixa](#design-dialog)de diálogo de design.

![](assets/screen_shot_2018-01-12at133353.png)
