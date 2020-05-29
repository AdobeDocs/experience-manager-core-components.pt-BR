---
title: Componente do botão
description: O componente de Botão Componente Principal permite a criação e a exibição de um botão.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 4%

---


# Componente do botão{#button-component}

O componente de Botão Componente Principal permite a configuração e a exibição de um item de botão em uma página.

## Uso {#usage}

O componente do botão Componente principal permite a inclusão de um botão em uma página.

* As propriedades do botão podem ser selecionadas na caixa de diálogo [](#configure-dialog)configurar.
* Os estilos para o componente Botão podem ser definidos na caixa de diálogo [de](#design-dialog)design.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de botão é v1, que foi introduzida com a versão 2.5.0 dos Componentes principais em junho de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o componente Botão e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_button)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do botão [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_button_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o botão e como ele se comportará e aparecerá para um visitante da página.

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo Editar do componente Botão](/help/assets/button-edit-properties.png)

* **Texto** - O texto a ser exibido no botão
* **Link** - Link para uma página de conteúdo no AEM, um recurso externo ou uma âncora
   * Use a caixa de diálogo **** de seleção para escolher um caminho no AEM.
* **Ícone** - Identificador para exibir um ícone no botão
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade da caixa de diálogo Editar do Componente de Botão](/help/assets/button-edit-accessibility.png)

Na guia **Acessibilidade** , os valores podem ser definidos para rótulos de acessibilidade [](https://www.w3.org/WAI/standards-guidelines/aria/) ARIA para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente de imagem suporta o sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
