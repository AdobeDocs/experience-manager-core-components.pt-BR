---
title: Introdução aos Componentes principais
description: 'Os componentes principais foram introduzidos para fornecer componentes básicos robustos e extensíveis, baseados na tecnologia mais recente e nas práticas recomendadas. '
translation-type: tm+mt
source-git-commit: fe8a121520000ffd56ae3347469590e89121eaf0

---


# Introdução aos componentes principais{#core-components-introduction}

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas. Os componentes sempre foram um elemento fundamental da experiência do AEM, tornando a criação de páginas simples, mas poderosa para o autor e o desenvolvimento de componentes flexíveis e extensíveis para o desenvolvedor.

Os componentes principais foram introduzidos para fornecer componentes básicos robustos e extensíveis, baseados na tecnologia mais recente e nas práticas recomendadas, além de seguir as diretrizes de acessibilidade e serem compatíveis com o padrão WCAG 2.0 AA. Os componentes principais tornam a criação de páginas mais flexível e personalizável, e sua extensão para oferecer funcionalidade personalizada é simples para o desenvolvedor.

## Experimente os componentes principais

Se você quiser começar imediatamente a experimentar os Componentes principais, vá para a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library). A Biblioteca de componentes é uma demonstração on-line da versão atual da maioria dos componentes principais, que permite interagir com variações dos componentes, além de ver exemplos de saída HTML e JSON.

O tutorial [](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) WKND também ilustra como os componentes principais podem ser usados.

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
| [Localizados](get-started/localization.md) | A resolução de referência inteligente permite que determinados componentes localizem e renderizem o conteúdo correspondente automaticamente |

## Componentes disponíveis {#available-components}

A versão atual dos Componentes principais apresenta os seguintes componentes:

* [Menu sanfonado](components/accordion.md)
* [Caminho](components/breadcrumb.md)
* [Botão](components/button.md)
* [Container](components/container.md)
* [Carrossel](components/carousel.md)
* [Fragmento do conteúdo](components/content-fragment-component.md)
* [Lista de fragmentos do conteúdo](components/content-fragment-list.md)
* [Download](components/download.md)
* [Incorporar](components/embed.md)
* [Fragmento de experiência](components/experience-fragment.md)
* [Botão de formulário](components/forms/form-button.md)
* [Contêineres de formulário](components/forms/form-container.md)
* [Formulário oculto](components/forms/form-hidden.md)
* [Opções de formulário](components/forms/form-options.md)
* [Texto do formulário](components/forms/form-text.md)
* [Imagem](components/image.md)
* [Navegação de idiomas](components/language-navigation.md)
* [Lista](components/list.md)
* [Navegação](components/navigation.md)
* [Página](components/page.md)
* [Busca rápida](components/quick-search.md)
* [Separador](components/separator.md)
* [Compartilhamento em mídia social](components/sharing.md)
* [Guias](components/tabs.md)
* [Texto](components/text.md)
* [Título](components/title.md)

>[!NOTE]
>
>Os Componentes principais não estão imediatamente disponíveis para os autores, a [equipe de desenvolvimento deve primeiro integrá-los ao seu ambiente](get-started/using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Algumas versões dos Componentes principais individuais podem ser compatíveis apenas com certas versões do AEM.
>
>Consulte a página de ajuda individual (ligada à lista anterior) para o componente específico para informações de compatibilidade ou referência das [Versões dos componentes principais](versions.md) para mais informações.

## Quando usar os componentes principais {#when-to-use-core-components}

Como os Componentes principais são totalmente novos e oferecem vários benefícios, é recomendável que os novos projetos AEM os usem. No caso dos projetos existentes, a migração deve fazer parte de um maior esforço de projeto, por exemplo, uma reformulação da marca ou uma reformulação global.

Para obter recomendações de uso específicas, consulte [Quando usar os componentes principais?](developing/overview.md#when-to-use-the-core-components) no documento [Desenvolvendo componentes principais](developing/overview.md).

## Visão geral da sessão Gems {#gems-session-overview}

Para obter uma introdução aos Componentes principais, os recursos que eles oferecem e como eles são aproveitados no AEM, verifique os Componentes principais do AEM [da sessão do AEM Gems.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[O Gems no Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) é uma série de soluções técnicas oferecidas por especialistas da Adobe. Esta série complementa a documentação do produto e de todos os outros canais técnicos, permitindo que os desenvolvedores entrem em contato e aprofundem o assunto.

## Desenvolver com os componentes principais {#developing-core-components}

Os componentes principais fornecem componentes básicos robustos e extensíveis que implementam vários padrões que permitem personalização fácil, desde o estilo simples até a reutilização avançada da funcionalidade. Consulte a documentação [de desenvolvimento dos Componentes](developing/overview.md) principais para obter mais informações.

Comece a desenvolver o AEM Sites com componentes principais seguindo [o tutorial da WKND.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

Não se esqueça de iniciar seu próprio projeto do AEM aproveitando o [AEM Project Archetype](developing/archetype/overview.md) com os componentes principais mais recentes!

## Suporte para componentes principais {#core-components-support}

Os componentes principais são parte integrante do AEM e são suportados como estão, nos mesmos termos e condições como se fossem fornecidos como parte do Início rápido.

Como outros recursos do produto, a regra geral do fim da vida útil é:

* Os componentes são anunciados como obsoletos antes de serem removidos
* Logo que possível, eles serão removidos do lançamento do AEM após o anúncio.

Isso dá aos clientes pelo menos um ciclo de lançamento para migrar para a nova versão do componente, antes que o suporte termine.

A versão de cada componente indica claramente as versões do AEM suportadas. Quando o suporte para uma versão do AEM é interrompido, o mesmo acontece com o suporte dos Componentes principais para essa versão do AEM.

Para obter detalhes sobre o suporte às personalizações de componentes, consulte a página [Personalizando componentes principais](developing/customizing.md) da versão relevante dos componentes principais.

## Suporte aos componentes da fundação {#foundation-component-support}

Como os Componentes da Fundação serviram de base para tantas versões de desenvolvimento de projetos, eles continuarão a ser apoiados num futuro previsível.

Entretanto, a ênfase de desenvolvimento da Adobe foi transferida para os Componentes principais e novos recursos serão adicionados a eles, enquanto [quase todos os Componentes básicos foram descontinuados com o AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) e somente correções de erros serão feitas nos Componentes de fundação a partir de agora.
