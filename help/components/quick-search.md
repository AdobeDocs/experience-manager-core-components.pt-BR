---
title: Componente de pesquisa rápida
description: O Componente de pesquisa rápida fornece recursos de pesquisa para um site e apresenta resultados de pesquisa para que os visitantes possam pesquisar no site e filtrar os resultados.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 2%

---


# Componente de pesquisa rápida {#quick-search-component}

O Componente de pesquisa rápida fornece recursos de pesquisa para um site e apresenta resultados de pesquisa para que os visitantes possam encontrar facilmente conteúdo correspondente e resultados de visualização.

## Uso {#usage}

O componente de Pesquisa rápida oferta o site visitante a capacidade de pesquisar por conteúdo, visualização os resultados no local e navegar facilmente para as páginas correspondentes. Os novos resultados são obtidos dinamicamente à medida que o usuário rola os resultados da pesquisa.

A caixa de diálogo [edit](#edit-dialog) permite que o autor do conteúdo defina onde a pesquisa deve ser start na árvore de conteúdo. Usando a caixa de diálogo [design](#design-dialog), o autor do modelo pode definir o valor padrão para onde na árvore de conteúdo a pesquisa deve começar, bem como o tamanho máximo do conjunto de resultados e a duração mínima do termo de pesquisa.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de pesquisa rápida é a v1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

### Detalhes técnicos {#technical-details}

>[!NOTE]
>
>A proteção do componente de pesquisa ou de qualquer aplicativo baseado em AEM contra ataques de DOS deve ser implementada em um nível superior, por exemplo, usando `mod_security` no despachante.

A documentação técnica mais recente sobre o Componente de pesquisa rápida [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_search_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo defina onde a pesquisa deve ser start na árvore de conteúdo.

![Caixa de diálogo de edição do Componente de pesquisa rápida](/help/assets/quick-search-edit.png)

**Raiz**  de pesquisa - A página raiz de onde a pesquisa será start. A Raiz de pesquisa pode ser um blueprint principal, um idioma principal ou uma página regular.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [ de ](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

## Caixa de diálogo Design {#design-dialog}

Usando a caixa de diálogo de design, o autor do modelo pode definir o valor padrão para onde a pesquisa deve começar na árvore de conteúdo, bem como o tamanho máximo do conjunto de resultados e a duração mínima do termo de pesquisa. A caixa de diálogo de design permite que o autor do modelo defina quais opções de formatação de texto estão disponíveis para os autores do conteúdo.

### Guia Propriedades {#properties-tab}

![Caixa de diálogo de design do Componente de pesquisa rápida](/help/assets/quick-search-design.png)

* **Raiz**
de pesquisaO valor padrão da raiz de pesquisa quando um autor de conteúdo coloca o Componente de pesquisa rápida em uma página de conteúdo
* **Tamanho**
dos resultadosO número máximo de resultados obtidos por uma solicitação de pesquisa
* **Duração mínima do**
termo de pesquisaDuração mínima do termo de pesquisa para start da pesquisa

>[!NOTE]
>
>**O** Tamanho de resultados e o  **Lentidão mínimo de termos de** pesquisa só podem ser definidos no modo de design e, portanto, somente no nível do modelo, o que significa que os autores de conteúdo não podem modificar esses valores.

>[!CAUTION]
>
>**O** Tamanho de resultados e o  **Lentidão mínimo de termos de** pesquisa podem ter impacto no desempenho se forem definidos como muito altos ou muito baixos, respectivamente.

### Guia Estilos {#styles-tab}

O Componente de pesquisa rápida oferece suporte ao Sistema de estilo AEM [a1/>.](/help/get-started/authoring.md#component-styling)
