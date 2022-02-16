---
title: Componente de Teaser
description: O componente de Teaser pode mostrar uma imagem, um título, um rich text e, opcionalmente, vincular a conteúdo adicional.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: 395a1669cf3e17f649c23852addc37316b923bfd
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 69%

---

# Componente de Teaser {#teaser-component}

O componente de Teaser, do Componentes principais, pode mostrar uma imagem, um título, um rich text e, opcionalmente, um link para conteúdo adicional.

## Uso {#usage}

O componente de Teaser permite que o autor do conteúdo crie facilmente um teaser para conteúdo adicional usando uma imagem, título ou rich text e vinculando a conteúdo adicional ou outras ações.

O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir se as opções para criar frases de chamariz e adicionar links estão disponíveis, bem como desativar várias opções de exibição. O autor do conteúdo pode usar o [a caixa de diálogo de configuração](#configure-dialog) para configurar uma imagem, definir CTAs, definir títulos e descrições e configurar links para o teaser individual. A [caixa de diálogo de edição](image.md#edit-dialog) do [componente de Imagem](image.md) pode ser acessada para modificar a imagem do teaser.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Teaser Component é v2, que foi introduzida com a versão 2.18.0 dos Componentes principais em fevereiro de 2022, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | - | Compatível | Compatível |
| [v1](v1/teaser.md) | Compatível | Compatível | Compatível |

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Teaser, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_teaser_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Teaser [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

O autor do conteúdo pode usar a caixa de diálogo de configuração para definir as propriedades do teaser individual. Também há uma [caixa de diálogo de edição](#edit-dialog) para modificar a imagem do teaser, se essa opção estiver selecionada.

### Links Tab {#links-tab}

![Guia de links de diálogo de edição do componente Teaser](/help/assets/teaser-edit-links.png)

O título, a descrição e a imagem do teaser podem ser herdados da página vinculada ou da página vinculada na primeira chamada à ação. Se não for especificado um link ou uma chamada à ação, o título, a descrição e a imagem serão herdados da página atual.

* **Link** - This file links to a content page, external URL, or page anchor.
* **Abrir link em uma nova guia** - Se estiver habilitado, o link será aberto em uma nova guia do navegador.
* **Chamada para ações** - Essa opção permite vincular a vários destinos.
   * A página vinculada na primeira chamada para a ação é usada ao herdar o título, a descrição ou a imagem do teaser.

### Text Tab {#text-tab}

![Guia Texto da caixa de diálogo de edição do componente de Teaser](/help/assets/teaser-edit-text.png)

* **Pretítulo** - O pretítulo será exibido antes do título do teaser.
* **Título** - Define um título a ser exibido como o título do teaser.
   * **Obter título de página vinculada** - Quando marcado, o título será preenchido com o título da página vinculada.
* **Descrição** - Define uma descrição a ser exibida como o subtítulo do teaser.
   * **Obter descrição de uma página vinculada** - Quando marcada, a descrição será preenchida com a descrição da página vinculada.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Guia Ativo {#asset-tab}

![Guia Imagem da caixa de diálogo de edição do componente de Teaser](/help/assets/teaser-edit-image.png)

* **Herdar imagem em destaque da página** - Use a imagem definida nas propriedades de página da página vinculada ou da página atual, se nenhuma for encontrada.
* **Image asset** - Drop an asset from the [asset browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR) or tap the **browse** option to upload from a local file system.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=pt-BR) no editor de ativos.
* **Texto alternativo para acessibilidade** - Este campo permite que você defina uma descrição da imagem para usuários com deficiências visuais.
   * **Inherit alternative text from page** - This option uses the alternative description of the linked asset value of the `dc:description` metadata in DAM or of the current page if no asset is linked.
* **Don&#39;t provide an alternative text** - This option marks the image to be ignored by assistive technologies like screen readers for cases where the image is purely decorative or otherwise conveys no additional information to the page.

>[!NOTE]
>
>Atualmente, os [recursos do Dynamic Media](image.md#dynamic-media) não estão disponíveis no componente de Teaser.

### Guia Estilos {#styles-tab-edit}

![Styles tab of the edit dialog of Teaser List Component](/help/assets/teaser-edit-styles.png)

O componente Teaser é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling).

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito que as selecionadas na barra de ferramentas do componente.

Styles must be configured for this component in the [design dialog](#design-dialog) in order for the drop down menu to be available.

## Caixa de diálogo de edição {#edit-dialog}

O componente de Teaser delega a renderização da imagem ao [componente de Imagem](image.md). Portanto, a [caixa de diálogo de edição](image.md#edit-dialog do componente de Imagem está disponível ao autor de conteúdo para manipular a imagem do teaser.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de teaser que o autor do conteúdo terá ao usar esse componente.

### Guia Teaser {#teaser-tab}

![Caixa de diálogo de design do componente de Teaser](/help/assets/teaser-design.png)

* **Frases de chamariz**
   * **Desativar Frases de chamariz** - Ocultar a opção **Frases de chamariz** para autores de conteúdo
* **Elementos**
   * **Ocultar pretítulo** - Oculta a opção de **Pretítulo** para autores de conteúdo
   * **Ocultar título** - Oculta a opção de **Título** para autores de conteúdo
      * Quando selecionado, o **Tipo de Título** fica oculto
   * **Ocultar descrição** - Oculta a opção de **Descrição** para autores de conteúdo
* **Tipo de título padrão** - Define a tag H a ser usada pelo título do teaser.
* **Delegação de imagem** - Exibição informativa indicando para qual componente o Teaser delega o manuseio de imagem.

### Guia Estilos {#styles-tab}

O componente de Teaser é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Teaser é compatível com a [Camada de dados de clientes Adobe.](/help/developing/data-layer/overview.md)
