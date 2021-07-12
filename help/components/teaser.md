---
title: Componente Teaser
description: O componente de teaser pode mostrar uma imagem, um título, rich text e, opcionalmente, vincular a conteúdo adicional.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 2%

---

# Componente Teaser {#teaser-component}

O Componente Teaser do componente principal pode mostrar uma imagem, um título, rich text e, opcionalmente, um link para conteúdo adicional.

## Uso {#usage}

O componente Teaser permite que o autor do conteúdo crie facilmente um teaser para conteúdo adicional usando uma imagem, título ou rich text e vinculando a conteúdo adicional ou outras ações.

O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir se as opções para criar chamadas para ações e adicionar links estão disponíveis, bem como desativar várias opções de exibição. O autor de conteúdo pode usar o [configurar a caixa de diálogo](#configure-dialog) para definir uma imagem, definir CTAs, definir títulos e descrições e configurar links para o teaser individual. O [edit dialog](image.md#edit-dialog) do [Image Component](image.md) pode ser acessado para modificar a imagem do teaser.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Teaser Component é v1, que foi introduzida com a versão 2.1.0 dos Componentes principais em julho de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | Compatível | Compatível |

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Teaser Component, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Component Library](https://adobe.com/go/aem_cmp_library_teaser).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Teaser Component [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

O autor de conteúdo pode usar a caixa de diálogo de configuração para definir as propriedades do teaser individual. Também há um [editar diálogo](#edit-dialog) para modificar a imagem do teaser, se essa opção estiver selecionada.

### Imagem {#image}

![Guia Editar imagem da caixa de diálogo do Componente de Teaser](/help/assets/teaser-edit-image.png)

* **Ativos da imagem**
   * Solte um ativo do [navegador de ativos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) ou toque na opção **browse** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) no editor de ativos.

>[!NOTE]
>
>[No momento, ](image.md#dynamic-media) os recursos do Dynamic Media não estão disponíveis no Teaser Component.

### Texto {#text}

![Guia de texto da caixa de diálogo de edição do Componente de Teaser](/help/assets/teaser-edit-text.png)

* **Pretitle**  - O pretítulo será exibido antes do título do teaser.
* **Título**  - Define um título a ser exibido como título para o teaser.
   * **Obter título de página vinculada**  - Quando marcado, o título será preenchido com o título da página vinculada.
* **Descrição**  - Define uma descrição para ser exibida como o subtítulo do teaser.
   * **Obter descrição de uma página vinculada**  - Quando marcada, a descrição será preenchida com a descrição da página vinculada.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

### Links e ações {#links-actions}

![Guia do link de edição do componente Teaser](/help/assets/teaser-edit-link.png)

* **Link**  - Link aplicado ao teaser. Use o navegador de caminho para selecionar o destino do link.
* **Habilitar ações de chamada para**  - quando marcado, habilita a definição de Ações de chamada para ação. O primeiro link de Chamada para Ação na lista é usado como o link para outros elementos de teaser.

## Editar caixa de diálogo {#edit-dialog}

O Teaser Component delega a renderização da imagem ao [Image Component](image.md). Portanto, a caixa de diálogo [edit](image.md#edit-dialog do Componente de imagem está disponível para o autor de conteúdo para manipular a imagem do teaser.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de teaser que o autor de conteúdo tem ao usar esse componente.

### Guia Teaser {#teaser-tab}

![Caixa de diálogo de design do componente Teaser](/help/assets/teaser-design.png)

* **Frases de chamariz**
   * **Desativar as ações de chamada**  - Ocultar a opção  **de ações de chamada para** autores de conteúdo
* **Elementos**
   * **Ocultar pretítulo**  - Oculta a opção  **** Predefinido para autores de conteúdo
   * **Ocultar título**  - Oculta a opção  **** Título para autores de conteúdo
      * Quando selecionado, o **Tipo de Título** fica oculto
   * **Ocultar descrição**  - Ocultar a opção de  **** Descrição para autores de conteúdo
* **Tipo de título**  - Define a tag H a ser usada pelo título do teaser.
* **Links**
   * **Não vincular a imagem**  - Quando selecionada, a imagem do teaser não é vinculada
   * **Não vincular o título**  - Quando selecionado, o título do teaser não é vinculado
* **Delegar imagem**  - Exibição informativa indicando para qual componente o Teaser delega o manuseio de imagem.

### Guia Estilos {#styles-tab}

O Teaser Component suporta o AEM [Style System](/help/get-started/authoring.md#component-styling).

## Camada de dados do cliente Adobe {#data-layer}

O componente Teaser suporta a [Camada de Dados do Cliente Adobe.](/help/developing/data-layer/overview.md)
