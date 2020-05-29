---
title: Autoria com Componentes principais
description: No AEM, os componentes são os elementos estruturais que constituem o conteúdo das páginas que estão sendo criadas - os componentes principais oferecem uma funcionalidade de criação flexível e repleta de recursos para a oferta.
translation-type: tm+mt
source-git-commit: 4281f6421482682f603f6a7f5e18df61f9a6d98c
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 7%

---


# Autor com componentes principais

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas.

Os componentes principais ofertas funcionalidade de criação flexível e repleta de recursos. O site [de referência](https://wknd.site) WKND e seus exemplos ilustram como os componentes principais podem ser usados para implementar uma experiência avançada no site.

Para experimentar os Componentes principais e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library)componentes.

Para obter uma introdução mais detalhada e orientada ao desenvolvedor para implementar os Componentes principais em um projeto do AEM usando o [AEM Project Archetype](/help/developing/archetype/overview.md) , consulte [o tutorial WKND.](https://docs.adobe.com/content/help/br/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!NOTE]
>
>Os Componentes principais não estão imediatamente disponíveis para os autores, a [equipe de desenvolvimento deve primeiro integrá-los ao seu ambiente](/help/get-started/using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Os componentes principais [exigem o AEM 6.3 ou superior](/help/versions.md) e exigem o uso de modelos [](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)editáveis. Eles não funcionam com a interface clássica nem com modelos estáticos.

## Autoria com Componentes principais {#authoring-with-core-components}

Como autor, você notará várias vantagens dos Componentes principais, incluindo:

* Simple to use and well-integrated with the [page editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)

* Recursos ricos em recursos para acomodar muitos casos de uso, conforme ilustrado pelo site [de referência](https://wknd.site) WKND, bem como na Biblioteca de [componentes](https://adobe.com/go/aem_cmp_library)

* [Pré-configurável](#pre-configuring-core-components) para definir quais recursos estão disponíveis para autores de página por meio do editor de [modelos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

* Built around [accessibility guidelines](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Built to support [responsive layout](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* Criado para suportar localizações [fáceis](localization.md)

Components are available on the **Components** tab of the side panel of the page editor when [editing a page](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html).

Os componentes são agrupados de acordo com as categorias chamadas grupos de componentes para organizar e filtrar facilmente os componentes. O nome do grupo de componentes é exibido com o componente no navegador [do](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) componente e também é possível filtrar por grupo para encontrar facilmente o componente correto.

>[!NOTE]
>
>Os Componentes principais são, por padrão, parte de um grupo oculto e não estão visíveis no navegador de componentes.
>
>Adicione os componentes necessários a um grupo visível ou personalize-os para que fiquem disponíveis para os autores.

## Pré-configuração dos componentes principais {#pre-configuring-core-components}

Configurar componentes básicos era tarefa de um desenvolvedor. Entretanto, com os Componentes principais, um autor de modelo pode configurar vários recursos por meio do editor de modelos.

Por exemplo, se um componente de imagem não permitir o upload de imagem do sistema de arquivos, ou se um componente de texto só permitir determinada formatação de parágrafo, esses recursos poderão ser ativados ou desativados com um simples clique.

Consulte [Criação de modelos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) de página para obter mais informações.

### Editar e projetar caixas de diálogo {#edit-and-design-dialogs}

Como os Componentes principais podem ser pré-configurados pelos autores do modelo para definir quais opções são permitidas como parte de um modelo e, em seguida, configuradas pelo autor da página para definir o conteúdo real da página, cada componente pode ter opções em duas caixas de diálogo diferentes.

|  | Descrição | O que controla | Exemplos |
|--- |--- |--- |--- |
| **Editar caixa de diálogo** | Opções que um autor **de** página pode modificar durante a edição normal de página para os componentes inseridos | O conteúdo exibido pelo componente e como ele aparecerá na página. | Formatação do texto do conteúdo, girar uma imagem em uma página |
| **Caixa de diálogo Design** | Opções que um autor **de** modelo pode modificar ao configurar um modelo de página. | Quais opções o autor da página tem disponíveis ao editar o componente | Quais opções de formatação de texto estão disponíveis, quais opções de imagem no local estão disponíveis |

### Estilo de componente {#component-styling}

Os estilos da maioria dos Componentes principais podem ser definidos usando o sistema de estilo AEM.

* Um autor de modelo pode definir quais estilos estão disponíveis para um componente específico na caixa de diálogo Design desse componente.
* O autor do conteúdo pode escolher quais estilos aplicar ao adicionar o componente e criar o conteúdo.

Para obter mais detalhes, consulte a documentação do Sistema [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html) estilo.

>[!NOTE]
>
>No AEM 6.3, o Service Pack 2 (6.3.2.0) ou mais recente é necessário para ativar o recurso de estilo do sistema.

## Recursos do desenvolvedor {#developer-resources}

Consulte a documentação do desenvolvedor [Desenvolvendo componentes](/help/developing/overview.md) principais para obter informações técnicas sobre os componentes principais.
