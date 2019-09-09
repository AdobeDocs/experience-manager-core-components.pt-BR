---
title: Criação com componentes principais
seo-title: Criação com componentes principais
description: No AEM, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas - Os Componentes principais oferecem funcionalidade de criação flexível e repleta de funções.
seo-description: No AEM, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas - Os Componentes principais oferecem funcionalidade de criação flexível e repleta de funções.
uuid: 4 a 54 cd 4 c -3 d 89-4683-8301-bf 1 e 634736 e 3
content-type: referência
topic-tags: criação
discoiquuid: 8751 e 490-d 427-44 f 2-b 767-51935 afda 988
translation-type: tm+mt
source-git-commit: b6fbef1cff2908533df6573cd3a92266857ba93f

---


# Autor com componentes principais

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas.

Os Componentes principais oferecem funcionalidade de criação flexível e repleta de funções. The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) illustrates how the core components can be used.

Para experimentar os Componentes principais e ver exemplos de suas opções de configuração, bem como de HTML e saída JSON, visite a Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html).

Para obter uma introdução mais detalhada e orientada pelo desenvolvedor, a implementação dos Componentes principais em um projeto do AEM verifica [o tutorial WKND.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html).

>[!CAUTION]
>
>Os Componentes [principais exigem o AEM 6.3 ou superior](versions.md) e exigem o uso de [modelos editáveis](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html). Eles não funcionam com a interface de usuário clássica nem com modelos estáticos.

## Criação com componentes principais {#authoring-with-core-components}

Como autor, você perceberá várias vantagens dos Componentes principais, incluindo:

* Simple to use and well-integrated with the [page editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)

* Recursos repletos de funções para acomodar muitos casos de uso, conforme [ilustrado em We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) , bem como na Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html)

* [Pré-configuráveis](#pre-configuring-core-components) para definir quais recursos estão disponíveis para autores de páginas por meio do [editor de modelo](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

* Built around [accessibility guidelines](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

* Built to support [responsive layout](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)

* Criado para oferecer suporte à [localização fácil](localization.md)

Components are available on the **Components** tab of the side panel of the page editor when [editing a page](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html).

Os componentes são agrupados de acordo com as categorias chamadas grupos de componentes para organizar e filtrar facilmente os componentes. O nome do grupo de componentes é exibido com o componente no navegador [de componentes](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) , e também é possível filtrar por grupo para localizar facilmente o componente correto.

>[!NOTE]
>
>Os Componentes principais são por padrão parte de um grupo oculto e não estão visíveis no navegador de componentes.
>
>Adicione os componentes necessários a um grupo visível ou personalize-os para que estejam disponíveis para autores.

## Pré-configuração dos componentes principais {#pre-configuring-core-components}

Configuração dos Componentes Fundamentais era a tarefa de um desenvolvedor. No entanto, com Componentes principais, um autor de modelo agora pode configurar vários recursos por meio do editor de modelo.

Por exemplo, se um componente de imagem não permitir upload de imagem do sistema de arquivos, ou se um componente de texto permitir apenas determinada formatação de parágrafo, esses recursos poderão ser ativados ou desativados com um clique simples.

Consulte [Criar modelos de página](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) para obter mais informações.

### Editar caixas de diálogo e design {#edit-and-design-dialogs}

Como os Componentes principais podem ser pré-configurados por autores de modelo para definir quais opções são permitidas como parte de um modelo e configuradas posteriormente pelo autor da página para definir o conteúdo da página real, cada componente pode ter opções em duas caixas de diálogo diferentes.

|  | Descrição | O que ele controla | Exemplos |
|--- |--- |--- |--- |
| **Editar caixa de diálogo** | Opções que um **autor** de página pode modificar durante a edição normal de página dos componentes colocados | O conteúdo exibido pelo componente e como ela será exibida na página. | Formatação de texto de conteúdo, gire uma imagem em uma página |
| **Caixa de diálogo de design** | Opções que um **autor de modelo** pode modificar ao configurar um modelo de página. | Que opções o autor da página tem disponível ao editar o componente | Quais opções de formatação de texto estão disponíveis, quais imagens no local estão disponíveis |

### Estilo do componente {#component-styling}

Os estilos da maioria dos componentes principais podem ser definidos usando o sistema de estilo AEM.

* Um autor de modelo pode definir quais estilos estão disponíveis para um componente específico na Caixa de diálogo de design desse componente.
* O autor do conteúdo pode escolher quais estilos aplicar ao adicionar o componente e criar conteúdo.

Para obter mais detalhes, consulte [a documentação do Sistema](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) de estilo.

>[!NOTE]
>
>No AEM 6.3, service pack 2 (6.3.2.0) ou mais recente é necessário para ativar o recurso do sistema de estilo.

## Lista de componentes principais disponíveis {#list-of-core-components-available}

A seguir está uma lista dos Componentes principais disponíveis vinculados às páginas que descrevem seus recursos de diálogo de edição e design detalhadamente.

A versão atual dos Componentes principais apresenta os seguintes componentes.

* [Expandir/recolher](accordion.md)
* [Caminho](breadcrumb.md)
* [Imagem](button.md)
* [Container](container.md)
* [Carrossel](carousel.md)
* [Fragmento do conteúdo](content-fragment-component.md)
* [Lista de fragmentos do conteúdo](content-fragment-list.md)
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
>Algumas versões de Componentes principais individuais podem ser compatíveis apenas com determinadas versões do AEM.
>
>Consulte a página de ajuda individual (vinculada à lista anterior) para o componente específico para obter informações de compatibilidade ou consultar o [documento Principais versões](versions.md) dos componentes para obter mais informações.

>[!NOTE]
>
>Dependendo do seu caso, você pode ter componentes personalizados desenvolvidos explicitamente para as suas necessidades. Eles podem até ter o mesmo nome que alguns dos componentes discutidos aqui.
>Os componentes principais do formulário não estão relacionados ao AEM Forms.

## Recursos do desenvolvedor {#developer-resources}

Consulte [a documentação do desenvolvedor de Componentes](developing.md) principais para obter informações técnicas relacionadas aos componentes principais.
