---
title: Componente de teaser (v1)
description: O componente de Teaser pode mostrar uma imagem, um título, um rich text e, opcionalmente, vincular a conteúdo adicional.
role: Architect, Developer, Admin, User
source-git-commit: f8aa86d58ba71ede3c3cd867c45aafff06923325
workflow-type: ht
source-wordcount: '748'
ht-degree: 100%

---


# Componente de Teaser (v1) {#teaser-component}

O componente de Teaser, do Componentes principais, pode mostrar uma imagem, um título, um rich text e, opcionalmente, um link para conteúdo adicional.

## Uso {#usage}

O componente de Teaser permite que o autor do conteúdo crie facilmente um teaser para conteúdo adicional usando uma imagem, título ou rich text e vinculando a conteúdo adicional ou outras ações.

O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir se as opções para criar frases de chamariz e adicionar links estão disponíveis, bem como desativar várias opções de exibição. O autor do conteúdo pode usar o [a caixa de diálogo de configuração](#configure-dialog) para configurar uma imagem, definir CTAs, definir títulos e descrições e configurar links para o teaser individual. A [caixa de diálogo de edição](image-v1.md#edit-dialog) do [componente de Imagem](image-v1.md) pode ser acessada para modificar a imagem do teaser.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a versão v1 do componente de teaser, que foi introduzida com a versão 2.1.0 dos componentes principais em julho de 2018.

>[!CAUTION]
>
>Este documento descreve a versão v1 do componente de teaser.
>
>Para obter detalhes sobre a versão atual do componente de teaser, consulte o documento [Componente de teaser](/help/components/teaser.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Teaser, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_teaser_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Teaser [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

O autor do conteúdo pode usar a caixa de diálogo de configuração para definir as propriedades do teaser individual. Também há uma [caixa de diálogo de edição](#edit-dialog) para modificar a imagem do teaser, se essa opção estiver selecionada.

### Imagem {#image}

![Guia Imagem da caixa de diálogo de edição do componente de Teaser](/help/assets/teaser-edit-image.png)

* **Ativos da imagem**
   * Solte um ativo do [navegador de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR) ou toque na opção **pesquisar** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=pt-BR) no editor de ativos.

>[!NOTE]
>
>Atualmente, os [recursos do Dynamic Media](image-v1.md#dynamic-media) não estão disponíveis no componente de Teaser.

### Texto {#text}

![Guia Texto da caixa de diálogo de edição do componente de Teaser](/help/assets/teaser-edit-text.png)

* **Pre-título** - O pre-título será exibido antes do título do teaser.
* **Título** - Define um título a ser exibido como o título do teaser.
   * **Obter título da página vinculada** - Quando marcado, o título será preenchido com o título da página vinculada.
* **Descrição** - Define uma descrição a ser exibida como o subtítulo do teaser.
   * **Obter descrição da página vinculada** - Quando marcada, a descrição será preenchida com a descrição da página vinculada.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Links e ações {#links-actions}

![Guia Link da caixa de diálogo de edição do componente de Teaser](/help/assets/teaser-edit-link.png)

* **Link** - Link aplicado ao teaser. Use o navegador de caminho para selecionar o destino do link.
* **Habilitar Frases de chamariz** - Quando marcado, habilita a definição de Frases de chamariz. O primeiro link de Chamada para Ação na lista é usado como o link para outros elementos de teaser.

## Caixa de diálogo de edição {#edit-dialog}

O componente de Teaser delega a renderização da imagem ao [componente de Imagem](image-v1.md). Portanto, a [caixa de diálogo de edição](image.md#edit-dialog) do componente de imagem está disponível ao autor de conteúdo para manipular a imagem do teaser.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de teaser que o autor do conteúdo terá ao usar esse componente.

### Guia Teaser {#teaser-tab}

![Caixa de diálogo de design do componente de Teaser](/help/assets/teaser-design.png)

* **Frases de chamariz**
   * **Desabilitar frases de chamariz** - Ocultar a opção **Frases de chamariz** para autores de conteúdo
* **Elementos**
   * **Ocultar pre-título** - Oculta a opção de **Pre-título** para autores de conteúdo
   * **Ocultar título** - Oculta a opção de **Título** para autores de conteúdo
      * Quando selecionado, o **Tipo de Título** fica oculto
   * **Ocultar descrição** - Oculta a opção de **Descrição** para autores de conteúdo
* **Tipo de título** - Define a tag H a ser usada pelo título do teaser.
* **Links**
   * **Não vincular a imagem** - Quando selecionada, a imagem do teaser não é vinculada
   * **Não vincular o título** - Quando selecionado, o título do teaser não é vinculado
* **Delegar imagem** - Exibição informativa indicando para qual componente o Teaser delega o manuseio de imagem.

### Guia Estilos {#styles-tab}

O componente de Teaser é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Teaser é compatível com a [Camada de dados de clientes Adobe.](/help/developing/data-layer/overview.md)
