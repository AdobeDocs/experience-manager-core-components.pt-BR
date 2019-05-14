---
title: Componente do título
seo-title: Componente do título
description: 'null'
seo-description: O Componente de título do componente principal é um componente de cabeçalho de seção que inclui a edição no local.
uuid: cf 190861-e 5 cd -42 b 8-9193-842 b 8 df 8 c 5 c 6
contentOwner: Usuário
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 243 efc 75-fcf 9-427 d -9303-9642 b 0602991
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b179888d19a95257602656d456d5c6bfe82877af

---


# Componente do título{#title-component}

O Componente de título do componente principal é um componente de cabeçalho de seção que inclui a edição no local.

## Uso {#usage}

O componente de título deve ser usado como título ou cabeçalho de uma seção do conteúdo. Os níveis de cabeçalho disponíveis podem ser definidos pelo autor do modelo na caixa de diálogo [de design](#design-dialog). O editor de conteúdo pode selecionar os níveis de cabeçalhos disponíveis na caixa de diálogo [de edição](#edit-dialog). Para maior conveniência, a edição simples no local do cabeçalho também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de título é v 2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v2 | Compatível | Compatível | Compatível |
| [v1](title-v1.md) | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/chlimage_1-36.png)

### Biblioteca de componentes

Para experimentar o Componente de título, bem como ver exemplos de suas opções de configuração, além de HTML e saída JSON, visite a Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/title.html).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de título [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo Editar permite que o autor do conteúdo defina o texto do título e selecione o nível de cabeçalho.

* **Título** - se estiver vazio, o título da página será usado
* **Tipo/Tamanho** - define o nível de cabeçalho do título
* **Link** - define o conteúdo para o qual o título será vinculado. Pode ser um caminho para uma página de conteúdo, um URL externo ou uma âncora de página.

![](assets/screenshot_2018-10-19at110055.png)

>[!CAUTION]
>
>A capacidade de definir um link para o título foi introduzida com a versão 2.2.0 dos Componentes principais.

O editor local também pode ser usado para editar o texto do componente de título.

![](assets/chlimage_1-37.png)

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o nível de cabeçalho padrão que os componentes de título terão quando criados pelos autores de conteúdo.

### Guia Tamanhos {#sizes-tab}

![](assets/screenshot_2018-10-19at110120.png)

* **Tipos/tamanhos permitidos para autores** - ativa ou desativa os tipos de cabeçalho que estarão disponíveis para autores de conteúdo quando usam o componente de título.
* **Tipo/Tamanho padrão**- Define o tipo de cabeçalho que será atribuído automaticamente quando um autor de conteúdo adiciona o Componente de título a uma página.
* **Desativar o suporte**- Desabilitar suporte para links no componente de título para proibir que autores de conteúdo vinculem a títulos.

>[!CAUTION]
>
>A capacidade de definir um link para o título foi introduzida com a versão 2.2.0 dos Componentes principais.

### Guia Estilos {#styles-tab}

O Componente de título é compatível com o Sistema [de estilo AEM](authoring.md#component-styling).