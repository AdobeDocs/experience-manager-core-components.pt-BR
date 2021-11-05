---
title: Autoria com Componentes principais
description: No AEM, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas - os Componentes principais oferecem funcionalidade de criação flexível e repleta de recursos.
role: Architect, Developer, Admin, User
exl-id: 56e58303-a178-45ab-b59d-e374c9cf90cf
source-git-commit: 888719359f9a1d1c9dccff97fb639b332f2be54c
workflow-type: ht
source-wordcount: '742'
ht-degree: 100%

---

# Crie com Componentes principais

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas.

Os Componentes principais oferecem funcionalidade de criação flexível e repleta de recursos. O [site de referência da WKND](https://wknd.site) e seus componentes ilustram como os componentes principais podem ser usados para implementar uma experiência rica em sites.

Para experimentar os Componentes principais, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_br).

Para uma introdução mais detalhada e orientada pelo desenvolvedor à implementação dos Componentes principais em um projeto AEM usando o [Arquétipo de projeto do AEM](/help/developing/archetype/overview.md), confira [o tutorial do WKND](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=pt-BR).

>[!NOTE]
>
>Os Componentes principais não estão imediatamente disponíveis para os autores, a [equipe de desenvolvimento deve primeiro integrá-los ao seu ambiente](/help/get-started/using.md). Uma vez integrados, eles podem ser disponibilizados e pré-configurados pelo [editor de modelos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR).

>[!CAUTION]
>
>Os Componentes principais [exigem o AEM 6.4 ou superior](/help/versions.md) e o uso de [modelos editáveis](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR). Eles não funcionam com a IU Clássica nem com modelos estáticos.

## Autoria com Componentes principais {#authoring-with-core-components}

Como autor, você perceberá várias vantagens dos Componentes principais, entre elas:

* Simples de usar e bem integrado ao [editor de páginas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR)

* Funcionalidades repletas de recursos para acomodar muitos casos de uso, conforme ilustrado pelo [site de referência da WKND](https://wknd.site) e na [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_br)

* [Pré-configurável](#pre-configuring-core-components) para definir quais recursos estão disponíveis para os autores de página por meio do [editor de modelos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR)

* Construídos em torno de [diretrizes de acessibilidade](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=pt-BR)

* Criados para serem compatíveis com [layout responsivo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html?lang=pt-BR)

* Criados para serem compatíveis com [localização fácil](localization.md)

Os componentes estão disponíveis na guia **Componentes** do painel lateral do editor de páginas ao [editar uma página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR).

Os componentes são agrupados de acordo com categorias chamadas grupos de componentes para organizá-los e filtrá-los com facilidade. O nome do grupo de componentes é exibido com o componente no [navegador de componentes](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR). Também é possível filtrar por grupo para localizá-lo fácil e corretamente.

>[!NOTE]
>
>Os Componentes principais são, por padrão, parte de um grupo oculto e não ficam visíveis no navegador de componentes.
>
>Adicione os componentes necessários a um grupo visível ou personalize-os para que fiquem disponíveis a autores.

## Pré-configuração dos Componentes principais {#pre-configuring-core-components}

Configurar Componentes de base era trabalho de um desenvolvedor. No entanto, com os Componentes principais, um autor de modelo agora pode configurar vários recursos por meio do editor de modelo.

Por exemplo, se um componente de Imagem não deve permitir o upload de imagem do sistema de arquivos ou se um componente de Texto deve permitir apenas determinadas formatações de parágrafo, esses recursos podem ser ativados ou desativados com um simples clique.

Consulte [Criação de modelos de página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR) para obter informações.

### Caixas de diálogo de edição e design {#edit-and-design-dialogs}

Os Componentes principais podem ser pré-configurados pelos autores de modelo para definir quais opções são permitidas como parte de um modelo. Em seguida, podem ser configurados pelo autor da página para definir o conteúdo real da página. Por isso, cada componente pode ter opções em duas caixas de diálogo diferentes.

|  | Descrição | O que ele controla | Exemplos |
|--- |--- |--- |--- |
| **Caixa de diálogo de edição** | Opções que um **autor da página** pode modificar durante a edição normal da página para os componentes colocados. | O conteúdo exibido pelo componente e como ele aparecerá na página. | Formatação do texto do conteúdo, rotação de uma imagem em uma página |
| **Caixa de diálogo de design** | Opções que um **autor do modelo** pode modificar ao configurar um modelo de página. | Quais opções o autor da página tem disponíveis ao editar o componente. | Quais opções de formatação de texto estão disponíveis, quais opções de imagem no local estão disponíveis |

### Aplicação de estilos aos componentes {#component-styling}

Os estilos da maioria dos Componentes principais podem ser definidos usando o Sistema de Estilos do AEM.

* Um autor de modelo pode definir quais estilos estão disponíveis para um componente específico na caixa de diálogo de design desse componente.
* O autor de conteúdo pode depois escolher quais estilos aplicar ao adicionar o componente e criar o conteúdo.

Para mais detalhes, consulte a documentação do [Sistema de Estilos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/style-system.html?lang=pt-BR).

## Recursos do desenvolvedor {#developer-resources}

Consulte a documentação do desenvolvedor [Desenvolvimento de Componentes principais](/help/developing/overview.md) para obter informações técnicas sobre os Componentes principais.
