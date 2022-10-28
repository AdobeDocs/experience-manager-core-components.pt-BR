---
title: Componente de título de email
description: O Componente de título de email é um componente de cabeçalho de seção para seus emails que apresenta edição no local.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 51%

---


# Componente de título de email {#email-title-component}

O Componente de título de email é um componente de cabeçalho de seção para seus emails que apresenta edição no local.

## Uso {#usage}

O Componente Título do email deve ser usado como o título ou cabeçalho de uma seção de um email.

* Os níveis de cabeçalho disponíveis podem ser definidos pelo autor do modelo na [caixa de diálogo design.](#design-dialog)
* O autor de conteúdo pode selecionar entre os níveis de cabeçalho disponíveis na variável [editar caixa de diálogo.](#edit-dialog)

Para maior conveniência, a edição simples no local do texto do cabeçalho também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de título de email é a v1, que foi introduzida com a versão x dos Componentes principais de email em outubro de 2022, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos Componentes principais de email](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Título, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes.](https://adobe.com/go/aem_cmp_library_email_title)

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Título [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_email_title_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo defina o texto do título, e selecione o nível do cabeçalho.

* **Título** - Se estiver vazio, o título da página será usado
   * Clique no ícone Campanha para abrir o [Selecionar variável Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Tipo / Tamanho** - Define o nível de cabeçalho do título
* **Link** - Define o conteúdo ao qual o título será vinculado. Pode ser um caminho para uma página de conteúdo, um URL externo ou uma âncora de página.
   * Clique no ícone Campanha para abrir o [Selecionar variável Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML.
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração da ID pode afetar o CSS.

![Caixa de diálogo de edição do componente Título de email](/help/email/assets/email-title-edit.png)

O editor local também pode ser usado para editar o texto do componente de Título.

![Edição no local do componente Título do email](/help/email/assets/email-title-edit-inline.png)

### Guia Estilos {#styles-tab-edit}

O componente Título do email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que o menu suspenso esteja disponível.

![Guia Estilos da caixa de diálogo de edição do componente de título](/help/email/assets/email-title-edit-styles.png)

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o nível de cabeçalho padrão que os componentes de título terão quando criados pelos autores de conteúdo.

### Guia Tamanhos {#sizes-tab}

![Caixa de diálogo de design do componente de Título](/help/email/assets/email-title-design.png)

* **Tipos/tamanhos permitidos para Autores** - Ative ou desative os tipos de cabeçalho que estarão disponíveis para autores de conteúdo quando usarem o Componente de título de email .
* **Tipo/tamanho padrão** - Defina o tipo de cabeçalho que será atribuído automaticamente quando um autor de conteúdo adicionar o Componente de título de email a uma página.
* **Desativar link** - Desative o suporte para links no Componente de título de email para impedir que os autores de conteúdo vinculem de títulos.

### Guia Estilos {#styles-tab}

O componente Título do email é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).
