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
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de trilha de navegação{#breadcrumb-component}

O componente de navegação estrutural do componente principal é um componente de navegação que cria uma navegação estrutural de links com base no local da página na hierarquia de conteúdo.

## Uso {#usage}

O componente de navegação estrutural exibe a posição da página atual na hierarquia do site, permitindo que os visitantes da página naveguem pela hierarquia da página a partir do seu local atual. Isso é frequentemente integrado aos cabeçalhos de página ou rodapés.

As opções disponíveis, como o nível de navegação padrão e a capacidade de mostrar a página atual ou páginas ocultas, podem ser definidas pelo autor do modelo na caixa de diálogo [de design](#design-dialog). O editor de conteúdo pode então escolher se páginas ocultas devem ser exibidas ou não e o nível de navegação real do componente na janela [de edição](#edit-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de navegação estrutural é v 2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatível | Compatível | Compatível |
| [v1](breadcrumb-v1.md) | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/chlimage_1.png)

### HTML {#html}

```
<nav class="cmp-breadcrumb">
    <ol class="cmp-breadcrumb__list">
        <li class="cmp-breadcrumb__item">
            <a href="/content/we-retail/us.html" class="cmp-breadcrumb__item-link">
                United States
            </a>
        </li>
    
        <li class="cmp-breadcrumb__item">
            <a href="/content/we-retail/us/en.html" class="cmp-breadcrumb__item-link">
                English
            </a>
        </li>
    
        <li class="cmp-breadcrumb__item cmp-breadcrumb__item--active">
            
                Experience
            
        </li>
    </ol>
</nav>
```

### JSON {#json}

```
"breadcrumb":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "items":[  
                        {  
                           "page":{  
                              "path":"/content/we-retail/us",
                              "pageTitle":null,
                              "name":"us",
                              "description":null,
                              "title":"United States"
                           },
                           "active":false
                        },
                        {  
                           "page":{  
                              "path":"/content/we-retail/us/en",
                              "pageTitle":null,
                              "name":"en",
                              "description":null,
                              "title":"English"
                           },
                           "active":false
                        },
                        {  
                           "page":{  
                              "path":"/content/we-retail/us/en/experience",
                              "pageTitle":null,
                              "name":"experience",
                              "description":null,
                              "title":"Experience"
                           },
                           "active":true
                        }
                     ],
                     ":type":"weretail/components/content/breadcrumb"
                  }
```

>[!NOTE]
>
>A partir da versão Components .1.0 dos Componentes principais, o componente da trilha de navegação suporta [schema.org microdados](https://schema.org/BreadcrumbList).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de navegação estrutural [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo Editar permite que o autor do conteúdo exclua páginas ocultas e ativas nas navegações estruturais, bem como a profundidade na hierarquia que ela deve ser exibida.

![](assets/screen_shot_2018-01-12at124250.png)

* **Nível de início de navegação** - Onde na hierarquia o componente da trilha de navegação deve começar para percorrer a página atual. Por exemplo, em We. Retail:

   * 0 inicia em `/content`

   * 1 inicia em `/content/we-retail`
   * 2 inicia em `/content/we-retail/<country>`

* **Mostrar itens de navegação ocultos** - Mostrar páginas marcadas como ocultas na navegação estrutural (por padrão, eles não serão exibidos)
* **Ocultar a página** atual - Suprimir a página atual na navegação estrutural (por padrão, ela será exibida)

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o que os valores padrão são para as opções de suprimir páginas ocultas e ativas nas navegações estruturais, bem como a profundidade na hierarquia que ela deve ser exibida.

### Guia Principal {#main-tab}

![](assets/screen_shot_2018-01-12at124437.png)

* **Nível de início de navegação** - define o valor padrão para onde, na hierarquia, o componente da trilha de navegação deve começar para se movimentar até a página atual quando o componente da navegação estrutural for adicionado a uma página.
* **Mostrar itens de navegação ocultos** - Define o valor padrão da opção **Mostrar itens** de navegação ocultos quando o componente de navegação estrutural é adicionado a uma página.

   * Isso não ativa ou desativa a opção para o autor. Ela apenas define o valor padrão.

* **Ocultar página** atual - Define o valor padrão da opção **Ocultar página** atual quando o componente de navegação estrutural é adicionado a uma página.

   * Isso não ativa ou desativa a opção para o autor. Ela apenas define o valor padrão.

### Guia Estilos {#styles-tab}

O componente de navegação estrutural é compatível com o Sistema [de estilo AEM](authoring.md#component-styling).