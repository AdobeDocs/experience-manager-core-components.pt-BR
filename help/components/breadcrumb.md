---
title: Componente de navegação estrutural
description: O Componente de navegação estrutural principal é um componente de navegação que cria uma trilha de navegação de links com base na localização da página na hierarquia de conteúdo.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 2%

---


# Componente de navegação estrutural{#breadcrumb-component}

O Componente de navegação estrutural principal é um componente de navegação que cria uma trilha de navegação de links com base na localização da página na hierarquia de conteúdo.

## Uso {#usage}

O Componente de navegação estrutural exibe a posição da página atual dentro da hierarquia do site, permitindo que os visitantes de página naveguem na hierarquia da página a partir do local atual. Geralmente, isso é integrado aos cabeçalhos ou rodapés da página.

As opções disponíveis, como o nível de navegação padrão e a capacidade de mostrar a página atual ou páginas ocultas, podem ser definidas pelo autor do modelo na caixa de diálogo [de](#design-dialog)design. O editor de conteúdo pode escolher se as páginas ocultas devem ou não ser exibidas e o nível de navegação real do componente na caixa de diálogo [de](#edit-dialog)edição.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de navegação estrutural é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | - | Compatível | Compatível | Compatível |
| [v1](v1/breadcrumb-v1.md) | Compatível | Compatível | Compatível | - |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de navegação estrutural, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_breadcrumb)componentes.

>[!NOTE]
>
>A partir da versão 2.1.0 dos Componentes principais, o Componente de navegação estrutural suporta os microdados [](https://schema.org/BreadcrumbList)schema.org.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de navegação estrutural [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Edit Dialog {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo suprima páginas ocultas e ativas nas navegações estruturais, bem como a profundidade na hierarquia que deve ser exibida.

![Caixa de diálogo de edição de componentes da navegação estrutural](/help/assets/breadcrumb-edit.png)

* **Nível** do Start de navegação - onde na hierarquia o componente de navegação estrutural deve ser start para ir até a página atual. Por exemplo em We.Retail:

   * 0 start em `/content`
   * 1 start em `/content/<yourSite>`
   * 2 start em `/content/<yourSite>/<country>`

* **Mostrar itens** de navegação ocultos - Mostrar páginas marcadas como ocultas na navegação estrutural (por padrão, elas não serão exibidas)
* **Ocultar página** atual - Suprimir a página atual na navegação estrutural (por padrão, ela será exibida)
* **Desativar sombreamento** - Se a página na hierarquia for um redirecionamento, o nome da página de redirecionamento será exibido em vez do público alvo. Consulte o Suporte [à estrutura do site de](navigation.md#shadow-structure) sombra do Componente de navegação para obter mais informações.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais são os valores padrão para as opções de suprimir páginas ocultas e ativas nas navegações estruturais, bem como a profundidade na hierarquia que devem ser exibidas.

### Guia Principal {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **Nível** do Start de navegação - Define o valor padrão para onde na hierarquia o componente de navegação estrutural deve ser start para ir até a página atual quando o componente de navegação estrutural é adicionado a uma página.
* **Mostrar itens** de navegação ocultos - Define o valor padrão da opção **Mostrar itens** de navegação ocultos quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção do autor. Ela só define o valor padrão.

* **Ocultar página** atual - Define o valor padrão da opção **Ocultar página** atual quando o componente de navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção do autor. Ela só define o valor padrão.

* **Desativar sombreamento** - Define o valor padrão da opção **Desativar sombreamento** quando o componente da trilha de navegação é adicionado a uma página.

### Guia Estilos {#styles-tab}

O componente de navegação estrutural suporta o AEM [Style System](/help/get-started/authoring.md#component-styling).
