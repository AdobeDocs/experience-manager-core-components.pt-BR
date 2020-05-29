---
title: Componente Teaser
description: O componente do teaser pode mostrar uma imagem, um título, rich text e, opcionalmente, vincular para conteúdo adicional.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 2%

---


# Componente Teaser {#teaser-component}

O Componente principal do teaser do componente pode mostrar uma imagem, um título, rich text e, opcionalmente, um link para conteúdo adicional.

## Uso {#usage}

O componente Teaser permite que o autor do conteúdo crie facilmente um teaser para obter mais conteúdo usando uma imagem, um título ou texto formatado e vinculando a conteúdo adicional ou outras ações.

O autor do modelo pode usar a caixa de diálogo [de](#design-dialog) design para definir se as opções para criar chamadas para ações e adicionar links estão disponíveis, além de desativar várias opções de exibição. O autor do conteúdo pode usar a caixa de diálogo [de](#configure-dialog) configuração para definir uma imagem, definir CTAs, definir títulos e descrições e configurar links para o teaser individual. A caixa de diálogo [de](image.md#edit-dialog) edição do Componente [de](image.md) imagem pode ser acessada para modificar a imagem do teaser.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Teaser Component é v1, que foi introduzida com a versão 2.1.0 dos Componentes Principais em julho de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | Compatível | Compatível |

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o componente Teaser e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_teaser)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Teaser [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

O autor do conteúdo pode usar a caixa de diálogo de configuração para definir as propriedades do teaser individual. Também há uma caixa de diálogo [de](#edit-dialog) edição para modificar a imagem do teaser, se ela estiver selecionada.

### Imagem {#image}

![Guia de imagem da caixa de diálogo de edição do Componente Teaser](/help/assets/teaser-edit-image.png)

* **Ativos da imagem**
   * Solte um ativo do navegador [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) ativos ou toque na opção de **navegação** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) no editor de ativos.

### Texto {#text}

![Guia de texto da caixa de diálogo de edição do Componente Teaser](/help/assets/teaser-edit-text.png)

* **Pretitle** - O pretitle será exibido antes do título do teaser.
* **Título** - Define um título a ser exibido como o título do teaser.
   * **Obter título da página** vinculada - Quando marcado, o título será preenchido com o título da página vinculada.
* **Descrição** - Define uma descrição para ser exibida como o subtítulo do teaser.
   * **Obter descrição da página** vinculada - Quando marcada, a descrição será preenchida com a descrição da página vinculada.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

### Links e ações {#links-actions}

![Guia do link de edição do componente Teaser](/help/assets/teaser-edit-link.png)

* **Link** - Link aplicado ao teaser. Use o navegador de caminho para selecionar o público alvo do link.
* **Ativar ações** de chamada - quando marcada, ativa a definição de Ações de chamada. O primeiro link de Chamada para Ação na lista é usado como link para outros elementos do teaser.

## Edit Dialog {#edit-dialog}

O componente Teaser delega a renderização de imagem ao componente [de](image.md)imagem. Portanto, a caixa de diálogo [de]edição (image.md#edit-dialog) do Componente de imagem está disponível para o autor do conteúdo para manipular a imagem do teaser.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções do teaser que o autor do conteúdo possui ao usar esse componente.

### Guia Teaser {#teaser-tab}

![Caixa de diálogo de design do componente Teaser](/help/assets/teaser-design.png)

* **Frases de chamariz**
   * **Desabilitar ações** de chamada - Ocultar a opção **Chamada para ações** para autores de conteúdo
* **Elementos**
   * **Ocultar pretítulo** - Oculta a opção **Pretítulo** para autores de conteúdo
   * **Ocultar título** - Oculta a opção **Título** para autores de conteúdo
      * Quando selecionado, o Tipo **de** Título fica oculto
   * **Ocultar descrição** - Ocultar a opção **Descrição** para autores de conteúdo
* **Tipo** de título - Define a tag H a ser usada pelo título do teaser.
* **Links**
   * **Não vincular a imagem** - quando selecionada, a imagem do teaser não está vinculada
   * **Não vincular o título** - Quando selecionado, o título do teaser não está vinculado
* **Delegar** imagem - exibição informativa indicando para qual componente o Teaser delega o gerenciamento de imagens.

### Guia Estilos {#styles-tab}

O componente Teaser suporta o sistema [AEM](/help/get-started/authoring.md#component-styling)Style.
