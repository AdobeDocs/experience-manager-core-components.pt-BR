---
title: Autoria com Componentes principais
description: No AEM, os componentes são os elementos estruturais que constituem o conteúdo das páginas que estão sendo criadas - Componentes principais, funcionalidade de criação flexível e repleta de recursos.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 7%

---


# Autor com componentes principais

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas.

Os componentes principais ofertas funcionalidade de criação flexível e repleta de recursos. O [site de referência WKND](https://wknd.site) e seus ilustra como os componentes principais podem ser usados para implementar uma experiência avançada no site.

Para experimentar os Componentes principais e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library).

Para obter uma introdução mais detalhada e orientada ao desenvolvedor para implementar os Componentes Principais em um projeto AEM usando o [AEM Project Archetype](/help/developing/archetype/overview.md) dê uma olhada [no tutorial WKND.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!NOTE]
>
>Os Componentes principais não estão imediatamente disponíveis para os autores, a [equipe de desenvolvimento deve primeiro integrá-los ao seu ambiente](/help/get-started/using.md). Uma vez integrados, eles podem ser disponibilizados e pré-configurados por meio do [editor de modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Os componentes principais [exigem AEM 6.4 ou superior](/help/versions.md) e exigem o uso de [modelos editáveis](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html). Eles não funcionam com a interface clássica nem com modelos estáticos.

## Autoria com Componentes principais {#authoring-with-core-components}

Como autor, você notará várias vantagens dos Componentes principais, incluindo:

* Simples de usar e bem integrado com o [editor de página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)

* Recursos ricos em recursos para acomodar muitos casos de uso, conforme ilustrado pelo [site de referência WKND](https://wknd.site), bem como na [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library)

* [Pré-](#pre-configuring-core-components) configurável para definir quais recursos estão disponíveis para autores de página por meio do editor de  [modelos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

* Construído em torno de [diretrizes de acessibilidade](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Criado para suportar [layout responsivo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* Criado para suportar [localização fácil](localization.md)

Os componentes estão disponíveis na guia **Components** do painel lateral do editor de página quando [editar uma página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html).

Os componentes são agrupados de acordo com as categorias chamadas grupos de componentes para organizar e filtrar facilmente os componentes. O nome do grupo de componentes é exibido com o componente no [navegador de componentes](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) e também é possível filtrar por grupo para encontrar facilmente o componente correto.

>[!NOTE]
>
>Os Componentes principais são, por padrão, parte de um grupo oculto e não estão visíveis no navegador de componentes.
>
>Adicione os componentes necessários a um grupo visível ou personalize-os para que fiquem disponíveis para os autores.

## Pré-configuração dos componentes principais {#pre-configuring-core-components}

Configurar componentes básicos era tarefa de um desenvolvedor. Entretanto, com os Componentes principais, um autor de modelo pode configurar vários recursos por meio do editor de modelos.

Por exemplo, se um componente de imagem não permitir o upload de imagem do sistema de arquivos, ou se um componente de texto só permitir determinada formatação de parágrafo, esses recursos poderão ser ativados ou desativados com um simples clique.

Consulte [Criação de modelos de página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) para obter mais informações.

### Editar e criar caixas de diálogo {#edit-and-design-dialogs}

Como os Componentes principais podem ser pré-configurados pelos autores do modelo para definir quais opções são permitidas como parte de um modelo e, em seguida, configuradas pelo autor da página para definir o conteúdo real da página, cada componente pode ter opções em duas caixas de diálogo diferentes.

|  | Descrição | O que controla | Exemplos |
|--- |--- |--- |--- |
| **Editar caixa de diálogo** | Opções que um **autor de página** pode modificar durante a edição normal de página para os componentes colocados | O conteúdo exibido pelo componente e como ele aparecerá na página. | Formatação do texto do conteúdo, girar uma imagem em uma página |
| **Caixa de diálogo Design** | Opções que um **autor de modelo** pode modificar ao configurar um modelo de página. | Quais opções o autor da página tem disponíveis ao editar o componente | Quais opções de formatação de texto estão disponíveis, quais opções de imagem no local estão disponíveis |

### Estilo de componente {#component-styling}

Os estilos da maioria dos Componentes principais podem ser definidos usando o sistema de estilo AEM.

* Um autor de modelo pode definir quais estilos estão disponíveis para um componente específico na caixa de diálogo Design desse componente.
* O autor do conteúdo pode escolher quais estilos aplicar ao adicionar o componente e criar o conteúdo.

Para obter mais detalhes, consulte a documentação [Sistema de estilo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html).

## Recursos do desenvolvedor {#developer-resources}

Consulte a documentação do desenvolvedor [Developing Core Components](/help/developing/overview.md) para obter informações técnicas sobre os componentes principais.
