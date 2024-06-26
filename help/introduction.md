---
title: Introdução aos Componentes principais
description: Obtenha soluções para problemas com os Componentes principais e permita que outros criem elementos dentro do AEM.
role: Architect, Developer, Admin, User
exl-id: d294db22-4cb0-48a4-9366-03fda5b8bb8e
source-git-commit: 39c9dd3374ea7c31b9f03cc02e883ab26f463368
workflow-type: ht
source-wordcount: '808'
ht-degree: 100%

---


# Introdução aos Componentes principais{#core-components-introduction}

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas. Os componentes sempre foram um elemento fundamental da experiência do AEM, tornando a criação de páginas simples, mas poderosa para o autor e o desenvolvimento de componentes flexíveis e extensíveis para o desenvolvedor.

Os Componentes principais são um conjunto de componentes padronizados de Gerenciamento de Conteúdo Online (WCM, na sigla em inglês) para que o AEM acelere o tempo de desenvolvimento e reduza o custo de manutenção de seus sites.

## Recursos {#resources}

* **[Biblioteca de componentes](https://www.adobe.com/go/aem_cmp_library_br)**: Uma coleção de exemplos para exibir os componentes em suas várias configurações.
* **Documentação de componentes (este documento)**: Para desenvolvedores e autores, com detalhes sobre cada componente.
* **[Repositório GitHub dos Componentes principais](https://github.com/adobe/aem-core-wcm-components)**: Para detalhes do desenvolvedor sobre cada componente e download do projeto.
* Introdução:
   * **[Sucesso com os Componentes principais](/help/developing/success.md)**: Diretrizes que devem ser consideradas antes do início de qualquer projeto que usará os Componentes principais.
   * **[Tutorial do WKND](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=pt-BR)**: Tutorial de dois dias para criar um novo site.
   * **[Tutorial do Summit](https://expleague.azureedge.net/labs/L767/index.html)**: Tutorial de duas horas para a criação de um novo site (de um laboratório no US Summit 2019).
   * **[Gems Webinar](https://helpx.adobe.com/br/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)**: Tour orientado sobre os Componentes principais (gravado em dezembro de 2018).

## Recursos {#features}

|  |  |
|---|---|
| Prontos para produção | Os componentes principais incluem 30 componentes WCM robustos, bem testados, amplamente usados e que apresentam um bom desempenho. |
| Prontos para nuvem | Seja no [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=pt-BR), no [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), ou no local, eles simplesmente funcionam. |
| Versáteis | Os componentes representam conceitos genéricos com os quais os autores podem reunir quase qualquer layout. |
| Configuráveis | As [políticas de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=pt-BR#content-policies) no nível do modelo definem quais recursos os autores da página podem usar ou não usar. |
| [Responsivo](responsive.md) | Todos os Componentes principais foram projetados para serem totalmente responsivos, garantindo uma experiência perfeita em todos os dispositivos |
| Rastreáveis | A [integração da Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md) permite rastrear todos os aspectos da experiência do visitante. |
| Acessíveis | Eles estão em conformidade com o [padrão WCAG 2.1](https://www.w3.org/TR/WCAG21/), fornecem rótulos ARIA e são compatíveis com a navegação pelo teclado ([problemas conhecidos](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)). |
| Compatíveis com SEO | A saída HTML é semântica e fornece anotações de microdados [schema.org](https://schema.org). |
| Prontos para aplicativos Web | A [saída JSON simplificada](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/develop-sling-model-exporter.html?lang=pt-BR) permite renderização no lado do cliente, ainda com uma possibilidade de [edição no contexto](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=pt-BR). |
| Suporte ao AMP | Os componentes têm [suporte para o padrão AMP](/help/developing/amp.md) integrado, o que acelera suas experiências em dispositivos móveis. |
| Kit de design | Um [kit de interface do usuário para Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) permite que os designers criem wireframes para que possam [estilizar conforme necessário](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-0.0.2/AEM_UI-kit-WKND.xd). |
| Temáticos | Os componentes implementam o [Sistema de Estilos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=pt-BR), e a marcação segue as [convenções de CSS de BEM.](https://getbem.com/) |
| Personalizáveis | Vários padrões permitem [fácil personalização](developing/customizing.md), desde o ajuste do HTML até a reutilização de funcionalidade avançada. |
| Versões | A [política de controle de versão](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garante que os Componentes principais não interrompam seu site ao melhorar coisas que podem afetar você. |
| Localizáveis | A resolução de referência inteligente permite que certos componentes encontrem e [renderizem conteúdos correspondentes localizados automaticamente](get-started/localization.md). |
| Código aberto | Se algo não sair como deveria, [contribua com suas melhorias!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |


## Os componentes do WCM {#the-wcm-components}

A versão atual dos Componentes principais apresenta os seguintes componentes:

### Componentes de modelos {#template-components}

* [Página](components/page.md)
* [Navegação](components/navigation.md)
* [Navegação de idiomas](components/language-navigation.md)
* [Navegação estrutural](components/breadcrumb.md)
* [Busca rápida](components/quick-search.md)
* [Índice](components/tableofcontents.md)

### Componentes de Criação de página {#page-authoring-components}

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
* [Incorporação](components/embed.md)
* [Compartilhamento em redes sociais](components/sharing.md) (descontinuado)
* [Separador](components/separator.md)
* [Barra de progresso](components/progress-bar.md)
* [Visualizador de PDF](components/pdf-viewer.md)

### Componentes de Contêineres {#container-components}

* [Contêiner](components/container.md)
* [Carrossel](components/carousel.md)
* [Guias](components/tabs.md)
* [Acordeão](components/accordion.md)

### Componentes de formulários {#form-components}

* [Contêineres de formulário](components/forms/form-container.md)
* [Texto do formulário](components/forms/form-text.md)
* [Opções de formulário](components/forms/form-options.md)
* [Formulário oculto](components/forms/form-hidden.md)
* [Botão de formulário](components/forms/form-button.md)

>[!NOTE]
>
>Os Componentes principais não estão imediatamente disponíveis para os autores, a [equipe de desenvolvimento deve primeiro integrá-los ao seu ambiente](get-started/using.md). Uma vez integrados, eles podem ser disponibilizados e pré-configurados pelo [editor de modelos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR).

>[!NOTE]
>
>Algumas versões dos Componentes principais individuais podem ser compatíveis apenas com certas versões do AEM.
>
>Consulte a página de ajuda individual (ligada à lista anterior) para o componente específico para informações de compatibilidade ou referência das [Versões dos componentes principais](versions.md) para mais informações.

## Requisitos do sistema {#system-requirements}

| Lançamento dos Componentes principais | AEM as a Cloud Service | Nível de correção do AEM 6.5 | Versão do Java SE | Versão do Maven |
|---------|---------|---------|---------|---------|
| [2.25.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.25.4) | Contínuo | 6.5.21.0+ | 8, 11 | 3.3.9+ |

Para saber quais são os requisitos das versões anteriores dos Componentes principais, consulte [Versões dos Componentes principais](versions.md).

Os Componentes principais exigem o uso de [modelos editáveis](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=pt-BR) e não são compatíveis com a IU Clássica nem com modelos estáticos. Se necessário, verifique as [Ferramentas de modernização do AEM](https://opensource.adobe.com/aem-modernize-tools/) para atualizar seu projeto com esses recursos modernos do AEM.

Para configurar seu ambiente de desenvolvimento local, confira esta [visão geral do SDK do AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html?lang=pt-BR) ou este documento [para versões mais antigas do AEM](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=pt-BR).

>[!TIP]
>
>Os Componentes principais fazem parte automaticamente do AEM as a Cloud Service, e você sempre terá a versão mais recente dos Componentes principais.
>
>Consulte o documento [Uso dos Componentes principais](/help/get-started/using.md) para mais informações sobre como começar a usar os Componentes principais no AEMaaCS e no local.

## Outros componentes {#other-components}

Há componentes adicionais disponíveis para autores do AEM, que estão integrados nos componentes principais.

* [Os componentes principais de email](/help/email/introduction.md) - Descubra componentes integrados aos componentes principais especificamente para uso no Adobe Campaign.
