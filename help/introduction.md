---
title: Introdução aos Componentes principais
description: 'Os componentes principais fornecem componentes básicos robustos e extensíveis, baseados na tecnologia mais recente e nas práticas recomendadas. '
translation-type: tm+mt
source-git-commit: 850fbeec3cb31f4ea6873daa2555953684fd5a8d
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 26%

---


# Introdução aos componentes principais{#core-components-introduction}

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas. Os componentes sempre foram um elemento fundamental da experiência do AEM, tornando a criação de páginas simples, mas poderosa para o autor e o desenvolvimento de componentes flexíveis e extensíveis para o desenvolvedor.

Os componentes principais são um conjunto de componentes padronizados de Gestão de conteúdo da Web (WCM) para AEM acelerar o tempo de desenvolvimento e reduzir o custo de manutenção de seus sites.

## Recursos {#resources}

* **[Biblioteca de componentes:](https://www.adobe.com/go/aem_cmp_library)** uma coleção de exemplos para visualização dos componentes em suas várias configurações.
* **Documentação do componente (este documento):** Para desenvolvedores e autores, com detalhes sobre cada componente.
* **[Repositório GitHub dos componentes principais:](https://github.com/adobe/aem-core-wcm-components)** Para obter detalhes do desenvolvedor sobre cada componente e download do projeto.
* Introdução:
   * **[Sucesso com os componentes principais:](/help/developing/success.md)** Diretrizes para considerar bem antes do start de qualquer projeto que usará os componentes principais.
   * **[Tutorial de WKND:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** um tutorial de dois dias para criar um novo site.
   * **[Tutorial do Summit: ](https://expleague.azureedge.net/labs/L767/index.html)** um tutorial de duas horas para a construção de um novo site (de um Laboratório no US Summit 2019).
   * **[Gems Webinar: ](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** um tour guiado dos Componentes Principais (gravado em dez de 2018).

## Recursos {#features}

|  |  |
|---|---|
| Prontos para produção | Os Componentes principais são 28 componentes robustos que são bem testados, amplamente utilizados e têm bom desempenho. |
| Pronto para nuvem | Seja em [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), em [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), ou no local, eles funcionam apenas. |
| Versáteis | Os componentes representam conceitos genéricos com os quais os autores podem montar praticamente qualquer layout. |
| Configurável | As políticas de conteúdo [em nível de modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html#content-policies) definem quais recursos os autores de página podem usar ou não. |
| Trackable | A [integração da Camada de Dados do Cliente Adobe](/help/developing/data-layer/overview.md) permite rastrear todos os aspectos da experiência do visitante. |
| Acessíveis | Eles estão em conformidade com o [padrão WCAG 2.1](https://www.w3.org/TR/WCAG21/), fornecem etiquetas ARIA e suportam a navegação do teclado ([problemas conhecidos](https://github.com/adobe/aem-core-wcm-components/issues?utf8= ✓&amp;q=is%3Aissue+is%3Aopen+acessibilidade+in%3Atitle)). |
| Amigável para SEO | A saída HTML é semântica e fornece [schema.org](https://schema.org) anotações de microdados. |
| WebApp-Ready | A [saída JSON simplificada](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) permite a renderização do lado do cliente, ainda com uma possibilidade de [edição no contexto](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html). |
| Suporte AMP | Os componentes têm suporte [integrado para o padrão AMP,](/help/developing/amp.md) acelerando suas experiências móveis. |
| Kit de design | Um [kit de interface de usuário para Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) permite que os designers criem wireframes que podem, então, [estilo, conforme necessário](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_WKND.xd). |
| Temível | Os componentes implementam o [Sistema de estilo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/style-system.html) e a marcação segue [convenções CSS de BEM](http://getbem.com/). |
| Personalizável | Vários padrões permitem [fácil personalização](developing/customizing.md), desde o ajuste do HTML até a reutilização avançada da funcionalidade. |
| Versões | A [política de controle de versão](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garante que os Componentes principais não quebrem seu site ao melhorar coisas que podem afetar você. |
| Localizável | A resolução de referência inteligente permite que determinados componentes localizem e [renderizem o conteúdo localizado correspondente automaticamente](get-started/localization.md). |
| Abrir origem | Se algo não for como deveria, [contribua com seus aprimoramentos!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |

## Os componentes {#the-components}

A versão atual dos Componentes principais apresenta os seguintes componentes:

### Componentes do modelo {#template-components}

* [Página](components/page.md)
* [Navegação](components/navigation.md)
* [Navegação de idiomas](components/language-navigation.md)
* [Caminho](components/breadcrumb.md)
* [Busca rápida](components/quick-search.md)

### Componentes de criação de página {#page-authoring-components}

* [Título](components/title.md)
* [Texto](components/text.md)
* [Imagem](components/image.md)
* [Botão](components/button.md)
* [Teaser](components/teaser.md)
* [Download](components/download.md)
* [Lista](components/list.md)
* [Fragmento de experiência](components/experience-fragment.md)
* [Fragmento do conteúdo](components/content-fragment-component.md)
* [Lista de fragmentos do conteúdo](components/content-fragment-list.md)
* [Incorporar](components/embed.md)
* [Compartilhamento em mídia social](components/sharing.md)
* [Separador](components/separator.md)
* [Barra de progresso](components/progress-bar.md)
* [Visualizador de PDF](components/pdf-viewer.md)

### Componentes do container {#container-components}

* [Container](components/container.md)
* [Carrossel](components/carousel.md)
* [Guias](components/tabs.md)
* [Menu sanfonado](components/accordion.md)

### Componentes de forma {#form-components}

* [Contêineres de formulário](components/forms/form-container.md)
* [Texto do formulário](components/forms/form-text.md)
* [Opções de formulário](components/forms/form-options.md)
* [Formulário oculto](components/forms/form-hidden.md)
* [Botão de formulário](components/forms/form-button.md)

>[!NOTE]
>
>Os Componentes principais não estão imediatamente disponíveis para os autores, a [equipe de desenvolvimento deve primeiro integrá-los ao seu ambiente](get-started/using.md). Uma vez integrados, eles podem ser disponibilizados e pré-configurados por meio do [editor de modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Algumas versões dos Componentes principais individuais podem ser compatíveis apenas com certas versões do AEM.
>
>Consulte a página de ajuda individual (ligada à lista anterior) para o componente específico para informações de compatibilidade ou referência das [Versões dos componentes principais](versions.md) para mais informações.

## Requisitos do sistema {#system-requirements}

| Componentes principais | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | Java SE | Maven |
|---------|---------|---------|---------|---------|---------|
| [2,12,2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | Contínuo | 6.5.5.0+ * | 6.4.8.1+ * | 8, 11 | 3.3.9+ |

>[!NOTE]
>
>(*) Desde a versão 2.11.0, `org.apache.sling.models.impl` versão 1.4.12 ou superior é necessário (devido a [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Isso será fornecido para AEM 6.4 e 6.5 em um Service Pack futuro. Até então, o pacote Sling Models é incluído no pacote `core.wcm.components.all`.

Para saber os requisitos das versões anteriores do Componente principal, consulte [Versões dos componentes principais](versions.md).

Os Componentes principais exigem o uso de [modelos editáveis](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) e não são compatíveis com a interface clássica nem com modelos estáticos. Se necessário, verifique as [AEM Ferramentas de Modernização](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) para atualizar seu projeto com esses recursos AEM modernos.

Para configurar seu ambiente de desenvolvimento local, consulte [esta visão geral para AEM como um SDK de Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) ou este documento [para versões mais antigas do AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).
