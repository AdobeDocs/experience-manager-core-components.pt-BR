---
title: Componente de botão (v1)
description: O componente de botão, dos componentes principais, permite a criação e a exibição de um botão.
role: Architect, Developer, Admin, User
exl-id: 63af16e4-dd4d-426d-88ef-769ecd1b3175
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '397'
ht-degree: 100%

---


# Componente de botão (v1) {#button-component}

O componente de Botão, dos Componentes principais, permite a configuração e a exibição de um item de botão em uma página.

## Uso {#usage}

O componente de Botão, dos Componentes principais, permite a inclusão de um botão em uma página.

* As propriedades do botão podem ser selecionadas na [caixa de diálogo de configuração](#configure-dialog).
* Os estilos do componente de Botão podem ser definidos na [caixa de diálogo de design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

O documento descreve a versão v1 do componente de botão, que foi introduzida com a versão 2.5.0 dos componentes principais em junho de 2019.

>[!CAUTION]
>
>Este documento descreve a versão v1 do componente de botão.
>
>Para obter detalhes sobre a versão atual do componente de botão, consulte o documento [Componente de botão](/help/components/button.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Botão, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_button).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Botão [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_button_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o botão e como ele se comportará e será exibido para um visitante da página.

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do componente de Botão](/help/assets/button-edit-properties.png)

* **Texto** - O texto a ser exibido no botão
* **Link** - Link para uma página de conteúdo no AEM, um recurso externo ou uma âncora
   * Use a **Caixa de diálogo de seleção** para escolher um caminho dentro do AEM.
* **Ícone** - Identificador para exibir um ícone no botão
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade da caixa de diálogo de edição do componente de Botão](/help/assets/button-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

## Caixa de diálogo de design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente de Botão é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Botão é compatível com a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
