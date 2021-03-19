---
title: Componente de navegação estrutural (v1)
description: O Componente principal de navegação estrutural é um componente de navegação que cria uma navegação estrutural de links com base no local da página na hierarquia de conteúdo.
index: n
role: Arquiteto, Desenvolvedor, Administrador, Praticante de negócios
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 1%

---


# Componente de navegação estrutural (v1) {#breadcrumb-component-v}

O Componente principal de navegação estrutural é um componente de navegação que cria uma navegação estrutural de links com base no local da página na hierarquia de conteúdo.

## Uso {#usage}

O Componente de navegação estrutural exibe a posição da página atual na hierarquia do site, permitindo que os visitantes da página naveguem na hierarquia da página a partir do local atual. Geralmente, isso é integrado aos cabeçalhos ou rodapés da página.

As opções disponíveis, como o nível de navegação padrão e a capacidade de mostrar a página atual ou as páginas ocultas, podem ser definidas pelo autor do modelo na caixa de diálogo [design](#design-dialog). O editor de conteúdo pode então escolher se as páginas ocultas devem ser mostradas ou não, e o nível de navegação real do componente no [diálogo de edição](#edit-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente de navegação estrutural, introduzido originalmente com a versão 1.0.0 dos Componentes principais com a AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do Componente de navegação estrutural.

| Versão do AEM | Componente de navegação estrutural v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve v1 do Componente de navegação estrutural.
>Para obter detalhes sobre a versão atual do Componente de navegação estrutural, consulte o documento [Componente de navegação estrutural](/help/components/breadcrumb.md).

## Saída de componente de exemplo {#sample-component-output}

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
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Editar Caixa de Diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo suprima páginas ocultas e ativas na navegação estrutural, bem como a profundidade na hierarquia que deve ser exibida.

![](/help/assets/chlimage_1-34.png)

* **Nível de navegação para iniciar**  - Onde na hierarquia o componente de navegação estrutural deve começar a ir para a página atual. Por exemplo, em We.Retail:

   * 1 inicia em `/content/we-retail`
   * 2 inicia em `/content/we-retail/<country>`

* **Mostrar oculto**  - mostra as páginas marcadas como ocultas na navegação estrutural (por padrão, elas não serão exibidas)
* **Ocultar atual** - suprimir a página atual na navegação estrutural (por padrão, ela será exibida)

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais são os valores padrão para as opções de suprimir páginas ocultas e ativas na navegação estrutural, bem como a profundidade na hierarquia que deve ser exibida.

![](/help/assets/chlimage_1-35.png)

* **Nível de navegação para iniciar**  - Define o valor padrão para onde na hierarquia o componente de navegação estrutural deve começar a ir para a página atual quando o componente de navegação estrutural for adicionado a uma página.
* **Mostrar oculto**  - Define o valor padrão da opção  **Mostrar** oculto quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção para o autor. Ela só define o valor padrão.

* **Ocultar atual**  - Define o valor padrão da opção  **Ocultar** atual quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção para o autor. Ela só define o valor padrão.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de navegação estrutural [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb).

O projeto de componentes principais inteiro pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
