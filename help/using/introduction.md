---
title: Introdução aos componentes principais
seo-title: Introdução aos componentes principais
description: 'Componentes principais foram introduzidos para fornecer componentes básicos robustos e extensíveis, com base na tecnologia mais recente e práticas recomendadas. '
seo-description: 'Componentes principais foram introduzidos para fornecer componentes básicos robustos e extensíveis, com base na tecnologia mais recente e práticas recomendadas. '
uuid: b 815 c 7 d 1-fbb 0-4480-bd 23-42606 ff 8 b 1 eb
contentOwner: Usuário
content-type: referência
topic-tags: introdução
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: c 44 bb 0 d 7-5 d 91-4659-878 e-a 0658 fe 29 aa 2
translation-type: tm+mt
source-git-commit: 63e75079e41d3091ca57bfc3129e700675bf4939

---


# Introdução aos componentes principais{#core-components-introduction}

No Adobe Experience Manager, os componentes são os elementos estruturais que constituem o conteúdo das páginas criadas. Os componentes sempre foram um elemento fundamental da experiência do AEM, tornando a criação da página simples, mas poderosa para o autor e o desenvolvimento de componentes flexíveis e extensível para o desenvolvedor.

Os Componentes principais foram introduzidos para fornecer componentes básicos e extensíveis, construídos com base na tecnologia mais recente e práticas recomendadas, além de aderir às diretrizes de acessibilidade e são compatíveis com o padrão WCAG 2.0 AA. Os componentes principais tornam a criação de página mais flexível e personalizável, e ampliá-los para oferecer funcionalidade personalizada é simples para o desenvolvedor.

## Testar os componentes principais

Se você quiser começar a testar os Componentes principais, acesse a Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library.html). A Biblioteca de componentes é uma exibição on-line da versão atual da maioria dos Componentes principais, permitindo interagir com variações dos componentes, bem como ver a amostra de HTML e JSON.

The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) also illustrates how the core components can be used.

## Componentes principais - Recursos principais {#core-components-core-features}

Os Componentes principais são:

|  |  |
|--- |--- |
| Pré-configurável | Os modelos podem definir como os autores de página podem usá-los. |
| Versátil | Os autores podem criar mais tipos de conteúdo com eles. |
| Fácil de usar | Os autores podem criar e gerenciar com eficiência o conteúdo com eles. |
| Production-Ready | Uso utilizável! Eles são robustos, bem testados e apresentam bom desempenho. |
| Acessível | Elas seguem o padrão WCAG 2.0, fornecem rótulos ARIA e oferecem suporte à navegação do teclado. |
| Fácil de estilo | Os componentes implementam o Sistema de estilo e a marcação segue o nome de CSS de IBM. |
| Compatível com SEO | A saída HTML é semântica e fornece anotações de microdados schema.org. |
| PWA/SPA/App Ready | A saída JSON simplificada também pode ser usada para renderização no cliente. |
| Extensible | Para cobrir necessidades personalizadas, mas sem começar do zero, tudo pode ser estendido. |
| Abrir fonte | Se algo não for como deveria, contribui com melhorias no github (Apache License). |
| Controle de versão | Os componentes principais não quebrarão seu site ao aprimorar o que pode impactar você. |

## Componentes disponíveis {#available-components}

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

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) or in [design mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html).

>[!CAUTION]
>
>Algumas versões de Componentes principais individuais podem ser compatíveis apenas com determinadas versões do AEM.
>
>Consulte a página de ajuda individual (vinculada à lista anterior) para o componente específico para obter informações de compatibilidade ou consultar o [documento Principais versões](versions.md) dos componentes para obter mais informações.

## Quando usar componentes principais {#when-to-use-core-components}

Como os Componentes principais são totalmente novos e oferecem vários benefícios, recomendamos que os novos projetos do AEM sejam usados. Para projetos existentes, uma migração deve ser parte de um esforço de projeto maior, por exemplo, uma reformulação ou uma atualização geral.

Para obter recomendações específicas de uso, consulte [Quando usar os componentes principais?](developing.md) no documento Componentes do [Desenvolvimento](developing.md) principais.

## Visão geral da sessão Gems {#gems-session-overview}

Para obter uma introdução aos Componentes principais, os recursos que eles oferecem e como eles são aproveitados no AEM, confira os Componentes principais do [AEM Gems Session AEM.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[O Gems no Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) é uma série de soluções técnicas oferecidas pelos especialistas da Adobe. Esta série complementa a documentação do produto e de todos os outros canais técnicos, permitindo que os desenvolvedores entrem em contato e se aprofunde em um tópico específico.

## Tutorial do desenvolvedor WKND {#wknd-developer-tutorial}

Comece a desenvolver o AEM Sites com os Componentes principais seguindo [este tutorial passo a passo.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Suporte aos componentes principais {#core-components-support}

Os Componentes principais são parte integrante do AEM e são compatíveis com os mesmos termos e condições que se fossem entregues como parte do Início rápido.

Como outros recursos do produto, a regra geral do fim da vida útil é:

* Os componentes são anunciados pela primeira vez antes de serem removidos
* No máximo, são removidas da versão do AEM após o anúncio.

Isso proporciona aos clientes pelo menos um ciclo de lançamento para se mover para a nova versão do componente antes de terminar o suporte.

A versão de cada componente declara claramente as versões do AEM que ele suporta. Quando o suporte for interrompido para uma versão do AEM, então o suporte aos Componentes principais dessa versão do AEM será compatível.

Para obter detalhes sobre a compatibilidade com as personalizações de componentes, consulte a página [Personalizar componentes](customizing.md) principais da Versão dos componentes principais relevantes.

## Suporte para componentes de base {#foundation-component-support}

Como os Componentes básicos serviram como base de tanta desenvolvimento de projeto em várias versões, eles continuarão a ser suportados no futuro próximo.

No entanto, a ênfase de desenvolvimento da Adobe mudou para os Componentes principais e os novos recursos serão adicionados a eles, enquanto [quase todos os Componentes fundamentais foram descontinuados com o AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) e somente correções de erros serão feitas nos Componentes de fundação que estiverem avançando.
