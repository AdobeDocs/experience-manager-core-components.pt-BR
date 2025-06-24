---
title: Componente de Pesquisa rápida
description: O componente de Pesquisa rápida fornece recursos de pesquisa para um site e apresenta resultados de pesquisa para que os visitantes possam pesquisar no site e filtrar os resultados.
role: Architect, Developer, Admin, User
exl-id: fc40ce1d-e69a-4a40-853e-67a37228271b
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 100%

---


# Componente de Pesquisa rápida {#quick-search-component}

O componente de Pesquisa rápida fornece recursos de pesquisa para um site e apresenta resultados de pesquisa para que os visitantes possam encontrar facilmente o conteúdo correspondente e visualizar os resultados.

{{traditional-aem}}

## Uso {#usage}

O componente de Pesquisa rápida oferece aos visitantes do site a capacidade de pesquisar conteúdo, visualizar os resultados no local e navegar facilmente até as páginas correspondentes. Novos resultados são buscados dinamicamente à medida que o usuário rola os resultados da pesquisa.

A [caixa de diálogo de edição](#edit-dialog) permite que o autor de conteúdo defina onde, na árvore de conteúdo, a pesquisa deve iniciar. Usando a [caixa de diálogo de design](#design-dialog), o autor do modelo pode definir o valor padrão para onde a pesquisa deve começar na árvore de conteúdo, bem como o tamanho máximo do conjunto de resultados e a duração mínima do termo de pesquisa.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Pesquisa rápida é a v2, introduzida com a versão 2.18.0 dos Componentes principais em janeiro de 2018, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | - | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/quick-search.md) | Compatível com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | - | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

### Detalhes técnicos {#technical-details}

>[!NOTE]
>
>A proteção do componente de Pesquisa ou de qualquer aplicativo baseado no AEM contra ataques de DOS deve ser implementada em um nível superior, por exemplo, usando `mod_security` no dispatcher.

A documentação técnica mais recente sobre o componente de Pesquisa rápida [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_search_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo defina onde a pesquisa deve iniciar na árvore de conteúdo.

![Caixa de diálogo de edição do componente de Pesquisa rápida](/help/assets/quick-search-edit.png)

**Pesquisar raiz** - A página raiz de onde a pesquisa deve ser iniciada. A Pesquisar raiz pode ser um blueprint principal, idioma principal ou página regular.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

>[!NOTE]
>
>Se a **Pesquisar raiz** não estiver configurada ou não puder ser resolvida, a Pesquisa rápida assumirá como padrão a pesquisa abaixo da página atual.

## Caixa de diálogo de design {#design-dialog}

Usando a caixa de diálogo de design, o autor do modelo pode definir o valor padrão para onde a pesquisa deve começar na árvore de conteúdo, bem como o tamanho máximo do conjunto de resultados e o comprimento mínimo do termo de pesquisa. A caixa de diálogo de design permite ao autor do modelo definir quais opções de formatação de texto estão disponíveis para os autores de conteúdo.

### Guia Propriedades {#properties-tab}

![Caixa de diálogo de design do componente de Pesquisa rápida](/help/assets/quick-search-design.png)

* **Pesquisar raiz**
O valor padrão da raiz de pesquisa quando um autor de conteúdo coloca o componente de Pesquisa rápida em uma página de conteúdo
* **Tamanho dos resultados**
O número máximo de resultados obtidos por uma solicitação de pesquisa
* **Tamanho mínimo do termo de pesquisa**
Comprimento mínimo do termo de pesquisa para iniciar a pesquisa

>[!NOTE]
>
>O **Tamanho dos resultados** e o **Tamanho mínimo do termo de pesquisa** só podem ser definidos no modo de design e, portanto, somente no nível do modelo, o que significa que os autores de conteúdo não podem modificar esses valores.

>[!CAUTION]
>
>O **Tamanho dos resultados** e o **Tamanho mínimo do termo de pesquisa** podem ter impacto no desempenho se forem definidos como muito altos ou muito baixos, respectivamente.

### Guia Estilos {#styles-tab}

O componente de Pesquisa rápida é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
