---
title: Introdução aos Componentes principais
description: 'Os Componentes principais fornecem componentes básicos robustos e extensíveis, baseados na tecnologia mais recente e nas práticas recomendadas. '
role: Architect, Developer, Administrator, Business Practitioner
exl-id: d294db22-4cb0-48a4-9366-03fda5b8bb8e
source-git-commit: 9f7ecb12c7135033a87508901a5c8bd006f72a0e
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 25%

---

# Introdução aos componentes principais{#core-components-introduction}

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas. Os componentes sempre foram um elemento fundamental da experiência do AEM, tornando a criação de páginas simples, mas poderosa para o autor e o desenvolvimento de componentes flexíveis e extensíveis para o desenvolvedor.

Os Componentes principais são um conjunto de componentes padronizados do WCM (Web Content Management, gerenciamento de conteúdo da Web) para AEM acelerar o tempo de desenvolvimento e reduzir o custo de manutenção de seus sites.

## Recursos {#resources}

* **[Biblioteca de componentes:](https://www.adobe.com/go/aem_cmp_library)** uma coleção de exemplos para exibir os componentes em suas várias configurações.
* **Documentação do componente (este documento):**  para desenvolvedores e autores, com detalhes sobre cada componente.
* **[Repositório GitHub dos componentes principais:](https://github.com/adobe/aem-core-wcm-components)** para obter detalhes do desenvolvedor sobre cada componente e download do projeto.
* Introdução:
   * **[Sucesso com os componentes principais:](/help/developing/success.md)** diretrizes que devem ser consideradas antes do início de qualquer projeto que usará os componentes principais.
   * **[Tutorial WKND: ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** um tutorial de dois dias para criar um novo site.
   * **[Tutorial do Summit: ](https://expleague.azureedge.net/labs/L767/index.html)** um tutorial de duas horas para a criação de um novo site (de um laboratório no US Summit 2019).
   * **[Webinar do Gems: ](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** um tour orientado por componentes principais (gravado em dezembro de 2018).

## Recursos {#features}

|  |  |
|---|---|
| Prontos para produção | Os Componentes principais são 28 componentes robustos que são bem testados, amplamente usados e têm bom desempenho. |
| Pronto para nuvem | Seja em [AEM como um Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), em [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), ou no local, eles apenas funcionam. |
| Versáteis | Os componentes representam conceitos genéricos com os quais os autores podem reunir quase qualquer layout. |
| Configurável | As políticas de conteúdo [no nível do modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html#content-policies) definem quais recursos os autores da página podem usar ou não usar. |
| Rastreável | A [integração da camada de dados do cliente do Adobe](/help/developing/data-layer/overview.md) permite rastrear todos os aspectos da experiência do visitante. |
| Acessíveis | Eles estão em conformidade com o [padrão WCAG 2.1](https://www.w3.org/TR/WCAG21/), fornecem etiquetas ARIA e suportam a navegação pelo teclado ([problemas conhecidos](https://github.com/adobe/aem-core-wcm-components/issues?utf8= ✓&amp;q=is%3Aissue+is%3Aopen+acessibilidade+in%3Atitle)). |
| compatível com SEO | A saída HTML é semântica e fornece anotações de microdados [schema.org](https://schema.org). |
| WebApp-Ready | O [saída JSON simplificada](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) permite renderização no lado do cliente, ainda com uma possibilidade de [edição no contexto](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html). |
| Suporte ao AMP | Os componentes têm suporte [integrado para o padrão AMP,](/help/developing/amp.md) acelerando suas experiências móveis. |
| Kit de design | Um [kit de interface do usuário para Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) permite que os designers criem wireframes para que possam [estilo, conforme necessário](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-0.0.2/AEM_UI-kit-WKND.xd). |
| Themeable | Os componentes implementam o [Sistema de estilos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/style-system.html) e a marcação segue [Convenções CSS do BEM](http://getbem.com/). |
| Personalizável | Vários padrões permitem [fácil personalização](developing/customizing.md), desde o ajuste do HTML até a reutilização de funcionalidade avançada. |
| Versões | A [política de controle de versão](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garante que os Componentes principais não quebrem seu site ao melhorar coisas que podem afetar você. |
| Localizável | A resolução de referência inteligente permite que determinados componentes encontrem e [renderizem o conteúdo localizado correspondente automaticamente](get-started/localization.md). |
| Abrir de origem | Se algo não for como deveria, [contribua com suas melhorias!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |

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
* [Fragmento de conteúdo](components/content-fragment-component.md)
* [Lista de fragmentos do conteúdo](components/content-fragment-list.md)
* [Incorporar](components/embed.md)
* [Compartilhamento em mídia social](components/sharing.md)
* [Separador](components/separator.md)
* [Barra de progresso](components/progress-bar.md)
* [Visualizador de PDF](components/pdf-viewer.md)

### Componentes do contêiner {#container-components}

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
| [2.16.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.4) | Contínuo | 6.5.5.0+ * | 6.4.8.1+ * | 8, 11 | 3.3.9+ |

>[!NOTE]
>
>(*) Desde a versão 2.11.0, `org.apache.sling.models.impl` versão 1.4.12 ou superior é necessário (devido a [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Isso será fornecido para AEM 6.4 e 6.5 em um Service Pack futuro. Até lá, o pacote Sling Models é incluído no pacote `core.wcm.components.all`.

Para conhecer os requisitos das versões anteriores do Componente principal, consulte [Versões dos componentes principais](versions.md).

Os Componentes principais exigem o uso de [modelos editáveis](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) e não são compatíveis com a interface do usuário clássica nem modelos estáticos. Se necessário, verifique as [Ferramentas de Modernização AEM](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) para atualizar seu projeto com esses recursos de AEM modernos.

Para configurar seu ambiente de desenvolvimento local, marque [esta visão geral para AEM como um Cloud Service SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) ou este documento [para versões mais antigas do AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

>[!TIP]
>
>Os Componentes principais fazem automaticamente parte do AEM como um Cloud Service e você sempre tem a versão mais recente dos Componentes principais.
>
>Consulte o documento [Using Core Components](/help/get-started/using.md) para obter mais informações sobre como começar a usar os Componentes principais no AEMaaCS e no local.
