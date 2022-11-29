---
title: Componente Teaser do email
description: O Componente Teaser do email pode mostrar uma imagem, um título, rich text e, opcionalmente, um link para conteúdo adicional.
role: Architect, Developer, Admin, User
exl-id: d6123b22-7cba-406c-986d-b6f00322d135
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 53%

---


# Componente Teaser do email {#email-teaser-component}

O Componente Teaser do email pode mostrar uma imagem, um título, rich text e, opcionalmente, um link para conteúdo adicional.

## Uso {#usage}

O componente Teaser do email permite que o autor do conteúdo crie facilmente um teaser usando uma imagem, um título ou rich text e vinculando a conteúdo adicional ou outras ações.

* O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir se as opções para criar frases de chamariz e adicionar links estão disponíveis, bem como desativar várias opções de exibição.
* O autor do conteúdo pode usar o [a caixa de diálogo de configuração](#configure-dialog) para configurar uma imagem, definir CTAs, definir títulos e descrições e configurar links para o teaser individual.
* O [caixa de diálogo editar](image.md#edit-dialog) do [Componente de imagem de email](image.md) pode ser acessada para modificar a imagem do teaser.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de teaser de email é v1, que foi introduzida com a versão x dos Componentes principais de email em outubro de 2022, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | Compatível |

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente de Teaser do email, bem como ver exemplos de suas opções de configuração, bem como a saída do HTML e JSON, visite o [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_email_teaser)

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de teaser de email [pode ser encontrado no GitHub.](https://adobe.com/go/aem_cmp_tech_email_teaser_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

O autor do conteúdo pode usar a caixa de diálogo de configuração para definir as propriedades do teaser individual. Também há uma [caixa de diálogo de edição](#edit-dialog) para modificar a imagem do teaser, se essa opção estiver selecionada.

### Guia Links {#links-tab}

![Guia de links de diálogo de edição do componente Teaser do email](/help/email/assets/email-teaser-edit-links.png)

O título, a descrição e a imagem do teaser podem ser herdados do conteúdo vinculado ou do conteúdo vinculado na primeira chamada para ação. Se nem um link nem uma chamada para a ação forem especificados, o título, a descrição e a imagem serão herdados do conteúdo atual.

* **Link** - Esse arquivo vincula-se ao conteúdo, URL externo ou âncora.
   * Clique no ícone Campanha para abrir o [Selecionar variável Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Frases de chamariz** - Esta opção permite vincular a vários destinos.
   * A página vinculada na primeira frase de chamariz é usada ao herdar o título, a descrição ou a imagem do teaser.
   * Clique no ícone Campanha para abrir o [Selecionar variável Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.

### Guia Texto {#text-tab}

![Guia de texto da caixa de diálogo de edição do componente Teaser do email](/help/email/assets/email-teaser-edit-text.png)

* **Pre-título** - O pre-título será exibido antes do título do teaser.
* **Título** - Define um título a ser exibido como o título do teaser.
   * Clique no ícone Campanha para abrir o [Selecionar variável Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
   * **Obter título da página vinculada** - Quando marcado, o título será preenchido com o título da página vinculada.
* **Descrição** - Define uma descrição a ser exibida como o subtítulo do teaser.
   * Clique no botão **Selecionar variável Adobe Campaign** ícone para abrir o [Selecionar variável Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
   * **Obter descrição da página vinculada** - Quando marcada, a descrição será preenchida com a descrição da página vinculada.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML.
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração da ID pode afetar o CSS.

### Guia Ativo {#asset-tab}

![Guia Editar imagem da caixa de diálogo do Componente Teaser do email](/help/email/assets/email-teaser-edit-image.png)

* **Herdar imagem em destaque da página** - Use a imagem definida nas propriedades da página vinculada ou da página atual, se nenhuma for encontrada.
* **Ativo de imagem** - Solte um ativo do [navegador de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR) ou toque na opção **procurar** para fazer upload a partir de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique **Editar** para [gerenciar as representações do ativo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=pt-BR) no Editor de ativos.
* **Texto alternativo para acessibilidade** - Este campo permite definir uma descrição da imagem para usuários com deficiências visuais.
   * **Herdar texto alternativo da página** - Esta opção utiliza a descrição alternativa do valor do ativo vinculado dos metadados `dc:description` no DAM ou da página atual, se nenhum ativo estiver vinculado.
* **Não fornecer um texto alternativo** - Esta opção marca a imagem a ser ignorada por tecnologias assistivas, como leitores de tela, nos casos em que a imagem é meramente decorativa ou não transmite informações adicionais para a página.

>[!NOTE]
>
>Atualmente, os [recursos do Dynamic Media](image.md#dynamic-media) não estão disponíveis no componente de teaser.

### Guia Estilos {#styles-tab-edit}

O componente Teaser de email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que a guia esteja disponível.

## Caixa de diálogo de edição {#edit-dialog}

O Componente Teaser de email delega renderização de imagem ao [Componente de imagem](image.md). Portanto, a [caixa de diálogo de edição](image.md#edit-dialog) do Componente de imagem está disponível ao autor de conteúdo para manipular a imagem do teaser.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de teaser que o autor do conteúdo terá ao usar esse componente.

### Guia Teaser {#teaser-tab}

![Caixa de diálogo de design do componente Teaser do email](/help/email/assets/email-teaser-design.png)

* **Elementos de cabeçalho permitidos** - Use o menu suspenso para definir quais elementos de HTML de cabeçalho podem ser selecionados por um autor para o tipo de título do teaser.
* **Elemento de cabeçalho padrão do título** - O elemento HTML de cabeçalho padrão usado para o tipo de título do teaser
* **Frases de chamariz**
   * **Desabilitar frases de chamariz** - Ocultar a opção **Frases de chamariz** para autores de conteúdo
* **Elementos**
   * **Ocultar pre-título** - Oculta a opção de **Pre-título** para autores de conteúdo
   * **Ocultar título** - Oculta a opção de **Título** para autores de conteúdo
      * Quando selecionado, o **Tipo de Título** fica oculto
   * **Mostrar tipo de título**
   * **Ocultar descrição** - Oculta a opção de **Descrição** para autores de conteúdo
* **Delegar imagem** - Exibição informativa indicando para qual componente o Teaser do email delega o manuseio de imagens.

### Guia Estilos {#styles-tab}

O componente Teaser de email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)
