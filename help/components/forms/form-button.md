---
title: Componente do botão de formulário
description: O componente Componente principal Formulário oculto permite a inclusão de um campo oculto em um formulário.
role: Arquiteto, Desenvolvedor, Administrador, Praticante de negócios
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 4%

---


# Componente do botão de formulário {#form-button-component}

O Componente de botão de formulário do componente principal permite a inclusão de um botão para acionar uma ação em uma página.

## Uso {#usage}

O componente do Botão de formulário do componente principal permite a criação de campo de botão, muitas vezes para acionar o envio do formulário e deve ser usado junto com o [componente do Contêiner de formulário](form-container.md).

As propriedades do botão podem ser definidas pelo editor de conteúdo na caixa de diálogo [configurar](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do botão de formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-button-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente do botão de formulário, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_button).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do botão de formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo configurar permite que o autor de conteúdo defina os parâmetros do botão.

### Guia Propriedades {#properties-tab}

![Caixa de diálogo de edição do componente do botão de formulário](/help/assets/form-button-edit.png)

* **Tipo**

   * **Botão**
   * **Enviar**

* **Título**  - O texto exibido no botão

   * Se nenhum fornecido, o padrão será o tipo de botão

* **Nome**  - O nome do botão, que é enviado com os dados do formulário
* **Valor**  - O valor do botão, que é enviado com os dados do formulário

* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O Componente do botão de formulário é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).
