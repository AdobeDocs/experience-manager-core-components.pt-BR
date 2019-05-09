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
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de navegação de idioma{#language-navigation-component}

O componente de navegação de idioma fornece uma navegação de idioma/país para um site, para que os visitantes possam navegar até a mesma página em uma localidade diferente.

## Uso {#usage}

Geralmente, os sites são fornecidos em vários idiomas para diferentes regiões. O componente de navegação de idioma permite que um visitante visualize a mesma página em idiomas/localidades diferentes.

A caixa de diálogo [Editar](#edit-dialog) permite a definição da raiz de navegação do site global, bem como a profundidade da estrutura que a navegação deve ir. Usando a [caixa de diálogo de design](#design-dialog), o autor do modelo pode definir os valores padrão para as mesmas opções.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de navegação de idioma é v 1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatível | Compatível | Compatível |


Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/screen_shot_2018-01-12at133119.png)

### HTML {#html}

```
<nav class="cmp-languagenavigation">
    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-en cmp-languagenavigation__item--level-0 cmp-languagenavigation__item--active">
        
    <span class="cmp-languagenavigation__item-title" lang="en">United States</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-en cmp-languagenavigation__item--level-1 cmp-languagenavigation__item--active">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/us/en/equipment.html" hreflang="en" lang="en" rel="alternate" title="English">English</a>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-es cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/us/es.html" hreflang="es" lang="es" rel="alternate" title="Español">Español</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CA cmp-languagenavigation__item--langcode-en-CA cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="en-CA">Canada</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CA cmp-languagenavigation__item--langcode-en-CA cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/ca/en/equipment.html" hreflang="en-CA" lang="en-CA" rel="alternate" title="English">English</a>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CA cmp-languagenavigation__item--langcode-en-CA cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/ca/fr.html" hreflang="en-CA" lang="en-CA" rel="alternate" title="Français">Français</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CH cmp-languagenavigation__item--langcode-de-CH cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="de-CH">Switzerland</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CH cmp-languagenavigation__item--langcode-de-CH cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/ch/de.html" hreflang="de-CH" lang="de-CH" rel="alternate" title="Deutsch">Deutsch</a>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CH cmp-languagenavigation__item--langcode-de-CH cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/ch/fr.html" hreflang="de-CH" lang="de-CH" rel="alternate" title="Français">Français</a>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CH cmp-languagenavigation__item--langcode-de-CH cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/ch/it.html" hreflang="de-CH" lang="de-CH" rel="alternate" title="Italiano">Italiano</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-de cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="de">Germany</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-de cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/de/de.html" hreflang="de" lang="de" rel="alternate" title="Deutsch">Deutsch</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-fr cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="fr">France</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-fr cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/fr/fr.html" hreflang="fr" lang="fr" rel="alternate" title="Français">Français</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-es cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="es">Spain</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-es cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/es/es.html" hreflang="es" lang="es" rel="alternate" title="Español">Español</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-it cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="it">Italy</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-it cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/it/it.html" hreflang="it" lang="it" rel="alternate" title="Italiano">Italiano</a>

    </li>

    </ul>

    </li>

    </ul>
</nav>
```

### JSON {#json}

```
"languagenavigation":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "items":[  
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":true,
                                 "title":"English",
                                 "locale":"en",
                                 "country":"",
                                 "language":"en",
                                 "url":"/content/we-retail/us/en/equipment.html",
                                 "path":"/content/we-retail/us/en/equipment",
                                 "description":null,
                                 "lastModified":1515760174857
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Español",
                                 "locale":"es",
                                 "country":"",
                                 "language":"es",
                                 "url":"/content/we-retail/us/es.html",
                                 "path":"/content/we-retail/us/es",
                                 "description":null,
                                 "lastModified":1474673505454
                              }
                           ],
                           "level":0,
                           "active":true,
                           "title":"United States",
                           "locale":"en",
                           "country":"",
                           "language":"en",
                           "url":"/content/we-retail/us/en/equipment.html",
                           "path":"/content/we-retail/us/en/equipment",
                           "description":null,
                           "lastModified":1515760174857
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"English",
                                 "locale":"en_CA",
                                 "country":"CA",
                                 "language":"en-CA",
                                 "url":"/content/we-retail/ca/en/equipment.html",
                                 "path":"/content/we-retail/ca/en/equipment",
                                 "description":null,
                                 "lastModified":1477493028617
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Français",
                                 "locale":"en_CA",
                                 "country":"CA",
                                 "language":"en-CA",
                                 "url":"/content/we-retail/ca/fr.html",
                                 "path":"/content/we-retail/ca/fr",
                                 "description":null,
                                 "lastModified":1474673388792
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"Canada",
                           "locale":"en_CA",
                           "country":"CA",
                           "language":"en-CA",
                           "url":"/content/we-retail/ca/en/equipment.html",
                           "path":"/content/we-retail/ca/en/equipment",
                           "description":null,
                           "lastModified":1477493028617
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Deutsch",
                                 "locale":"de_CH",
                                 "country":"CH",
                                 "language":"de-CH",
                                 "url":"/content/we-retail/ch/de.html",
                                 "path":"/content/we-retail/ch/de",
                                 "description":null,
                                 "lastModified":1474673744891
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Français",
                                 "locale":"de_CH",
                                 "country":"CH",
                                 "language":"de-CH",
                                 "url":"/content/we-retail/ch/fr.html",
                                 "path":"/content/we-retail/ch/fr",
                                 "description":null,
                                 "lastModified":1474673356319
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Italiano",
                                 "locale":"de_CH",
                                 "country":"CH",
                                 "language":"de-CH",
                                 "url":"/content/we-retail/ch/it.html",
                                 "path":"/content/we-retail/ch/it",
                                 "description":null,
                                 "lastModified":1474673460578
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"Switzerland",
                           "locale":"de_CH",
                           "country":"CH",
                           "language":"de-CH",
                           "url":"/content/we-retail/ch.html",
                           "path":"/content/we-retail/ch",
                           "description":null,
                           "lastModified":1474673057327
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Deutsch",
                                 "locale":"de",
                                 "country":"",
                                 "language":"de",
                                 "url":"/content/we-retail/de/de.html",
                                 "path":"/content/we-retail/de/de",
                                 "description":null,
                                 "lastModified":1474673744681
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"Germany",
                           "locale":"de",
                           "country":"",
                           "language":"de",
                           "url":"/content/we-retail/de.html",
                           "path":"/content/we-retail/de",
                           "description":null,
                           "lastModified":1474673019700
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Français",
                                 "locale":"fr",
                                 "country":"",
                                 "language":"fr",
                                 "url":"/content/we-retail/fr/fr.html",
                                 "path":"/content/we-retail/fr/fr",
                                 "description":null,
                                 "lastModified":1474673321300
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"France",
                           "locale":"fr",
                           "country":"",
                           "language":"fr",
                           "url":"/content/we-retail/fr.html",
                           "path":"/content/we-retail/fr",
                           "description":null,
                           "lastModified":1474672999375
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Español",
                                 "locale":"es",
                                 "country":"",
                                 "language":"es",
                                 "url":"/content/we-retail/es/es.html",
                                 "path":"/content/we-retail/es/es",
                                 "description":null,
                                 "lastModified":1474673542068
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"Spain",
                           "locale":"es",
                           "country":"",
                           "language":"es",
                           "url":"/content/we-retail/es.html",
                           "path":"/content/we-retail/es",
                           "description":null,
                           "lastModified":1474673075638
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Italiano",
                                 "locale":"it",
                                 "country":"",
                                 "language":"it",
                                 "url":"/content/we-retail/it/it.html",
                                 "path":"/content/we-retail/it/it",
                                 "description":null,
                                 "lastModified":1474673426215
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"Italy",
                           "locale":"it",
                           "country":"",
                           "language":"it",
                           "url":"/content/we-retail/it.html",
                           "path":"/content/we-retail/it",
                           "description":null,
                           "lastModified":1474673037021
                        }
                     ],
                     ":type":"core/wcm/sandbox/components/languagenavigation/v1/languagenavigation"
                  }
```

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de navegação de idioma [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo Editar permite a definição da raiz de navegação do site global, bem como a profundidade da estrutura que a navegação deve ir.

![](assets/screen_shot_2018-01-12at133353.png)

* **Raiz
de navegação** Define a página raiz da estrutura de navegação.
   * Use o botão **Abrir caixa de diálogo** de seleção para navegar facilmente pela estrutura do conteúdo e selecionar a raiz.
* **Profundidade de profundidade**
da estrutura do idioma da estrutura de idioma global relativa à raiz de navegação.

## Caixa de diálogo de design {#design-dialog}

Usando a caixa de diálogo de design, o autor do modelo pode definir os valores padrão para as mesmas opções disponíveis na janela de edição.

### Guia Propriedades {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Valor padrão de**navegação da
raiz de navegação quando um autor de conteúdo posiciona o componente Alternador de idiomas em uma página de conteúdo
* **Valor padrão de Profundidade**
da estrutura de idioma da profundidade da estrutura de idioma quando um autor de conteúdo posiciona o Componente Alternador de idiomas em uma página de conteúdo

### Guia Estilos {#styles-tab}

O componente de navegação de idioma é compatível com o sistema [de estilo do AEM](authoring.md#component-styling).