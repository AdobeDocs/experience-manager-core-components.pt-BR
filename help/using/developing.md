---
title: Componentes principais do desenvolvimento
seo-title: Componentes principais do desenvolvimento
description: Os Componentes principais fornecem componentes básicos e extensíveis que oferecem recursos ricos em recursos, entrega contínua, controle de versão de componentes, implementação moderna, marcação de leiaute e exportação de conteúdo JSON.
seo-description: Os Componentes principais fornecem componentes básicos e extensíveis que oferecem recursos ricos em recursos, entrega contínua, controle de versão de componentes, implementação moderna, marcação de leiaute e exportação de conteúdo JSON.
uuid: 68569 da 2-9 bc 8-4 e 20-9 a 71-e 5816 ace 51 ce
contentOwner: Usuário
content-type: referência
topic-tags: developing
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 157 a 2 ec 3-9 fca -4 fad -977 a-d 93013 fe 218
translation-type: tm+mt
source-git-commit: f30a6a9f4d41c672472beb60767f3766479d9c16

---


# Developing Core Components{#developing-core-components}

## Visão geral {#overview}

Os Componentes principais fornecem componentes básicos e extensíveis, e seus destaques são:

* Recursos repletos de funções
   * [Opções de configuração flexíveis](authoring.md) para acomodar muitos casos de uso
   * [Recursos pré-configuráveis](authoring.md#pre-configuring-core-components) para definir quais recursos estão disponíveis para autores de páginas
* Entrega contínua
   * Melhorias na funcionalidade incremental frequente
   * Availability of the [source code on GitHub](https://github.com/adobe/aem-core-wcm-components) to allow the developer community to give feedback and contribute
   * Installation through a [separately released content package](https://github.com/adobe/aem-core-wcm-components/releases) for component upgrades to be done independently from AEM upgrades
* [Controle de versão do componente](guidelines.md#component-versioning)
   * [Garantir compatibilidade em uma versão](#upgrade-of-core-components), ainda permitir que os componentes evoluam
   * Permitir que várias versões de um componente coexistam no mesmo ambiente
* Implementação moderna
   * Markup defined in [HTML Template Language](https://helpx.adobe.com/experience-manager/htl/using/overview.html) (HTL)
   * Content model logic implemented with [Sling Models](https://sling.apache.org/documentation/bundles/models.html)
* Markan markup
   * Following [Block Element Modifier](https://getbem.com/) (BEM) notation as of Release 2.0.0
      * Prior release follow [Bootstrap](https://getbootstrap.com/css/) naming conventions
   * Built around [accessibility guidelines](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)
   * Capaz de ser usado para sites responsivos e móveis
* Capacidade de serializar como JSON o modelo de conteúdo para casos de uso com CMS sem marcas
* Acessível
   * Compliant with the [WCAG 2.0 AA standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

>[!CAUTION]
>
>Core Components require AEM 6.3 or later and Java 8 and and require the use of [editable templates](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)
>
>Os Componentes principais não funcionam com a interface clássica nem com modelos estáticos.

## Gems Session Overview {#gems-session-overview}

For an introduction to the Core Components, the features they offer, and how they are leveraged in AEM, check out the AEM Gems Session [AEM Core Components.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[O Gems no Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) é uma série de soluções técnicas oferecidas pelos especialistas da Adobe. Esta série complementa a documentação do produto e de todos os outros canais técnicos, permitindo que os desenvolvedores entrem em contato e se aprofunde em um tópico específico.

## WKND Developer Tutorial {#wknd-developer-tutorial}

Get started developing AEM Sites with Core Components by following [this step-by-step tutorial.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Delivered over GitHub {#delivered-over-github}

Os Componentes principais são desenvolvidos e entregues por meio do github.

CODE EM GITHUB

Você pode encontrar o código desta página no github

* [Abrir o projeto aem-core-wcm-components no github](https://github.com/adobe/aem-core-wcm-components)
* Download the project as [a ZIP file](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

See the [Using Core Components](using.md) documentation page to learn how to get started using them in your project.

Ter os componentes principais no github permite fazer atualizações frequentes e ouvir o feedback da comunidade de desenvolvedores do AEM. Além disso, isso deve ajudar os clientes e parceiros a seguir padrões similares ao construir componentes personalizados.

>[!NOTE]
>
>To keep up-to-date on the latest changes to the core components, you can watch the [Core Components repository](https://github.com/adobe/aem-core-wcm-components) on GitHub.

## Biblioteca de componentes

Check out the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library.html), which showcases the current release of the Core Components and gives examples of their usage.

### Sample Content Run-Mode {#sample-content-run-mode}

The Core Components are visible in the Quickstart when the sample content is present, because the [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) uses them. However, when running in production (in `nosamplecontent` runmode, without sample content enabled), the core components won&#39;t be present anymore and must be installed on the AEM instances by the development and/or operations team.

>[!NOTE]
>
>In production environments, always run the Quickstart in `nosamplecontent` runmode. To use the Core Components in `nosamplecontent` runmode, follow the instructions of the [Using Core Components](using.md) documentation page.

## Technical Capabilities {#technical-capabilities}

A tabela a seguir apresenta uma visão geral das diferenças entre componentes principais e componentes de fundação.

For details about their authoring capabilities and options to pre-configurable them, [refer to the authoring page about them](authoring.md).

| **Recurso** | **Componente principal** | **Componente de base** |
|-----|---|---|
| Implementação lógica | Java POJOs with [Sling Models](https://sling.apache.org/documentation/bundles/models.html) annotations | Código JSP |
| Definição de marcação | [Sintaxe HTML do Modelo de HTML](https://helpx.adobe.com/experience-manager/htl/user-guide.html) (HTL) | Código JSP |
| Limpeza de XSS | Automatizado por HTL | Principal manual |
| Nomenclatura de classes CSS | Standardized naming convention based on [Block Element Modifier](https://getbem.com/) (BEM) notation (as of release 2.0.0) | Esquemas personalizados |
| Definição da caixa de diálogo | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + Classic UI |
| Saída JSON | [Sling Model Exporter with Jackson serialization](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet de sling padrão |
| Versões | [Para o modelo e HTL](guidelines.md) | Nenhum |
| Testes | Testes de unidade + Testes de integração | Testes de integração |
| Entrega | [Via github pública](https://github.com/adobe/aem-core-wcm-components) | Por início rápido |
| Licença | [Licença do Apache](https://www.apache.org/licenses/LICENSE-2.0) | Proprietário da Adobe |
| Contribuição | Solicitação de extração | Não é possível |
| Acessibilidade | Fully compliant with the [WCAG 2.0 AA standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) | Only partially compliant with the [WCAG 2.0 AA standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) |

## Component List {#component-list}

A tabela a seguir lista os Componentes principais disponíveis, vinculação à API e indica quais componentes de fundação eles substituem.

| Componente principal | Descrição | Componentes de base substituídos |
|---|---|---|
| [Modos](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page) | Página responsiva trabalhando com editor de modelo | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Caminho](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb) | Navegação de hierarquia de página | `/libs/foundation/components/breadcrumb` |
| [Título](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title) | Título H 1-H 6 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Text](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Rich Text | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Imagem](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image) | Carregamento inteligente e lento de um ótimo tamanho de execução | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Lista](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list) | Lista de páginas | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Compartilhamento em rede social](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/sharing/v1/sharing) | Widget de compartilhamento do Facebook e Pinterest | `-` |
| [Contêineres de formulário](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container) | Sistema de parágrafos de formulário responsivo | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Texto do formulário](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text) | Campo de entrada de texto | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Opções de formulário](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options) | Campo de entrada de várias opções | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulário oculto](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden) | Campo de entrada oculto | `/libs/foundation/components/form/hidden` |
| [Botão de formulário](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button) | Botão Enviar ou personalizar | `/libs/foundation/components/form/submit` |
| [Navegação](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation) | Um componente de navegação do site que lista a hierarquia de página aninhada | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navegação de idiomas](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation) | Um idioma e um alternador de país que lista a estrutura de idioma global | `-` |
| [Pesquisa rápida](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search) | Um componente de pesquisa que exibe os resultados como sugestões no local em um menu suspenso | `/libs/foundation/components/search` |
| [Teaser](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser) | Permite que o autor do conteúdo crie facilmente um teaser para mais conteúdo usando uma imagem, um título ou texto formatado e um link para outro conteúdo ou outras ações | `-` |
| [Guias](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs) | Permite que o autor do conteúdo organize o conteúdo da página em várias guias | `-` |
| [Carrossel](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel) | Permite que o autor do conteúdo organize o conteúdo em um carrossel giratório de slides | `/libs/foundation/components/carousel` |
| [Fragmento do conteúdo](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragment/v1/contentfragment) | Permite a exibição de um fragmento do conteúdo | `-` |
| [Lista de fragmentos do conteúdo](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragmentlist/v1/contentfragmentlist) | Permite a exibição de uma lista de fragmentos de conteúdo | `-` |
| [Separador](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/separator/v1/separator) | Separa o conteúdo em uma página | `-` |
| [Expandir/recolher](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/accordion/v1/accordion) | Organizar os painéis de conteúdo em um acordeão flexível | `-` |
| [Container](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/container/v1/container) | Organizar componentes em um contêiner | `-` |
| [Imagem](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/button/v1/button) | Criar um botão em uma página | `-` |
| [Download](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/download/v1/download) | Adicionar um ativo baixável a uma página | `-` |

### Upcoming Components {#upcoming-components}

For an overview of the upcoming Core Componente roadmap see the [project wiki on GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Upgrade of Core Components {#upgrade-of-core-components}

Uma vantagem dos componentes com versões de versão é que ela permite separar a migração para uma nova versão do AEM da migração para novas versões de componentes. Além disso, se novas versões de componentes estiverem disponíveis, permitirá a migração individual de cada componente para a nova versão.

As migrações para uma nova versão do AEM não afetarão a forma como os Componentes principais funcionam, desde que suas versões também sejam compatíveis com a nova versão do AEM que está sendo migrada. Customizations made to the Core Components should not be affected either, as long as they don&#39;t use APIs that have been [deprecated or removed](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

As migrações para novas versões dos Componentes principais não afetarão a forma como o componente funciona, mas novos recursos podem ser introduzidos para autores de páginas, o que pode exigir alguma configuração por um editor de modelo, caso o comportamento padrão não seja desejado. Customizations however might need to be adapted, for more details see the [Customizing Core Components](customizing.md#upgrade-compatibility-of-customizations) page.

## When to Use the Core Components? {#when-to-use-the-core-components}

Como os Componentes principais são totalmente novos e oferecem vários benefícios, recomendamos que os novos projetos do AEM sejam usados. Para projetos existentes, uma migração deve ser parte de um esforço de projeto maior, por exemplo, uma reformulação ou uma atualização geral.

Portanto, a Adobe fornece as seguintes recomendações:

* **Novos projetos**
Novos projetos devem sempre tentar usar Componentes principais. If Core Components cannot be used directly or [extended](customizing.md) to satisfy project requirements, then create a custom component following the component architecture set forth in core components. Except where not otherwise possible, avoid using the [foundation components](developing.md).
* **A Recomendação de projetos**
existentes continua usando os componentes [de base](developing.md), a menos que um site ou a redefinição de componentes esteja planejada.\
   As they are very widely used by most existing projects, the foundation components [will continue to be supported.](developing.md)
* **Novos componentes
personalizados** Avaliar se um componente [principal existente pode ser personalizado](customizing.md).\
   If not, recommendation is to build a new custom component following the [Component Guidelines](guidelines.md).
* **Componentes
personalizados existentes** Se os componentes funcionarem como esperado e os mantenham como estão.\
   Caso contrário, consulte &quot;Novos componentes personalizados&quot; acima.

## Migração para os componentes principais

Qualquer novo projeto deve ser implementado com Componentes principais. No entanto, os projetos existentes geralmente terão implementações extensas dos Componentes fundamentais.

Um esforço maior em um projeto existente (por exemplo, uma reformulação ou atualização geral) geralmente oferece uma chance de migrar para os Componentes principais. Para facilitar essa migração, a Adobe forneceu várias ferramentas de migração para incentivar a adoção dos Componentes principais e da tecnologia mais recente do AEM.

[As Ferramentas de modernização do AEM](http://opensource.adobe.com/aem-modernize-tools/) permitem a fácil conversão de:

* Modelos estáticos para modelos editáveis
* Configurações de design para políticas
* Componentes fundamentais aos componentes principais
* Interface clássica para IU habilitada para toque

For further information about the usage of these tools, [see their documentation](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>As Ferramentas de modernização do AEM são um esforço da comunidade e não são suportadas ou garantidas pela Adobe.

## Core Component Support {#core-component-support}

Os Componentes principais são parte integrante do AEM e são compatíveis com os mesmos termos e condições que se fossem entregues como parte do Início rápido.

Como outros recursos do produto AEM, a regra geral é: Os componentes são anunciados pela primeira vez e os mais antigos foram removidos para a versão do AEM a seguir. Que dá aos clientes pelo menos um ciclo de lançamento para se mover para a nova versão do componente, antes de soltar seu suporte.

A versão de cada componente declara claramente as versões do AEM que ele suporta. Quando o suporte for interrompido para uma versão do AEM, então o suporte aos Componentes principais dessa versão do AEM será compatível.

For details about the support of component customizations, see the [Customizing Core Components](customizing.md) page.

## Foundation Component Support {#foundation-component-support}

Como os componentes de fundação serviram como base de muito desenvolvimento de projeto em muitas versões do AEM, eles continuarão a ser suportados no futuro próximo.

However, Adobe&#39;s development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.

**Ler em seguida:**

* [Usar componentes principais](using.md) - comece a usar componentes principais em seu próprio projeto.
* [Diretrizes de componentes](guidelines.md) - para saber os padrões de implementação dos Componentes principais.
