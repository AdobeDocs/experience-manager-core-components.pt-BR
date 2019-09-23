---
title: Criação com componentes principais
seo-title: Criação com componentes principais
description: No AEM, os componentes são os elementos estruturais que constituem o conteúdo das páginas que estão sendo criadas - os Componentes principais oferecem funcionalidade de criação flexível e repleta de recursos.
seo-description: No AEM, os componentes são os elementos estruturais que constituem o conteúdo das páginas que estão sendo criadas - os Componentes principais oferecem funcionalidade de criação flexível e repleta de recursos.
uuid: 4a54cd4c-3d89-4683-8301-bf1e634736e3
content-type: referência
topic-tags: autoria
discoiquuid: 8751e490-d427-44f2-b767-51935afda988
translation-type: tm+mt
source-git-commit: b6fbef1cff2908533df6573cd3a92266857ba93f

---


# Autor com componentes principais

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas.

Os Componentes principais oferecem funcionalidade de criação flexível e repleta de recursos. The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) illustrates how the core components can be used.

Para experimentar os Componentes principais e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html)componentes.

Para obter uma introdução mais detalhada e orientada ao desenvolvedor para implementar os componentes principais em um projeto AEM, consulte [o tutorial da WKND.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html).

>[!CAUTION]
>
>Os componentes principais [exigem o AEM 6.3 ou superior](versions.md) e exigem o uso de modelos [](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)editáveis. Eles não funcionam com a interface clássica nem com modelos estáticos.

## Criação com componentes principais {#authoring-with-core-components}

Como autor, você notará várias vantagens dos Componentes principais, incluindo:

* Simple to use and well-integrated with the [page editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)

* Recursos ricos em recursos para acomodar muitos casos de uso, conforme [ilustrado em We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) , bem como na Biblioteca de [componentes](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html)

* [Pré-configurável](#pre-configuring-core-components) para definir quais recursos estão disponíveis para autores de página por meio do editor de [modelos](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

* Built around [accessibility guidelines](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

* Built to support [responsive layout](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)

* Criado para suportar a localização [fácil](localization.md)

Components are available on the **Components** tab of the side panel of the page editor when [editing a page](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html).

Os componentes são agrupados de acordo com categorias chamadas grupos de componentes para organizar e filtrar facilmente os componentes. O nome do grupo de componentes é exibido com o componente no navegador [do](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) componente e também é possível filtrar por grupo para encontrar facilmente o componente correto.

>[!NOTE]
>
>Os Componentes principais são, por padrão, parte de um grupo oculto e não estão visíveis no navegador de componentes.
>
>Adicione os componentes necessários a um grupo visível ou personalize-os para que fiquem disponíveis para os autores.

## Pré-configuração dos componentes principais {#pre-configuring-core-components}

Configurar componentes básicos era tarefa de um desenvolvedor. Entretanto, com os Componentes principais, um autor de modelo pode configurar vários recursos por meio do editor de modelos.

Por exemplo, se um componente de imagem não permitir o upload de imagem do sistema de arquivos, ou se um componente de texto só permitir determinada formatação de parágrafo, esses recursos poderão ser ativados ou desativados com um simples clique.

Consulte [Criação de modelos](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) de página para obter mais informações.

### Editar e criar caixas de diálogo {#edit-and-design-dialogs}

Como os Componentes principais podem ser pré-configurados pelos autores do modelo para definir quais opções são permitidas como parte de um modelo e, em seguida, configuradas pelo autor da página para definir o conteúdo real da página, cada componente pode ter opções em duas caixas de diálogo diferentes.

|  | Descrição | O que controla | Exemplos |
|--- |--- |--- |--- |
| **Editar caixa de diálogo** | Opções que um autor **de** página pode modificar durante a edição normal de página dos componentes inseridos | O conteúdo exibido pelo componente e como ele será exibido na página. | Formatação do texto do conteúdo, girar uma imagem em uma página |
| **Caixa de diálogo Design** | Opções que um autor **de** modelo pode modificar ao configurar um modelo de página. | Quais opções o autor da página tem disponíveis ao editar o componente | Quais opções de formatação de texto estão disponíveis, quais opções de imagem no local estão disponíveis |

### Estilo de componente {#component-styling}

Os estilos da maioria dos Componentes principais podem ser definidos usando o sistema de estilo AEM.

* Um autor de modelo pode definir quais estilos estão disponíveis para um componente específico na caixa de diálogo Design desse componente.
* O autor do conteúdo pode escolher quais estilos aplicar ao adicionar o componente e criar o conteúdo.

Para obter mais detalhes, consulte a documentação do Sistema [de](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) estilo.

>[!NOTE]
>
>No AEM 6.3, o Service Pack 2 (6.3.2.0) ou mais recente é necessário para ativar o recurso de estilo do sistema.

## Lista de componentes principais disponíveis {#list-of-core-components-available}

A seguir está uma lista dos Componentes principais disponíveis vinculados às páginas que descrevem detalhadamente seus recursos de diálogo de edição e design.

A versão atual dos Componentes principais apresenta os seguintes componentes.

* [Expandir/recolher](accordion.md)
* [Caminho](breadcrumb.md)
* [Imagem](button.md)
* [Container](container.md)
* [Carrossel](carousel.md)
* [Fragmento do conteúdo](content-fragment-component.md)
* [Lista de fragmentos de conteúdo](content-fragment-list.md)
* [Download](download.md)
* [Fragmento de experiência](experience-fragment.md)
* [Botão de formulário](form-button.md)
* [Contêineres de formulário](form-container.md)
* [Formulário oculto](form-hidden.md)
* [Opções de formulário](form-options.md)
* [Texto do formulário](form-text.md)
* [Imagem](image.md)
* [Navegação de idiomas](language-navigation.md)
* [Lista](list.md)
* [Navegação](navigation.md)
* [Modos](page.md)
* [Pesquisa rápida](quick-search.md)
* [Separador](separator.md)
* [Compartilhamento em rede social](sharing.md)
* [Guias](tabs.md)
* [Text](text.md)
* [Título](title.md)

>[!CAUTION]
>
>Algumas versões dos componentes principais individuais podem ser compatíveis apenas com determinadas versões do AEM.
>
>Consulte a página de ajuda individual (vinculada na lista anterior) do componente específico para obter informações sobre compatibilidade ou consulte o documento Versões [dos componentes](versions.md) principais para obter mais informações.

>[!NOTE]
>
>Dependendo do seu caso, você pode ter componentes personalizados desenvolvidos explicitamente para as suas necessidades. Eles podem até ter o mesmo nome que alguns dos componentes discutidos aqui.
>Os componentes principais do formulário não estão relacionados ao AEM Forms.

## Recursos do desenvolvedor {#developer-resources}

Consulte a documentação do desenvolvedor [Desenvolvendo componentes](developing.md) principais para obter informações técnicas sobre os componentes principais.
