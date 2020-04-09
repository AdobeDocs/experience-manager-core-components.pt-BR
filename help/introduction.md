---
title: Introdução aos Componentes principais
description: 'Os componentes principais foram introduzidos para fornecer componentes básicos robustos e extensíveis, baseados na tecnologia mais recente e nas práticas recomendadas. '
translation-type: tm+mt
source-git-commit: 71c1cca664dde91968df16848650df9f0f0a5218

---


# Introdução aos componentes principais{#core-components-introduction}

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas. Os componentes sempre foram um elemento fundamental da experiência do AEM, tornando a criação de páginas simples, mas poderosa para o autor e o desenvolvimento de componentes flexíveis e extensíveis para o desenvolvedor.

Os componentes principais são um conjunto de componentes padronizados de Gestão de conteúdo da Web (WCM) para o AEM, para acelerar o tempo de desenvolvimento e reduzir o custo de manutenção de seus sites.

## Recursos {#resources}

* **[Biblioteca de componentes:](https://www.adobe.com/go/aem_cmp_library)**Uma coleção de exemplos para visualização dos componentes em suas várias configurações.
* **Documentação do componente (este documento):** Para desenvolvedores e autores, com detalhes sobre cada componente.
* Introdução:
   * **[Sucesso com os componentes principais:](/help/developing/success.md)**Diretrizes para considerar bem antes do start de qualquer projeto que usará os Componentes principais.
   * **[Tutorial da WKND:](https://docs.adobe.com/content/help/br/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**Um tutorial de dois dias para criar um novo site.
   * **[Tutorial de cúpula:](https://expleague.azureedge.net/labs/L767/index.html)**Um tutorial de duas horas para a construção de um novo site (de um Laboratório no US Summit 2019).
   * **[Webinar Gems:](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)**Um tour orientado dos Componentes Principais (gravado em dezembro de 2018).

## Recursos {#features}

|||—|—|Preparados para produção | Os componentes principais são 27 componentes robustos, bem testados, amplamente utilizados e com bom desempenho.||Pronto para a nuvem| Quer no [AEM como serviço](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)em nuvem, nos serviços [gerenciados da](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)Adobe, ou no local, eles funcionam apenas.||Versátil| Os componentes representam conceitos genéricos com os quais os autores podem montar praticamente qualquer layout.||Configurável| As políticas [de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html#content-policies) conteúdo no nível do modelo definem quais recursos os autores da página podem usar ou não.|
|Accessible| They comply [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), provide ARIA labels, and support keyboard navigation ([known issues](https://github.com/adobe/aem-core-wcm-components/issues?utf8= ✓&amp;q=is%3Aissue+is%3Aopen+acessibilidade+in%3Atitle)).|
|SEO-Friendly| The HTML output is semantic and provides [schema.org](https://schema.org) microdata annotations.||Pronto para WebApp| A saída [JSON](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) otimizada permite a renderização do lado do cliente, ainda com uma possibilidade de edição [](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)no contexto.||Kit de design| Um kit de [interface do usuário para Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) permite que os designers criem wireframes que podem então [estilizar conforme necessário](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_WKND.xd).|
|Themeable| The components implement the [Style System](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/style-system.html), and the markup follows [BEM CSS conventions](http://getbem.com/).||Personalizável| Vários padrões permitem personalização [](developing/customizing.md)fácil, desde o ajuste do HTML até a reutilização avançada da funcionalidade.||Controle de versão| A política [de](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) controle de versão garante que os Componentes principais não quebrem seu site ao melhorar coisas que podem afetar você.|
|Localizable|Smart reference resolution allows certain components to find and [render corresponding localized content automatically](get-started/localization.md).||Open Source| Se algo não for como deveria, [contribua com suas melhorias!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md)|

## Os componentes {#the-components}

A versão atual dos Componentes principais apresenta os seguintes componentes:

### Componentes de modelo {#template-components}

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

### Componentes do Container {#container-components}

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
>Os Componentes principais não estão imediatamente disponíveis para os autores, a [equipe de desenvolvimento deve primeiro integrá-los ao seu ambiente](get-started/using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Algumas versões dos Componentes principais individuais podem ser compatíveis apenas com certas versões do AEM.
>
>Consulte a página de ajuda individual (ligada à lista anterior) para o componente específico para informações de compatibilidade ou referência das [Versões dos componentes principais](versions.md) para mais informações.

## Requisitos do sistema {#system-requirements}

| Componentes principais | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | AEM 6.3 | Java SE | Maven |
---------|---------|---------|---------|---------|---------|---------
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Contínuo | 6.5.0.0+ | 6.4.4.0+ | 6.3.3.4+ | 8, 11 | 3.3.9+ |

Para saber os requisitos das versões anteriores dos Componentes principais, consulte Versões [dos componentes](versions.md)principais.

Os Componentes principais exigem o uso de modelos [](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) editáveis e não são compatíveis com a interface clássica nem com modelos estáticos. Se necessário, verifique as Ferramentas [de modernização do](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) AEM para atualizar seu projeto com esses recursos modernos do AEM.

Para configurar seu ambiente de desenvolvimento local, verifique [esta visão geral do AEM como um SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) de serviço em nuvem ou este documento [para versões mais antigas do AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).
