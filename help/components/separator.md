---
title: Componente separador
description: O componente separador cria uma quebra entre componentes em uma página
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 5%

---


# Componente separador {#separator-component}

O Componente de separação do componente principal exibe uma regra horizontal para separar o conteúdo.

## Uso {#usage}

O Componente de separação permite que o autor de conteúdo crie facilmente uma regra horizontal como uma quebra entre o conteúdo para organizar melhor as informações em uma página.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de separação é v1, que foi introduzida com a versão 2.3.0 dos Componentes principais em fevereiro de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | Compatível | Compatível |

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de separação, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_separator).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de separação [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_separator_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

![Caixa de diálogo de edição do componente separador](/help/assets/separator-edit.png)

* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os estilos aplicados ao Componente de separação.

### Guia Estilos {#styles-tab}

O Componente de Separador suporta o AEM [Sistema de Estilos](/help/get-started/authoring.md#component-styling).
