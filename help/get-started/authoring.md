---
title: Autoria com Componentes principais
description: Em AEM, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas - os Componentes principais oferecem funcionalidade de criação flexível e repleta de recursos.
role: Architect, Developer, Admin, User
exl-id: 56e58303-a178-45ab-b59d-e374c9cf90cf
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 8%

---

# Autor com componentes principais

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas.

Os Componentes principais oferecem funcionalidade de criação flexível e repleta de recursos. O [site de referência WKND](https://wknd.site) e seu relatório ilustram como os componentes principais podem ser usados para implementar uma experiência rica em sites.

Para experimentar os Componentes principais e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library).

Para obter uma introdução mais detalhada e orientada pelo desenvolvedor à implementação dos Componentes principais em um projeto AEM usando o [AEM Arquétipo de projeto](/help/developing/archetype/overview.md) confira [o tutorial WKND.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!NOTE]
>
>Os Componentes principais não estão imediatamente disponíveis para os autores, a [equipe de desenvolvimento deve primeiro integrá-los ao seu ambiente](/help/get-started/using.md). Uma vez integrados, eles podem ser disponibilizados e pré-configurados por meio do [editor de modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Os Componentes principais [exigem AEM 6.4 ou superior](/help/versions.md) e exigem o uso de [modelos editáveis](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html). Eles não funcionam com a interface do usuário clássica nem com modelos estáticos.

## Autoria com Componentes principais {#authoring-with-core-components}

Como autor, você notará várias vantagens dos Componentes principais, incluindo:

* Simples de usar e bem integrado com o [editor de página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)

* Recursos repletos de recursos para acomodar muitos casos de uso, conforme ilustrado pelo [site de referência WKND](https://wknd.site), bem como na [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library)

* [Pré-](#pre-configuring-core-components) configuráveis para definir quais recursos estão disponíveis para os autores de página por meio do editor de  [modelos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

* Construído em torno de [diretrizes de acessibilidade](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Criado para suportar [layout responsivo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* Criado para suportar [localização fácil](localization.md)

Os componentes estão disponíveis na guia **Components** do painel lateral do editor de páginas ao [editar uma página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html).

Os componentes são agrupados de acordo com categorias chamadas grupos de componentes para organizar e filtrar facilmente os componentes. O nome do grupo de componentes é exibido com o componente no [navegador de componentes](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) e também é possível filtrar por grupo para localizar facilmente o componente correto.

>[!NOTE]
>
>Os Componentes principais são, por padrão, parte de um grupo oculto e não ficam visíveis no navegador de componentes.
>
>Adicione os componentes necessários a um grupo visível ou personalize-os para que fiquem disponíveis para autores.

## Pré-configuração dos componentes principais {#pre-configuring-core-components}

Configurar componentes básicos era trabalho de um desenvolvedor. No entanto, com os Componentes principais, um autor de modelo agora pode configurar vários recursos por meio do editor de modelo.

Por exemplo, se um componente de imagem não deve permitir o upload de imagem do sistema de arquivos ou se um componente de texto deve permitir apenas determinadas formatações de parágrafo, esses recursos podem ser ativados ou desativados com um simples clique.

Consulte [Criação de modelos de página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) para obter mais informações.

### Caixas de diálogo Editar e Design {#edit-and-design-dialogs}

Como os Componentes principais podem ser pré-configurados pelos autores de modelo para definir quais opções são permitidas como parte de um modelo e, em seguida, configuradas pelo autor da página para definir o conteúdo real da página, cada componente pode ter opções em duas caixas de diálogo diferentes.

|  | Descrição | O que ele controla | Exemplos |
|--- |--- |--- |--- |
| **Editar caixa de diálogo** | Opções que um **autor da página** pode modificar durante a edição normal da página para os componentes colocados | O conteúdo exibido pelo componente e como ele aparecerá na página. | Formatação do texto do conteúdo, girar uma imagem em uma página |
| **Caixa de diálogo Design** | Opções que um **autor do modelo** pode modificar ao configurar um modelo de página. | Quais opções o autor da página tem disponíveis ao editar o componente | Quais opções de formatação de texto estão disponíveis, quais opções de imagem no local estão disponíveis |

### Estilo do componente {#component-styling}

Os estilos da maioria dos Componentes principais podem ser definidos usando o sistema de estilo AEM.

* Um autor de modelo pode definir quais estilos estão disponíveis para um componente específico na caixa de diálogo Design desse componente.
* O autor de conteúdo pode então escolher quais estilos aplicar ao adicionar o componente e criar o conteúdo.

Para obter mais detalhes, consulte a documentação do [Style System](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html).

## Recursos do desenvolvedor {#developer-resources}

Consulte a documentação do desenvolvedor [Desenvolvimento de componentes principais](/help/developing/overview.md) para obter informações técnicas sobre os componentes principais.
