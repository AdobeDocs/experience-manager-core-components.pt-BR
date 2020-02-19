---
title: Componente de navegação estrutural
description: O Componente de navegação estrutural principal é um componente de navegação que cria uma trilha de navegação de links com base na localização da página na hierarquia de conteúdo.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Componente de navegação estrutural{#breadcrumb-component}

O Componente de navegação estrutural principal é um componente de navegação que cria uma trilha de navegação de links com base na localização da página na hierarquia de conteúdo.

## Uso {#usage}

O Componente de navegação estrutural exibe a posição da página atual na hierarquia do site, permitindo que os visitantes da página naveguem na hierarquia da página a partir do local atual. Geralmente, isso é integrado aos cabeçalhos ou rodapés da página.

As opções disponíveis, como o nível de navegação padrão e a capacidade de mostrar a página atual ou páginas ocultas, podem ser definidas pelo autor do modelo na caixa de diálogo [de](#design-dialog)design. O editor de conteúdo pode escolher se as páginas ocultas devem ou não ser exibidas e o nível de navegação real do componente na caixa de diálogo [de](#edit-dialog)edição.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de navegação estrutural é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível | Compatível |
| [v1](v1/breadcrumb-v1.md) | Compatível | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](/help/versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de navegação estrutural, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_breadcrumb)componentes.

>[!NOTE]
>
>A partir da versão 2.1.0 dos Componentes principais, o Componente de navegação estrutural oferece suporte aos microdados [](https://schema.org/BreadcrumbList)schema.org.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de navegação estrutural [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Edit Dialog {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo suprima páginas ocultas e ativas nas navegações estruturais, bem como a profundidade na hierarquia que deve ser exibida.

![](/help/assets/screen_shot_2018-01-12at124250.png)

* **Nível** inicial de navegação - onde na hierarquia o componente de navegação estrutural deve começar a ir até a página atual. Por exemplo em We.Retail:

   * 0 inicia em `/content`
   * 1 começa em `/content/we-retail`
   * 2 começa em `/content/we-retail/<country>`

* **Mostrar itens** de navegação ocultos - Mostrar páginas marcadas como ocultas na navegação estrutural (por padrão, elas não serão exibidas)
* **Ocultar página** atual - Suprimir a página atual na navegação estrutural (por padrão, ela será exibida)

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais são os valores padrão para as opções de suprimir páginas ocultas e ativas nas navegações estruturais, bem como a profundidade na hierarquia que devem ser exibidas.

### Guia Principal {#main-tab}

![](/help/assets/screen_shot_2018-01-12at124437.png)

* **Nível** inicial de navegação - Define o valor padrão para onde na hierarquia o componente de navegação estrutural deve começar a ir até a página atual quando o componente de navegação estrutural é adicionado a uma página.
* **Mostrar itens** de navegação ocultos - Define o valor padrão da opção **Mostrar itens** de navegação ocultos quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção do autor. Ela só define o valor padrão.

* **Ocultar página** atual - Define o valor padrão da opção **Ocultar página** atual quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção do autor. Ela só define o valor padrão.

### Guia Estilos {#styles-tab}

O componente de navegação estrutural suporta o AEM [Style System](/help/get-started/authoring.md#component-styling).
