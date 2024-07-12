---
title: Componente de Navegação estrutural (v1)
description: O componente de Navegação estrutural, dos Componentes principais, é um componente de navegação que cria uma navegação estrutural de links com base no local da página na hierarquia de conteúdo.
index: n
role: Architect, Developer, Admin, User
exl-id: 4845e649-033a-43a8-b5ee-892a3f2a8b98
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 100%

---

# Componente de Navegação estrutural (v1) {#breadcrumb-component-v}

O componente de Navegação estrutural, dos Componentes principais, é um componente de navegação que cria uma navegação estrutural de links com base no local da página na hierarquia de conteúdo.

## Uso {#usage}

O componente de Navegação estrutural exibe a posição da página atual na hierarquia do site, permitindo que os visitantes da página naveguem na hierarquia da página a partir do local atual. Geralmente, isso é integrado aos cabeçalhos ou rodapés da página.

As opções disponíveis, como o nível de navegação padrão e a capacidade de mostrar a página atual ou as páginas ocultas, podem ser definidas pelo autor do modelo na [caixa de diálogo de design](#design-dialog). O editor de conteúdo pode então escolher se as páginas ocultas devem ser mostradas ou não, e o nível de navegação real do componente na [caixa de diálogo de edição](#edit-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do componente de Navegação estrutural, introduzido originalmente com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do componente de Navegação estrutural.

| Versão do AEM | Componente de Navegação estrutural v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do componente de Navegação estrutural.
>Para obter detalhes sobre a versão atual do componente de Navegação estrutural, consulte o documento [Componente de Navegação estrutural](/help/components/breadcrumb.md).

## Exemplo de saída do componente {#sample-component-output}

O exemplo a seguir foi retirado do [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=pt-BR).

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
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para mais informações.

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo suprima páginas ocultas e ativas na navegação estrutural, bem como a profundidade na hierarquia que deve ser exibida.

![](/help/assets/chlimage_1-34.png)

* **Nível de navegação para começar** - Onde na hierarquia o componente de navegação estrutural deve começar a ir para a página atual. Por exemplo, em We.Retail:

   * 1 inicia em `/content/we-retail`
   * 2 inicia em `/content/we-retail/<country>`

* **Mostrar ocultos** - Mostra as páginas marcadas como ocultas na navegação estrutural (por padrão, elas não serão exibidas)
* **Ocultar atual** - Suprime a página atual na navegação estrutural (por padrão, ela será exibida)

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais são os valores padrão para as opções de suprimir páginas ocultas e ativas na navegação estrutural, bem como a profundidade na hierarquia que deve ser exibida.

![](/help/assets/chlimage_1-35.png)

* **Nível de navegação para começar** - Define o valor padrão para onde, na hierarquia, o componente de navegação estrutural deve começar a descer para a página atual quando o componente de navegação estrutural for adicionado a uma página.
* **Mostrar ocultos** - Define o valor padrão da opção **Mostrar ocultos** quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção para o autor. Ela só define o valor padrão.

* **Ocultar atual** - Define o valor padrão da opção **Ocultar atual** quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção para o autor. Ela só define o valor padrão.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Navegação estrutural [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb).

Todo o projeto dos Componentes principais pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
