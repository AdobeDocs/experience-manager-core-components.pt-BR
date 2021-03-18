---
title: Componente do botão
description: O componente Botão Componente principal permite a criação e a exibição de um botão.
role: Arquiteto, Desenvolvedor, Administrador, Praticante de negócios
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 3%

---


# Componente do botão{#button-component}

O componente Botão do componente principal permite a configuração e a exibição de um item de botão em uma página.

## Uso {#usage}

O componente Botão do componente principal permite a inclusão de um botão em uma página.

* As propriedades do botão podem ser selecionadas na caixa de diálogo [configurar](#configure-dialog).
* Os estilos do Componente de botão podem ser definidos na caixa de diálogo [design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de botão é a v1, que foi introduzida com a versão 2.5.0 dos Componentes principais em junho de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de botão, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_button).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de botão [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_button_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o botão e como ele se comportará e será exibido para um visitante da página.

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo Editar do Componente de Botão](/help/assets/button-edit-properties.png)

* **Texto**  - O texto a ser exibido no botão
* **Link**  - Link para uma página de conteúdo no AEM, um recurso externo ou uma âncora
   * Use a **Caixa de diálogo de seleção** para escolher um caminho dentro do AEM.
* **Ícone**  - Identificador para exibição de um ícone no botão
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade da caixa de diálogo Editar do Componente de Botão](/help/assets/button-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para os rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo**  - Valor de um atributo de rótulo ARIA para o componente

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O Componente de Botão suporta o AEM [Sistema de Estilos](/help/get-started/authoring.md#component-styling).

## Camada de dados do cliente Adobe {#data-layer}

O Componente de Botão oferece suporte à Camada de Dados do Cliente do Adobe.](/help/developing/data-layer/overview.md)[
