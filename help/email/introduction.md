---
title: Introdução aos Componentes principais de email
description: Crie conteúdo atraente de email usando a flexibilidade dos Componentes principais de email e forneça-o com o poder do Adobe Campaign.
role: Architect, Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 100%

---


# Introdução aos Componentes principais de email {#email-core-components-introduction}

Crie conteúdo atraente de email usando a flexibilidade dos Componentes principais de email e forneça-o com o poder do Adobe Campaign.

## Visão geral {#overview}

Os Componentes principais de email são criados na mesma base poderosa dos Componentes principais. Eles permitem a criação simples e flexível de conteúdo de email ao arrastar e soltar, o que pode ser entregue ao seu público usando o poder do Adobe Campaign.

## Benefícios {#benefits}

Os emails fazem parte da experiência da marca e da jornada do cliente. Com os Componentes principais do email, os autores podem criar conteúdo de email a partir do AEM, oferecendo uma experiência consistente com a marca e aumentando, assim, a velocidade do conteúdo.

* Assim como a criação de páginas com os Componentes principais, os Componentes principais de email permitem que os autores montem emails sem conhecimento técnico e garantem que sigam as diretrizes de marca.
* A capacidade de reutilizar ativos e conteúdo também incentiva os autores a seguir as diretrizes da marca e otimizar o processo de criação de conteúdo.

## Recursos {#features}

* Os Componentes principais de email são baseados nos [Componentes principais,](/help/introduction.md) e, por conseguinte, também são compatíveis com [Modelos editáveis](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR) e [Sistema de estilo.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=pt-BR)
* Existem [dez componentes prontos para produção otimizados por email](#components) para criar conteúdo de email.
* Os componentes principais de email fornecem personalização avançada graças à inserção de [variáveis do Adobe Campaign](campaign-variables.md) na maioria dos campos de caixa de diálogo.
* O [componente de Segmentação](/help/email/components/segmentation.md) flexível permite a segmentação avançada do seu conteúdo.
* Os Componentes principais de email fornecem saída de HTML amigável para email graças ao [inliner de estilos de CSS](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation), [ao inliner de atributo de HTML](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner), e [ao sanitizer de HTML](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing).
* Você pode criar conteúdo de email em qualquer lugar abaixo de `/content`.
* Os Componentes principais do email são de [código aberto.](https://github.com/adobe/aem-core-email-components)

## Requisitos {#requirements}

Os Componentes principais de email têm os seguintes requisitos.

| AEM | Adobe Campaign | Componentes principais  |
|---|---|---|
| AEM 6.5.14.0+<br>Local ou para AMS | Adobe Campaign Classic<br>Adobe Campaign Standard | [Versão 2.21.2](/help/versions.md)+ |

>[!NOTE]
>
>Como as integrações do Adobe Campaign não são compatíveis com o AEM as a Cloud Service, os Componentes principais de email também não são compatíveis com o AEM as a Cloud Service.

## Os componentes de email {#components}

A versão atual dos Componentes principais de email apresenta os seguintes componentes:

* [Página](components/page.md)
* [Contêiner](components/container.md)
* [Título](components/title.md)
* [Texto](components/text.md)
* [Imagem](components/image.md)
* [Botão](components/button.md)
* [Teaser](components/teaser.md)
* [Fragmento de experiência](components/experience-fragment.md)
* [Fragmento de conteúdo](components/content-fragment.md)
* [Segmentação](components/segmentation.md)

## Instalação e uso {#installation-usage}

Consulte o documento [Usar os Componentes principais de email](using.md) para obter detalhes sobre como instalar os Componentes principais de email.
