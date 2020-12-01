---
title: Componente da trilha de navegação (v1)
description: O Componente de navegação estrutural principal é um componente de navegação que cria uma trilha de navegação de links com base na localização da página na hierarquia de conteúdo.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 1%

---


# Componente de navegação estrutural (v1) {#breadcrumb-component-v}

O Componente de navegação estrutural principal é um componente de navegação que cria uma trilha de navegação de links com base na localização da página na hierarquia de conteúdo.

## Uso {#usage}

O Componente de navegação estrutural exibe a posição da página atual dentro da hierarquia do site, permitindo que os visitantes de página naveguem na hierarquia da página a partir do local atual. Geralmente, isso é integrado aos cabeçalhos ou rodapés da página.

As opções disponíveis, como o nível de navegação padrão e a capacidade de mostrar a página atual ou as páginas ocultas, podem ser definidas pelo autor do modelo na caixa de diálogo [design](#design-dialog). O editor de conteúdo pode escolher se as páginas ocultas devem ou não ser mostradas e o nível de navegação real do componente na caixa de diálogo [edit](#edit-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a versão 1 do Componente de navegação estrutural, originalmente introduzido com a versão 1.0.0 dos Componentes principais com a AEM 6.3.

A tabela a seguir lista a compatibilidade de v1 do Componente de navegação estrutural.

| Versão do AEM | Componente de navegação estrutural v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do Componente de navegação estrutural.
>Para obter detalhes sobre a versão atual do Componente de navegação estrutural, consulte o documento [Componente de navegação estrutural](/help/components/breadcrumb.md).

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](/help/assets/chlimage_1-33.png)

### HTML {#html}

```
<div class="cmp cmp-breadcrumb aem-GridColumn aem-GridColumn--default--12">

<ol class="breadcrumb">
    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us.html">
            United States
        </a>
    </li>

    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us/en.html">
            English
        </a>
    </li>

    <li class="breadcrumb-item active">
        
            Experience
        
    </li>
</ol>
 
</div>
```

### JSON {#json}

```
"breadcrumb": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/breadcrumb"
            }
```

>[!NOTE]
>
>A exportação JSON dos Componentes principais exige a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo suprima páginas ocultas e ativas nas navegações estruturais, bem como a profundidade na hierarquia que deve ser exibida.

![](/help/assets/chlimage_1-34.png)

* **Nível de navegação para start**  - onde na hierarquia o componente de navegação estrutural deve ser start para ir até a página atual. Por exemplo em We.Retail:

   * 1 start em `/content/we-retail`
   * 2 start em `/content/we-retail/<country>`

* **Mostrar ocultos**  - Mostrar páginas marcadas como ocultas na navegação estrutural (por padrão, elas não serão exibidas)
* **Ocultar atual** - Suprimir a página atual na navegação estrutural (por padrão, ela será exibida)

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais são os valores padrão para as opções de suprimir páginas ocultas e ativas nas navegações estruturais, bem como a profundidade na hierarquia que devem ser exibidas.

![](/help/assets/chlimage_1-35.png)

* **Nível de navegação para start** : define o valor padrão para onde na hierarquia o componente de navegação estrutural deve ser start para ir até a página atual quando o componente de navegação estrutural é adicionado a uma página.
* **Mostrar oculto**  - define o valor padrão da opção  **Mostrar** oculta quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção do autor. Ela só define o valor padrão.

* **Ocultar atual**  - define o valor padrão da opção  **Ocultar** atual quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção do autor. Ela só define o valor padrão.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de navegação estrutural [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb).

Todo o projeto de componentes principais pode ser baixado do GitHub.

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
