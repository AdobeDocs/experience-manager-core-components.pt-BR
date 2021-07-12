---
title: Componente de pesquisa rápida
description: O Componente de pesquisa rápida fornece recursos de pesquisa para um site e apresenta resultados de pesquisa para que os visitantes possam pesquisar no site e filtrar os resultados.
role: Architect, Developer, Admin, User
exl-id: fc40ce1d-e69a-4a40-853e-67a37228271b
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 1%

---

# Componente de pesquisa rápida {#quick-search-component}

O Componente de pesquisa rápida fornece recursos de pesquisa para um site e apresenta resultados de pesquisa para que os visitantes possam encontrar facilmente o conteúdo correspondente e visualizar os resultados.

## Uso {#usage}

O componente de Pesquisa rápida oferece aos visitantes do site a capacidade de pesquisar por conteúdo, visualizar os resultados no local e navegar facilmente até as páginas correspondentes. Novos resultados são buscados dinamicamente à medida que o usuário rola os resultados da pesquisa.

A [caixa de diálogo de edição](#edit-dialog) permite que o autor de conteúdo defina onde, na árvore de conteúdo, a pesquisa deve iniciar. Usando a caixa de diálogo [design](#design-dialog), o autor do modelo pode definir o valor padrão para onde a pesquisa deve começar na árvore de conteúdo, bem como o tamanho máximo do conjunto de resultados e a duração mínima do termo de pesquisa.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de pesquisa rápida é a v1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

### Detalhes técnicos {#technical-details}

>[!NOTE]
>
>A proteção do Componente de pesquisa ou de qualquer aplicativo baseado em AEM contra ataques de DOS deve ser implementada em um nível superior, por exemplo, usando `mod_security` no dispatcher.

A documentação técnica mais recente sobre o Componente de pesquisa rápida [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_search_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo defina onde a pesquisa deve iniciar na árvore de conteúdo.

![Caixa de diálogo de edição do Componente de pesquisa rápida](/help/assets/quick-search-edit.png)

**Raiz de pesquisa**  - A página raiz de onde a pesquisa deve ser iniciada. A Raiz de pesquisa pode ser um blueprint principal, idioma principal ou página regular.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada  [de dados.](/help/developing/data-layer/overview.md)
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

>[!NOTE]
>
>Se a **Raiz de Pesquisa** não estiver configurada ou não puder ser resolvida, a Pesquisa Rápida assumirá como padrão a pesquisa abaixo da página atual.

## Caixa de diálogo Design {#design-dialog}

Usando a caixa de diálogo de design, o autor do modelo pode definir o valor padrão para onde a pesquisa deve começar na árvore de conteúdo, bem como o tamanho máximo do conjunto de resultados e o comprimento mínimo do termo de pesquisa. A caixa de diálogo de design permite ao autor do modelo definir quais opções de formatação de texto estão disponíveis para os autores de conteúdo.

### Guia Propriedades {#properties-tab}

![Caixa de diálogo de design do Componente de pesquisa rápida](/help/assets/quick-search-design.png)

* **Raiz de pesquisa**
O valor padrão da raiz de pesquisa quando um autor de conteúdo coloca o Componente de pesquisa rápida em uma página de conteúdo
* **Tamanho**
dos resultadosO número máximo de resultados obtidos por uma solicitação de pesquisa
* **Tamanho mínimo do termo de pesquisaComprimento mínimo do**
termo de pesquisa para iniciar a pesquisa

>[!NOTE]
>
>**O** Tamanho Mínimo do Termo de  **** Pesquisa e do Tamanho dos Resultados só pode ser definido no modo de design e, portanto, somente no nível do modelo, o que significa que os autores de conteúdo não podem modificar esses valores.

>[!CAUTION]
>
>**O** tamanho dos resultados e o  **comprimento mínimo do termo de** pesquisa podem ter impacto no desempenho se forem definidos como muito altos ou muito baixos, respectivamente.

### Guia Estilos {#styles-tab}

O Componente de pesquisa rápida suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).
