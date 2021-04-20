---
title: Componente Oculto do Formulário
description: O componente Componente principal Formulário oculto permite a exibição de um campo oculto.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 3%

---


# Componente oculto do formulário{#form-hidden-component}

O componente Componente principal Formulário oculto permite a exibição de um campo oculto.

## Uso {#usage}

O Componente principal de formulário oculto permite que a criação de campos ocultos transmita informações sobre a página atual de volta ao AEM e deve ser usado junto com o [componente do contêiner de formulário](form-container.md).

As propriedades do campo podem ser definidas pelo editor de conteúdo na caixa de diálogo [configurar](form-hidden.md).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de formulário oculto é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de formulário oculto, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_hidden).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de formulário oculto [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo configurar permite que o autor de conteúdo defina os parâmetros do campo oculto.

![Caixa de diálogo de edição oculta do formulário](/help/assets/form-hidden-edit.png)

* **Nome**  - O nome do campo, que é enviado com os dados do formulário
* **Valor**  - O valor do campo, que é enviado com os dados do formulário
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

Como o componente Formulário oculto normalmente não tem atributos visíveis, o espaço reservado do componente no editor exibe os valores dos campos **Nome** e **Valor** se estiverem atribuídos para ajudar o autor a identificar o componente Formulário oculto apropriado.

![Exemplo de componente oculto do formulário](/help/assets/form-hidden-example.png)

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente Formulário oculto é compatível com o AEM [Style System](/help/get-started/authoring.md#component-styling).
