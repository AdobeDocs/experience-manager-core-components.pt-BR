---
title: Componente de teaser de email
description: O Componente de teaser de email pode mostrar uma imagem, um título, um texto formatado e, opcionalmente, um link para mais conteúdo.
role: Architect, Developer, Admin, User
exl-id: d6123b22-7cba-406c-986d-b6f00322d135
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 99%

---


# Componente de teaser de email {#email-teaser-component}

O Componente de teaser de email pode mostrar uma imagem, um título, um texto formatado e, opcionalmente, um link para mais conteúdo.

## Uso {#usage}

O Componente de teaser de email permite que o autor do conteúdo crie facilmente um teaser usando uma imagem, um título ou um texto formatado e adicione um link para outros conteúdos ou ações.

* O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir se as opções para criar frases de chamariz e adicionar links estão disponíveis, bem como desativar várias opções de exibição.
* O autor do conteúdo pode usar o [a caixa de diálogo de configuração](#configure-dialog) para configurar uma imagem, definir CTAs, definir títulos e descrições e configurar links para o teaser individual.
* A [caixa de diálogo de edição](image.md#edit-dialog) do [Componente de imagem de email](image.md) pode ser acessada para modificar a imagem do teaser.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de teaser de email é a v1, que foi introduzida com a versão x dos Componentes principais de email em outubro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | - | - |

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de teaser de email [pode ser encontrada no GitHub.](https://adobe.com/go/aem_cmp_tech_email_teaser_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

O autor do conteúdo pode usar a caixa de diálogo de configuração para definir as propriedades do teaser individual. Também há uma [caixa de diálogo de edição](#edit-dialog) para modificar a imagem do teaser, se essa opção estiver selecionada.

### Guia Links {#links-tab}

![Guia de links para a caixa de diálogo de edição do Componente de teaser de email](/help/email/assets/email-teaser-edit-links.png)

O título, a descrição e a imagem do teaser podem ser herdados do conteúdo vinculado ou do conteúdo vinculado na primeira frase de chamariz. Se nem um link nem uma frase de chamariz forem especificados, o título, a descrição e a imagem serão herdados do conteúdo atual.

* **Link** - Este arquivo contém um link para um conteúdo, um URL externo ou uma âncora.
   * Clique no ícone Campaign para abrir a caixa de diálogo [Selecionar variável do Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Frases de chamariz** - Esta opção permite vincular a vários destinos.
   * A página vinculada na primeira frase de chamariz é usada ao herdar o título, a descrição ou a imagem do teaser.
   * Clique no ícone Campanha para abrir a caixa de diálogo [Selecionar variável do Adobe Campaign](/help/email/campaign-variables.md) e inserir conteúdo dinâmico do Adobe Campaign.

### Guia Texto {#text-tab}

![Guia Texto da caixa de diálogo de edição do Componente de teaser de email](/help/email/assets/email-teaser-edit-text.png)

* **Pre-título** - O pre-título será exibido antes do título do teaser.
* **Título** - Define um título a ser exibido como o título do teaser.
   * Clique no ícone Campanha para abrir a caixa de diálogo [Selecionar variável do Adobe Campaign](/help/email/campaign-variables.md) e inserir conteúdo dinâmico do Adobe Campaign.
   * **Obter título da página vinculada** - Quando marcado, o título será preenchido com o título da página vinculada.
* **Descrição** - Define uma descrição a ser exibida como o subtítulo do teaser.
   * Clique no ícone **Selecionar variável do Adobe Campaign** para abrir a caixa de diálogo [Selecionar variável do Adobe Campaign](/help/email/campaign-variables.md) e inserir conteúdo dinâmico do Adobe Campaign.
   * **Obter descrição da página vinculada** - Quando marcada, a descrição será preenchida com a descrição da página vinculada.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML.
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração de ID pode afetar o CSS.

### Guia Ativo {#asset-tab}

![Guia Imagem da caixa de diálogo de edição do Componente de teaser de email](/help/email/assets/email-teaser-edit-image.png)

* **Herdar imagem em destaque da página** - Use a imagem definida nas propriedades da página vinculada ou da página atual, se nenhuma for encontrada.
* **Ativo de imagem** - Solte um ativo do [navegador de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR) ou toque na opção **procurar** para fazer upload a partir de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=pt-BR) no Editor de ativos.
* **Texto alternativo para acessibilidade** - Este campo permite definir uma descrição da imagem para usuários com deficiências visuais.
   * **Herdar texto alternativo da página** - Esta opção utiliza a descrição alternativa do valor do ativo vinculado dos metadados `dc:description` no DAM ou da página atual, se nenhum ativo estiver vinculado.
* **Não fornecer um texto alternativo** - Esta opção marca a imagem a ser ignorada por tecnologias assistivas, como leitores de tela, nos casos em que a imagem é meramente decorativa ou não transmite informações adicionais para a página.

>[!NOTE]
>
>Atualmente, os [recursos do Dynamic Media](image.md#dynamic-media) não estão disponíveis no componente de teaser.

### Guia Estilos {#styles-tab-edit}

O Componente de teaser de email é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para este componente na [caixa de diálogo de design](#design-dialog) para que a guia esteja disponível.

## Caixa de diálogo de edição {#edit-dialog}

O Componente de teaser de email delega a renderização da imagem ao [Componente de imagem](image.md). Portanto, a [caixa de diálogo de edição](image.md#edit-dialog) do Componente de imagem está disponível ao autor de conteúdo para manipular a imagem do teaser.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de teaser que o autor do conteúdo terá ao usar esse componente.

### Guia Teaser {#teaser-tab}

![Caixa de diálogo de design do Componente de teaser de email](/help/email/assets/email-teaser-design.png)

* **Elementos de cabeçalho permitidos** - Utilize o menu suspenso para definir quais elementos HTML de cabeçalho podem ser selecionados por um autor para o tipo de título do teaser.
* **Elemento de cabeçalho padrão do título** - O elemento HTML de cabeçalho padrão usado para o tipo de título do teaser
* **Frases de chamariz**
   * **Desabilitar frases de chamariz** - Ocultar a opção **Frases de chamariz** para autores de conteúdo
* **Elementos**
   * **Ocultar pre-título** - Oculta a opção de **Pre-título** para autores de conteúdo
   * **Ocultar título** - Oculta a opção de **Título** para autores de conteúdo
      * Quando selecionado, o **Tipo de Título** fica oculto
   * **Mostrar tipo de título**
   * **Ocultar descrição** - Oculta a opção de **Descrição** para autores de conteúdo
* **Delegar imagem** - Exibição informativa que indica para qual componente o teaser de email delega o tratamento da imagem.

### Guia Estilos {#styles-tab}

O Componente de teaser de email é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.
