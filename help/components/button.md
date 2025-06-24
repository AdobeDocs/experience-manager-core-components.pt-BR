---
title: Componente de Botão
description: O componente de Botão, dos Componentes principais, permite a criação e a exibição de um botão.
role: Architect, Developer, Admin, User
exl-id: e17efd1d-90d4-497a-9e7d-45934d81bc28
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 100%

---


# Componente de Botão {#button-component}

O componente de Botão, dos Componentes principais, permite a configuração e a exibição de um item de botão em uma página.

{{traditional-aem}}

## Uso {#usage}

O componente de Botão, dos Componentes principais, permite a inclusão de um botão em uma página.

* As propriedades do botão podem ser selecionadas na [caixa de diálogo de configuração](#configure-dialog).
* Os estilos do componente de Botão podem ser definidos na [caixa de diálogo de design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de botão é a v2, introduzida com a versão 2.18.0 dos componentes principais em fevereiro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v2 | - | Compatível | Compatível | Compatível |
| [v1](v1/button.md) | Compatível | Compatível | - | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Botão, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_button).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Botão [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_button_v2).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o botão e como ele se comportará e será exibido para um visitante da página.

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do componente de Botão](/help/assets/button-edit-properties.png)

* **Texto** - O texto a ser exibido no botão
* **Link** - Link para uma página de conteúdo no AEM, um recurso externo ou uma âncora
   * Use a **Caixa de diálogo de seleção** para escolher um caminho dentro do AEM.
* **Abrir link em nova guia** - Se marcada, o link será aberto em uma nova guia do navegador.
* **Ícone** - Identificador para exibir um ícone no botão
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade da caixa de diálogo de edição do componente de Botão](/help/assets/button-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

### Guia Estilos {#styles-tab-edit}

![Guia Estilos da caixa de diálogo de edição do componente de botão](/help/assets/button-edit-styles.png)

O componente de botão é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que o menu suspenso fique disponível.

## Caixa de diálogo de design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente de Botão é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Botão é compatível com a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
