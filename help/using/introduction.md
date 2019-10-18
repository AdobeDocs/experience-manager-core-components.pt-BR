---
title: Introdução aos Componentes principais
seo-title: Introdução aos Componentes principais
description: 'Os componentes principais foram introduzidos para fornecer componentes básicos robustos e extensíveis, baseados na tecnologia mais recente e nas práticas recomendadas. '
seo-description: 'Os componentes principais foram introduzidos para fornecer componentes básicos robustos e extensíveis, baseados na tecnologia mais recente e nas práticas recomendadas. '
uuid: b815c7d1-fbb0-4480-bd23-42606ff8b1eb
contentOwner: User
content-type: reference
topic-tags: introduction
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: c44bb0d7-5d91-4659-878e-a0658fe29aa2
translation-type: tm+mt
source-git-commit: 683b4f4705c226275439a408423cbf1b23bea66f

---


# Introdução aos componentes principais{#core-components-introduction}

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas. Os componentes sempre foram um elemento fundamental da experiência do AEM, tornando a criação de páginas simples, mas poderosa para o autor e o desenvolvimento de componentes flexíveis e extensíveis para o desenvolvedor.

Os componentes principais foram introduzidos para fornecer componentes básicos robustos e extensíveis, baseados na tecnologia mais recente e nas práticas recomendadas, além de seguir as diretrizes de acessibilidade e serem compatíveis com o padrão WCAG 2.0 AA. Os componentes principais tornam a criação de páginas mais flexível e personalizável, e sua extensão para oferecer funcionalidade personalizada é simples para o desenvolvedor.

## Experimente os componentes principais

Se você quiser começar imediatamente a experimentar os Componentes principais, vá para a [Biblioteca de componentes](http://opensource.adobe.com/aem-core-wcm-components/library.html). A Biblioteca de componentes é uma demonstração on-line da versão atual da maioria dos componentes principais, que permite interagir com variações dos componentes, além de ver exemplos de saída HTML e JSON.

The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) also illustrates how the core components can be used.

## Componentes principais - Recursos principais {#core-components-core-features}

Os componentes principais são:

|  |  |
|--- |--- |
| Pré-configuráveis | Os modelos podem definir como os autores de página podem usá-los. |
| Versáteis | Os autores podem criar a maioria dos tipos de conteúdo com eles. |
| Fáceis de usar | Os autores podem criar a maioria dos tipos de conteúdo com eles. |
| Prontos para produção | Uso imediato! Eles são robustos, bem testados e funcionam bem. |
| Acessíveis | Eles estão em conformidade com o padrão WCAG 2.0, fornecem etiquetas ARIA e suportam a navegação pelo teclado. |
| Fáceis de usar | Os componentes implementam o Sistema de estilo e a marcação segue a nomeação de CSS do BEM. |
| Intuitivos para SEO | O resultado em HTML é semântico e fornece anotações de microdados schema.org. |
| Pronto para PWA/SPA/App | Seu resultado direcionado JSON também pode ser usado para renderização pelo cliente. |
| Extensíveis | Para cobrir as necessidades de personalização sem iniciar do zero, tudo pode ser estendido. |
| Origem aberta | Se algo não é como deveria ser, contribua com aprimoramentos no GitlHub (Licença Apache). |
| Versão | Os componentes principais não vão quebrar seu site ao melhorar coisas que poderiam afetá-lo. |
| [Localizados](localization.md) | A resolução de referência inteligente permite que certos componentes encontrem e renderizem conteúdos correspondentes localizados automaticamente |

## Componentes disponíveis {#available-components}

A versão atual dos Componentes principais apresenta os seguintes componentes:

* [Menu sanfonado](accordion.md)
* [Caminho](breadcrumb.md)
* [Botão](button.md)
* [Container](container.md)
* [Carrossel](carousel.md)
* [Fragmento do conteúdo](content-fragment-component.md)
* [Lista de fragmentos do conteúdo](content-fragment-list.md)
* [Download](download.md)
* [Incorporar](embed.md)
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
* [Página](page.md)
* [Busca rápida](quick-search.md)
* [Separador](separator.md)
* [Compartilhamento em mídia social](sharing.md)
* [Guias](tabs.md)
* [Texto](text.md)
* [Título](title.md)

>[!NOTE]
>
>Os Componentes principais não estão imediatamente disponíveis para os autores, a [equipe de desenvolvimento deve primeiro integrá-los ao seu ambiente](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) or in [design mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html).

>[!CAUTION]
>
>Algumas versões dos Componentes principais individuais podem ser compatíveis apenas com certas versões do AEM.
>
>Consulte a página de ajuda individual (ligada à lista anterior) para o componente específico para informações de compatibilidade ou referência das [Versões dos componentes principais](versions.md) para mais informações.

## Quando usar os componentes principais {#when-to-use-core-components}

Como os Componentes principais são totalmente novos e oferecem vários benefícios, é recomendável que os novos projetos AEM os usem. No caso dos projetos existentes, a migração deve fazer parte de um maior esforço de projeto, por exemplo, uma reformulação da marca ou uma reformulação global.

Para obter recomendações de uso específicas, consulte [Quando usar os componentes principais?](developing.md) no documento [Desenvolvendo componentes principais](developing.md).

## Visão geral da sessão Gems {#gems-session-overview}

Para obter uma introdução aos Componentes principais, os recursos que eles oferecem e como eles são aproveitados no AEM, verifique os Componentes principais do AEM [da sessão do AEM Gems.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[O Gems no Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) é uma série de soluções técnicas oferecidas por especialistas da Adobe. Esta série complementa a documentação do produto e de todos os outros canais técnicos, permitindo que os desenvolvedores entrem em contato e aprofundem o assunto.

## Desenvolver com os componentes principais {#developing-core-components}

Os componentes principais fornecem componentes básicos robustos e extensíveis que implementam vários padrões que permitem personalização fácil, desde o estilo simples até a reutilização avançada da funcionalidade. Consulte a documentação [de desenvolvimento dos Componentes](developing.md) principais para obter mais informações.

Comece a desenvolver o AEM Sites com componentes principais seguindo [este tutorial passo a passo.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

Não se esqueça de iniciar seu próprio projeto do AEM aproveitando o [AEM Project Archetype](overview.md) com os componentes principais mais recentes!

## Suporte para componentes principais {#core-components-support}

Os componentes principais são parte integrante do AEM e são suportados como estão, nos mesmos termos e condições como se fossem fornecidos como parte do Início rápido.

Como outros recursos do produto, a regra geral do fim da vida útil é:

* Os componentes são anunciados como obsoletos antes de serem removidos
* Logo que possível, eles serão removidos do lançamento do AEM após o anúncio.

Isso dá aos clientes pelo menos um ciclo de lançamento para migrar para a nova versão do componente, antes que o suporte termine.

A versão de cada componente indica claramente as versões do AEM suportadas. Quando o suporte para uma versão do AEM é interrompido, o mesmo acontece com o suporte dos Componentes principais para essa versão do AEM.

Para obter detalhes sobre o suporte às personalizações de componentes, consulte a página [Personalizando componentes principais](customizing.md) da versão relevante dos componentes principais.

## Suporte aos componentes da fundação {#foundation-component-support}

Como os Componentes da Fundação serviram de base para tantas versões de desenvolvimento de projetos, eles continuarão a ser apoiados num futuro previsível.

Entretanto, a ênfase de desenvolvimento da Adobe foi transferida para os Componentes principais e novos recursos serão adicionados a eles, enquanto [quase todos os Componentes básicos foram descontinuados com o AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) e somente correções de erros serão feitas nos Componentes de fundação a partir de agora.
