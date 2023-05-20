---
title: Componente de Botão de formulário
description: O componente Formulário Oculto, dos Componentes Principais, possibilita a inclusão de um campo oculto em um formulário.
role: Architect, Developer, Admin, User
exl-id: 1e5cff43-57db-4bfc-b2d2-23307eaf5eb3
source-git-commit: 16930ccaa281f9d9c4ddbb890d4222e128557580
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 100%

---

# Componente de Botão de formulário {#form-button-component}

O componente de Botão de formulário, dos Componentes principais, permite a inclusão de um botão para acionar uma ação em uma página.

## Uso {#usage}

O componente de Botão de formulário, dos Componentes principais, permite a criação de campo de botão, muitas vezes para acionar o envio do formulário e deve ser usado junto com o [componente de Contêiner de formulário](form-container.md).

As propriedades do botão podem ser definidas pelo editor de conteúdo na [caixa de diálogo de configuração](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Botão de formulário é a v2, introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível  com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | Compatível |
| [v1](/help/components/v1/form-button-v1.md) | Compatível | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Botão de Formulário, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_form_button_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Botão de formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina os parâmetros do botão.

### Guia Propriedades {#properties-tab}

![Caixa de diálogo de edição do componente de Botão de formulário](/help/assets/form-button-edit.png)

* **Tipo**

   * **Botão**
   * **Enviar**

* **Título** - O texto exibido no botão

   * Se nenhum for fornecido, o padrão será o tipo de botão

* **Nome** - O nome do botão, que é enviado com os dados de formulário
* **Valor** - O valor do botão, que é enviado com os dados de formulário

* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

## Caixa de diálogo de design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente Botão de formulário é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
