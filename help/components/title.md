---
title: Componente do título
description: O componente de Título, dos Componentes principais, é um componente de cabeçalho de seção que apresenta edição no local.
role: Architect, Developer, Admin, User
exl-id: 393af72c-549f-4609-afb0-2712f827b549
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '623'
ht-degree: 100%

---


# Componente de Título{#title-component}

O componente de Título, dos Componentes principais, é um componente de cabeçalho de seção que apresenta edição no local.

{{traditional-aem}}

## Uso {#usage}

O componente de Título deve ser usado como o título ou cabeçalho de uma seção de conteúdo. Os níveis de cabeçalho disponíveis podem ser definidos pelo autor do modelo na [caixa de diálogo design](#design-dialog). O editor de conteúdo pode selecionar a partir dos níveis de cabeçalho disponíveis na [caixa de diálogo de edição](#edit-dialog). Para maior conveniência, a edição simples no local do texto do cabeçalho também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de título é a v3, introduzida com a versão 2.18.0 dos componentes principais em fevereiro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v3 | - | Compatível | Compatível | Compatível |
| [v2](v2/title.md) | Compatível | Compatível | - | Compatível |
| [v1](v1/title-v1.md) | Compatível | Compatível | - | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Título, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_title_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Título [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_title_v3_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo defina o texto do título, e selecione o nível do cabeçalho.

* **Título** - Se estiver vazio, o título da página será usado
* **Tipo / Tamanho** - Define o nível de cabeçalho do título
* **Link** - Define o conteúdo ao qual o título será vinculado. Pode ser um caminho para uma página de conteúdo, um URL externo ou uma âncora de página.
* **Abrir link em nova guia** - Quando marcada, o link abrirá em uma nova guia do navegador.
* **ID**: Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

![Caixa de diálogo de edição do componente de Título](/help/assets/title-edit.png)

O editor local também pode ser usado para editar o texto do componente de Título.

![Edição no local do componente de Título](/help/assets/title-edit-inline.png)

### Guia Estilos {#styles-tab-edit}

O componente de título é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que o menu suspenso fique disponível.

![Guia Estilos da caixa de diálogo de edição do componente de título](/help/assets/title-edit-styles.png)

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o nível de cabeçalho padrão que os componentes de título terão quando criados pelos autores de conteúdo.

### Guia Tamanhos {#sizes-tab}

![Caixa de diálogo de design do componente de Título](/help/assets/title-design.png)

* **Tipos / tamanhos permitidos para editores** - Ativa ou desativa tipos de cabeçalho que estarão disponíveis para autores de conteúdo quando eles usarem o componente de Título.
* **Tipo / Tamanho padrão** - Define o tipo de cabeçalho que será atribuído automaticamente quando um autor de conteúdo adicionar o componente de Título a uma página.
* **Desabilitar link** - Desativa o suporte para links no componente de título para impedir que os autores de conteúdo vinculem de títulos.

### Guia Estilos {#styles-tab}

O componente de Título é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Título oferece suporte à [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
