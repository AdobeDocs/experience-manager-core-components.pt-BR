---
title: Componente de navegação estrutural
description: O Componente principal de navegação estrutural é um componente de navegação que cria uma navegação estrutural de links com base no local da página na hierarquia de conteúdo.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 2%

---


# Componente de navegação estrutural{#breadcrumb-component}

O Componente principal de navegação estrutural é um componente de navegação que cria uma navegação estrutural de links com base no local da página na hierarquia de conteúdo.

## Uso {#usage}

O Componente de navegação estrutural exibe a posição da página atual na hierarquia do site, permitindo que os visitantes da página naveguem na hierarquia da página a partir do local atual. Geralmente, isso é integrado aos cabeçalhos ou rodapés da página.

As opções disponíveis, como o nível de navegação padrão e a capacidade de mostrar a página atual ou as páginas ocultas, podem ser definidas pelo autor do modelo na caixa de diálogo [design](#design-dialog). O editor de conteúdo pode então escolher se as páginas ocultas devem ser mostradas ou não, e o nível de navegação real do componente no [diálogo de edição](#edit-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de navegação estrutural é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- | --- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](v1/breadcrumb-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de navegação estrutural, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_breadcrumb).

>[!NOTE]
>
>Desde a versão 2.1.0 dos Componentes principais, o Componente de navegação estrutural suporta [schema.org microdata](https://schema.org/BreadcrumbList).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de navegação estrutural [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Editar Caixa de Diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo suprima páginas ocultas e ativas na navegação estrutural, bem como a profundidade na hierarquia que deve ser exibida.

![Caixa de diálogo de edição de componentes da navegação estrutural](/help/assets/breadcrumb-edit.png)

* **Nível de início da navegação**  - Onde na hierarquia o componente de navegação estrutural deve começar a ir para a página atual. Por exemplo:

   * 0 inicia em `/content`
   * 1 inicia em `/content/<yourSite>`
   * 2 inicia em `/content/<yourSite>/<country>`

* **Mostrar itens de navegação ocultos**  - Mostrar páginas marcadas como ocultas na navegação estrutural (por padrão, elas não serão exibidas)
* **Ocultar página**  atual - Suprimir a página atual na navegação estrutural (por padrão, ela será exibida)
* **Desativar sombreamento**  - Se a página na hierarquia for um redirecionamento, o nome da página de redirecionamento será exibido em vez do destino. Consulte o [Suporte à estrutura do site de sombra](navigation.md#shadow-structure) do Componente de navegação para obter mais informações.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais são os valores padrão para as opções de suprimir páginas ocultas e ativas na navegação estrutural, bem como a profundidade na hierarquia que deve ser exibida.

### Guia Principal {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **Nível inicial de navegação**  - Define o valor padrão para onde na hierarquia o componente de navegação estrutural deve começar a ir para a página atual quando o componente de navegação estrutural for adicionado a uma página.
* **Mostrar itens de navegação ocultos**  - Define o valor padrão da opção  **Mostrar itens de navegação ocultos** quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção para o autor. Ela só define o valor padrão.

* **Ocultar página atual** - Define o valor padrão da opção  **Ocultar** página atual quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção para o autor. Ela só define o valor padrão.

* **Desativar sombreamento**  - Define o valor padrão da opção  **Desativar** sombreamento quando o componente de navegação estrutural for adicionado a uma página.

### Guia Estilos {#styles-tab}

O Componente de navegação estrutural suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

## Camada de dados do cliente Adobe {#data-layer}

O componente de navegação estrutural suporta a [Camada de Dados do Cliente Adobe.](/help/developing/data-layer/overview.md)
