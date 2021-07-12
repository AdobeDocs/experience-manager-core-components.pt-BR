---
title: Componente da barra de progresso
description: O componente da barra de progresso representa visualmente o progresso em direção a uma meta
role: Architect, Developer, Admin, User
exl-id: 47afc5a6-ac57-4b6c-92c4-015ca956a20b
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 3%

---

# Componente da barra de progresso {#progress-bar-component}

O Componente de barra de progresso do componente principal representa o progresso em direção a uma meta.

## Uso {#usage}

O Componente de barra de progresso permite que o autor de conteúdo crie facilmente uma barra de progresso definindo uma porcentagem da conclusão, permitindo uma exibição visual intuitiva do progresso em direção a uma meta.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de barra de progresso é a v1, que foi introduzida com a versão 2.9.0 dos Componentes principais em maio de 2020, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | Compatível | Compatível |

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de barra de progresso, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_progressbar).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente da barra de progresso [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

![Caixa de diálogo de edição do Componente de barra de progresso](/help/assets/progress-bar-edit.png)

* **Conclusão**  - O progresso como representado por uma porcentagem
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os estilos aplicados ao Componente de barra de progresso.

### Guia Estilos {#styles-tab}

O Componente de barra de progresso suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

## Camada de dados do cliente Adobe {#data-layer}

O Componente de Barra de Progresso suporta a Camada de Dados do Cliente do Adobe [.](/help/developing/data-layer/overview.md)
