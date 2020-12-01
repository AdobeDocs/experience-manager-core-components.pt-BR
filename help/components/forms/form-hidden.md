---
title: Componente oculto do formulário
description: O componente principal Formulário oculto do componente permite a exibição de um campo oculto.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 3%

---


# Componente oculto do formulário{#form-hidden-component}

O componente principal Formulário oculto do componente permite a exibição de um campo oculto.

## Uso {#usage}

O Componente principal de formulário oculto permite que a criação de campos ocultos transmita informações sobre a página atual para AEM e é destinado a ser usado junto com o [componente de container de formulário](form-container.md).

As propriedades de campo podem ser definidas pelo editor de conteúdo na caixa de diálogo [configure](form-hidden.md).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente oculto do formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Oculto do formulário e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_hidden).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente oculto do formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina os parâmetros do campo oculto.

![Caixa de diálogo de edição oculta do formulário](/help/assets/form-hidden-edit.png)

* **Nome**  - O nome do campo, que é enviado com os dados do formulário
* **Valor**  - O valor do campo, que é submetido com os dados do formulário
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [ de ](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

Como o componente Form Hidden normalmente não tem atributos visíveis, o espaço reservado do componente no editor exibe os valores dos campos **Name** e **Value** se forem atribuídos para ajudar o autor a identificar o componente Form Hidden apropriado.

![Exemplo de componente oculto do formulário](/help/assets/form-hidden-example.png)

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente Oculto de formulário suporta o AEM [Sistema de estilo](/help/get-started/authoring.md#component-styling).
