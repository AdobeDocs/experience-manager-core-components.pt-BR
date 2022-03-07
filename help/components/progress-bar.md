---
title: Componente de Barra de progresso
description: O componente de Barra de progresso representa visualmente o progresso em direção a uma meta
role: Architect, Developer, Admin, User
exl-id: 47afc5a6-ac57-4b6c-92c4-015ca956a20b
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: ht
source-wordcount: '342'
ht-degree: 100%

---

# Componente de Barra de progresso {#progress-bar-component}

O componente de Barra de progresso, dos Componentes principais, representa o progresso em direção a uma meta.

## Uso {#usage}

O componente de Barra de progresso permite que o autor de conteúdo crie facilmente uma barra de progresso definindo uma porcentagem da conclusão, permitindo uma exibição visual intuitiva do progresso em direção a uma meta.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Barra de progresso é a v1, introduzida com a versão 2.9.0 dos Componentes principais em maio de 2020, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | Compatível |

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Barra de Progresso, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_progressbar_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente da Barra de progresso [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

![Caixa de diálogo de edição do componente de Barra de progresso](/help/assets/progress-bar-edit.png)

* **Conclusão** - O progresso conforme representado por uma porcentagem
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os estilos aplicados ao componente de Barra de progresso.

### Guia Estilos {#styles-tab}

O componente de Barra de progresso é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Barra de progresso suporta a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
