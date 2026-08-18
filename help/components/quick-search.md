---
title: Componente de Pesquisa rápida
description: O componente de Pesquisa rápida fornece recursos de pesquisa para um site e apresenta resultados de pesquisa para que os visitantes possam pesquisar no site e filtrar os resultados, opcionalmente usando a pesquisa semântica habilitada por IA por meio do botão Pesquisa semântica.
role: Developer, Admin, User
exl-id: fc40ce1d-e69a-4a40-853e-67a37228271b
TQID: https://experienceleague.adobe.com/wU-3pacdEz9ne8b53-mKJy-XxRdyz2gu4Jvj-yFgGOw
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: f7fb04a4420a61d8a4755f2b3f09aad91b12c7eb
workflow-type: tm+mt
source-wordcount: 863
ht-degree: 46%

---


# Componente de Pesquisa rápida {#quick-search-component}

O componente de Pesquisa rápida fornece recursos de pesquisa para um site e apresenta resultados de pesquisa para que os visitantes possam encontrar facilmente o conteúdo correspondente e visualizar os resultados.

{{traditional-aem}}

## Uso {#usage}

O componente de Pesquisa rápida oferece aos visitantes do site a capacidade de pesquisar conteúdo, visualizar os resultados no local e navegar facilmente até as páginas correspondentes. Novos resultados são buscados dinamicamente à medida que o usuário rola os resultados da pesquisa.

A [caixa de diálogo de edição](#edit-dialog) permite que o autor de conteúdo defina onde a pesquisa deve iniciar na árvore de conteúdo e, opcionalmente, oculte a opção Pesquisa Semântica. Usando a [caixa de diálogo de design](#design-dialog), o autor do modelo pode definir o valor padrão para onde a pesquisa deve começar na árvore de conteúdo, o tamanho máximo do conjunto de resultados, a duração mínima do termo de pesquisa e se a opção Pesquisa semântica será mostrada aos visitantes por padrão.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Pesquisa rápida é a v3, introduzida com a [versão 2.32.0](/help/versions.md) dos Componentes principais, adicionando uma opção de Pesquisa semântica, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v3 | - | Compatível | Compatível | Compatível |
| [v2](/help/components/v2/quick-search.md) | - | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/quick-search.md) | Compatível com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | - | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

### Detalhes técnicos {#technical-details}

>[!NOTE]
>
>A proteção do componente de Pesquisa ou de qualquer aplicativo baseado no AEM contra ataques de DOS deve ser implementada em um nível superior, por exemplo, usando `mod_security` no dispatcher.

A documentação técnica mais recente sobre o componente de Pesquisa rápida [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_search_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo defina onde a pesquisa deve iniciar na árvore de conteúdo e oculte, opcionalmente, o botão de alternância Pesquisa semântica.

![Caixa de diálogo de edição do componente de Pesquisa rápida](/help/assets/quick-search-edit-v3.png)

**Pesquisar raiz** - A página raiz de onde a pesquisa deve ser iniciada. A Pesquisar raiz pode ser um blueprint principal, idioma principal ou página regular.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de dados](/help/developing/data-layer/overview.md).
  * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
  * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
  * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.
* **Ocultar alternância de Pesquisa Semântica nesta instância** - Quando marcada, a alternância de Pesquisa Semântica fica oculta, independentemente do que a [caixa de diálogo de design](#design-dialog) está configurada para mostrar.
  * Deixe desmarcada para usar o padrão do modelo.
  * Essa opção não pode forçar o botão de alternância a ser exibido em um local onde a caixa de diálogo de design o oculta.

>[!NOTE]
>
>Se a **Pesquisar raiz** não estiver configurada ou não puder ser resolvida, a Pesquisa rápida assumirá como padrão a pesquisa abaixo da página atual.

>[!NOTE]
>
>O botão Pesquisa semântica só retorna resultados alimentados por IA quando o ambiente é configurado com a IA de conteúdo do AEM. Nos ambientes LTS do AEM 6.5 e AEM 6.5 que não estão configurados com a IA de conteúdo, oculte o botão de alternância [usando a caixa de diálogo de design](#design-dialog) para que os visitantes não recebam um modo de pesquisa que não seja funcional.

## Caixa de diálogo de design {#design-dialog}

Usando a caixa de diálogo de design, o autor do modelo pode definir o valor padrão para onde a pesquisa deve começar na árvore de conteúdo, bem como o tamanho máximo do conjunto de resultados, a duração mínima do termo de pesquisa e se a opção Pesquisa semântica é exibida aos visitantes por padrão.

### Guia Propriedades {#properties-tab}

![Caixa de diálogo de design do componente de Pesquisa rápida](/help/assets/quick-search-design-v3.png)

* **Raiz de Pesquisa** - O valor padrão da raiz de pesquisa quando um autor de conteúdo coloca o Componente de Pesquisa Rápida em uma página de conteúdo
* **Tamanho dos Resultados** - O número máximo de resultados obtidos por uma solicitação de pesquisa
* **Tamanho Mínimo do Termo de Pesquisa** - Tamanho mínimo do termo de pesquisa para iniciar a pesquisa
* **Ocultar alternância de pesquisa semântica** - Quando marcada, a opção **Pesquisa semântica** descrita em [Uso](#usage) não é mostrada aos visitantes do site por padrão, e o componente se comporta como [o componente v2 (somente pesquisa de texto completo).](/help/components/v2/quick-search.md)
  * Desmarcado por padrão.
  * Os autores de conteúdo também podem substituir isso por um Componente de Pesquisa rápida individual na [caixa de diálogo de edição.](#edit-dialog)

>[!NOTE]
>
>O botão Pesquisa semântica só retorna resultados alimentados por IA quando o ambiente é configurado com a IA de conteúdo do AEM. Nos ambientes AEM 6.5 e AEM 6.5 LTS que não estão configurados com a IA de conteúdo, oculte o botão de alternância usando a caixa de diálogo de design para que os visitantes não recebam um modo de pesquisa que não seja funcional.

>[!NOTE]
>
>O **Tamanho dos resultados** e o **Tamanho mínimo do termo de pesquisa** só podem ser definidos no modo de design e, portanto, somente no nível do modelo, o que significa que os autores de conteúdo não podem modificar esses valores.

>[!CAUTION]
>
>O **Tamanho dos resultados** e o **Tamanho mínimo do termo de pesquisa** podem ter impacto no desempenho se forem definidos como muito altos ou muito baixos, respectivamente.

### Guia Estilos {#styles-tab}

O componente de Pesquisa rápida é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
