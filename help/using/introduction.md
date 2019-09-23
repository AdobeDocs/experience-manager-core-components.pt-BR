---
title: Introdução aos componentes principais
seo-title: Introdução aos componentes principais
description: 'Os componentes principais foram introduzidos para fornecer componentes básicos robustos e extensíveis, baseados na tecnologia mais recente e nas práticas recomendadas. '
seo-description: 'Os componentes principais foram introduzidos para fornecer componentes básicos robustos e extensíveis, baseados na tecnologia mais recente e nas práticas recomendadas. '
uuid: b815c7d1-fbb0-4480-bd23-42606ff8b1eb
contentOwner: Usuário
content-type: referência
topic-tags: introdução
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: c44bb0d7-5d91-4659-878e-a0658fe29aa2
translation-type: tm+mt
source-git-commit: b6fbef1cff2908533df6573cd3a92266857ba93f

---


# Introdução aos componentes principais{#core-components-introduction}

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas. Os componentes sempre foram um elemento fundamental da experiência do AEM, tornando a criação de páginas simples, mas poderosa para o autor e o desenvolvimento de componentes flexíveis e extensíveis para o desenvolvedor.

Os componentes principais foram introduzidos para fornecer componentes básicos robustos e extensíveis, baseados na tecnologia mais recente e nas práticas recomendadas, além de seguir as diretrizes de acessibilidade e serem compatíveis com o padrão WCAG 2.0 AA. Os componentes principais tornam a criação de páginas mais flexível e personalizável, e sua extensão para oferecer funcionalidade personalizada é simples para o desenvolvedor.

## Experimente os componentes principais

Se você quiser começar imediatamente experimentando os Componentes principais, vá para a Biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library.html)componentes. A Biblioteca de componentes é uma demonstração on-line da versão atual da maioria dos componentes principais, que permite interagir com variações dos componentes, além de ver exemplos de saída HTML e JSON.

The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) also illustrates how the core components can be used.

## Componentes principais - Recursos principais {#core-components-core-features}

Os componentes principais são:

|  |  |
|--- |--- |
| Pré-configurável | Os modelos podem definir como os autores de página podem usá-los. |
| Versátil | Os autores podem criar a maioria dos tipos de conteúdo com eles. |
| Fácil de usar | Os autores podem criar e gerenciar conteúdo com eficiência. |
| Pronto para produção | Uso imediato! Eles são robustos, bem testados e funcionam bem. |
| Acessível | Eles estão em conformidade com o padrão WCAG 2.0, fornecem etiquetas ARIA e suportam a navegação pelo teclado. |
| Estilo fácil | Os componentes implementam o Sistema de estilo e a marcação segue a nomeação de CSS do BEM. |
| SEO amigável | A saída HTML é semântica e fornece anotações de microdados schema.org. |
| PWA/SPA/App Ready | A saída JSON otimizada também pode ser usada para renderização no cliente. |
| Extensível | Para cobrir necessidades personalizadas, mas sem começar do zero, tudo pode ser estendido. |
| Fonte aberta | Se algo não for como deveria ser, contribua com melhorias no GitHub (Licença Apache). |
| Versionado | Os componentes principais não quebrarão seu site ao melhorar coisas que podem afetar você. |
| [Localizado](localization.md) | A resolução de referência inteligente permite que determinados componentes localizem e renderizem automaticamente o conteúdo localizado correspondente |

## Componentes disponíveis {#available-components}

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

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) or in [design mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html).

>[!CAUTION]
>
>Algumas versões dos componentes principais individuais podem ser compatíveis apenas com determinadas versões do AEM.
>
>Consulte a página de ajuda individual (vinculada na lista anterior) do componente específico para obter informações sobre compatibilidade ou consulte o documento Versões [dos componentes](versions.md) principais para obter mais informações.

## Quando usar os componentes principais {#when-to-use-core-components}

Como os Componentes principais são totalmente novos e oferecem vários benefícios, é recomendável que os novos projetos AEM os usem. No caso dos projetos existentes, a migração deve fazer parte de um maior esforço de projeto, por exemplo, uma reformulação da marca ou uma reformulação global.

Para obter recomendações de uso específicas, consulte [Quando usar os componentes principais?](developing.md) no documento [Desenvolvendo componentes](developing.md) principais.

## Visão geral da sessão Gems {#gems-session-overview}

Para obter uma introdução aos Componentes principais, os recursos que eles oferecem e como eles são aproveitados no AEM, verifique os Componentes principais do AEM [AEM da sessão do AEM Gems.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[O Gems no Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) é uma série de soluções técnicas oferecidas por especialistas da Adobe. Esta série complementa a documentação do produto e de todos os outros canais técnicos, permitindo que os desenvolvedores entrem em contato e aprofundem o assunto.

## Tutorial do desenvolvedor WKND {#wknd-developer-tutorial}

Comece a desenvolver o AEM Sites com componentes principais seguindo [este tutorial passo a passo.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Suporte para componentes principais {#core-components-support}

Os componentes principais são parte integrante do AEM e são suportados como estão, nos mesmos termos e condições como se fossem fornecidos como parte do Início rápido.

Como outros recursos do produto, a regra geral do fim da vida útil é:

* Os componentes são anunciados como obsoletos antes de serem removidos
* Logo que possível, eles serão removidos do lançamento do AEM após o anúncio.

Isso dá aos clientes pelo menos um ciclo de lançamento para migrar para a nova versão do componente, antes que o suporte termine.

A versão de cada componente indica claramente as versões do AEM suportadas. Quando o suporte para uma versão do AEM é interrompido, o mesmo acontece com o suporte dos Componentes principais para essa versão do AEM.

Para obter detalhes sobre o suporte às personalizações de componentes, consulte a página [Personalizando componentes](customizing.md) principais da versão relevante dos componentes principais.

## Suporte ao componente básico {#foundation-component-support}

Como os Componentes da Fundação serviram de base para tantas versões de desenvolvimento de projetos, eles continuarão a ser apoiados num futuro previsível.

Entretanto, a ênfase de desenvolvimento da Adobe foi transferida para os Componentes principais e novos recursos serão adicionados a eles, enquanto [quase todos os Componentes básicos foram descontinuados com o AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) e somente correções de erros serão feitas nos Componentes básicos a partir de então.
