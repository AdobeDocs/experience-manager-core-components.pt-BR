---
title: Introdução aos Componentes principais de email
description: Crie conteúdo atraente de e-mail usando a flexibilidade dos Componentes principais de e-mail e forneça-o com o poder do Adobe Campaign.
role: Architect, Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 9%

---


# Introdução aos Componentes principais de email {#email-core-components-introduction}

Crie conteúdo atraente de e-mail usando a flexibilidade dos Componentes principais de e-mail e forneça-o com o poder do Adobe Campaign.

## Visão geral {#overview}

Os Componentes principais de email são criados na mesma base poderosa dos Componentes principais. Eles permitem a criação simples e flexível de arrastar e soltar de conteúdo de email, que pode ser entregue ao seu público usando o poder do Adobe Campaign.

## Benefícios {#benefits}

Os emails fazem parte da experiência da marca e da jornada do cliente. Com os Componentes principais do email, os autores podem criar conteúdo de email a partir do AEM, oferecendo uma experiência com marca consistente e aumentando, assim, a velocidade do conteúdo.

* Assim como a criação de páginas com os Componentes principais, os Componentes principais de email permitem que os autores reúnam emails sem conhecimento técnico e garantem que sigam as diretrizes de marca.
* A capacidade de reutilizar ativos e conteúdo também incentiva os autores a seguir as diretrizes de marca e otimizar o processo de criação de conteúdo.

## Recursos {#features}

* Os Componentes principais de email são baseados na variável [Componentes principais,](/help/introduction.md) e, por conseguinte, [Modelos editáveis](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR) e [Sistema de estilos.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=pt-BR)
* Existem [dez componentes prontos para produção otimizados por email](#components) para criar conteúdo de email.
* Os Componentes principais de email fornecem personalização avançada graças à inserção de [Variáveis do Adobe Campaign](campaign-variables.md) na maioria dos campos de diálogo.
* A flexibilidade [Componente de segmentação](/help/email/components/segmentation.md) O permite a segmentação avançada do seu conteúdo.
* Os Componentes principais de email fornecem saída de HTML amigável para email graças ao [estilos CSS em invólucro,](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation) [o atributo HTML inliner,](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner) e [o HTML sanitizer.](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing)
* Você pode criar conteúdo de email em qualquer lugar abaixo `/content`.
* Os Componentes principais do email são [código aberto.](https://github.com/adobe/aem-core-email-components)

## Requisitos {#requirements}

Os Componentes principais de email têm os seguintes requisitos.

| AEM | Adobe Campaign | Componentes principais  |
|---|---|---|
| AEM 6.5.14.0+<br>No local ou no AMS | Adobe Campaign Classic<br>Adobe Campaign Standard | [Versão 2.21.2](/help/versions.md)+ |

>[!NOTE]
>
>Como as integrações do Adobe Campaign não são compatíveis com AEM as a Cloud Service, os Componentes principais de email também não são compatíveis com AEM as a Cloud Service.

## Os componentes de email {#components}

A versão atual dos Componentes principais de email apresenta os seguintes componentes.

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

Consulte a [Usar os componentes principais de email](using.md) documento para obter detalhes sobre como instalar os Componentes principais de email.
