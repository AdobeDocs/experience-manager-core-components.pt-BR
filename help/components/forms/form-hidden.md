---
title: Componente oculto do formulário
description: O componente principal Formulário oculto do componente permite a exibição de um campo oculto.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Componente oculto do formulário{#form-hidden-component}

O componente principal Formulário oculto do componente permite a exibição de um campo oculto.

## Uso {#usage}

O Componente principal Formulário oculto permite a criação de campos ocultos para retornar as informações sobre a página atual ao AEM e é destinado ao uso junto com o componente [de container de](form-container.md)formulário.

As propriedades de campo podem ser definidas pelo editor de conteúdo na caixa de diálogo [](form-hidden.md)configurar.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente oculto do formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o componente Oculto do formulário e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_form_hidden)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente oculto do formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina os parâmetros do campo oculto.

![Caixa de diálogo de edição oculta do formulário](/help/assets/form-hidden-edit.png)

* **Nome** - O nome do campo, que é enviado com os dados do formulário
* **Valor** - O valor do campo, que é submetido com os dados do formulário
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

Como o componente Form Oculto normalmente não tem atributos visíveis, o espaço reservado do componente no editor exibe os valores dos campos **Nome** e **Valor** se eles forem atribuídos para ajudar o autor a identificar o componente Form Oculto apropriado.

![Exemplo de componente oculto do formulário](/help/assets/form-hidden-example.png)

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente Oculto do formulário é compatível com o Sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
