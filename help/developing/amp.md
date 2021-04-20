---
title: Suporte AMP para os componentes principais
description: Os componentes principais são compatíveis com AMP - Accelerated Mobile Pages
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 1%

---


# Suporte AMP para os componentes principais {#amp-support}

Desde [versão 2.11.0](/help/versions.md) dos Componentes principais, [AMP - Accelerated Mobile Pages](https://developers.google.com/amp) - são totalmente compatíveis.

Este documento fornece uma visão geral de como o AMP é compatível, bem como como habilitá-lo para seus sites. No entanto, para obter detalhes técnicos completos, consulte a documentação do desenvolvedor do [GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## O que é o AMP? {#what-is-amp}

Accelerated Mobile Pages ou AMP é uma estrutura de código aberto originalmente projetada pelo Google para otimizar páginas para navegação móvel. As páginas AMP normalmente carregam muito mais rapidamente do que as páginas padrão da Web, oferecendo melhores experiências móveis.

## AMP nos Componentes principais {#amp-in-core-components}

O suporte para AMP nos Componentes principais é [totalmente configurável.](#enabling-amp) As versões do AMP de páginas podem ser fornecidas exclusivamente, junto com as versões HTML padrão, ou de modo algum.

Os Componentes principais usam `amp` como um seletor do Sling para renderizar uma página da AMP. Por exemplo, `example.html` renderizaria a página normal e `example.amp.html` seria a versão da AMP.

Os projetos individuais podem decidir se utilizam ou não a AMP. Na verdade, como as páginas AMP e HTML padrão podem ser entregues em paralelo, um projeto pode optar por usar a AMP em determinadas páginas do projeto.

## Introdução ao suporte ao AMP em seu projeto {#getting-started}

Embora o suporte à AMP ofereça muita flexibilidade, para começar a usá-lo rapidamente requer apenas algumas etapas simples:

1. Instale a extensão de suporte AMP, se necessário.
   * Para projetos do AEM as a Cloud Service, a extensão é disponibilizada automaticamente com os Componentes principais e nenhuma instalação é necessária.
   * Para projetos no local e do AMS, a extensão deve ser explicitamente instalada ao instalar os Componentes principais.
1. Quando a extensão AMP estiver instalada, o autor do componente deverá simplesmente apontar os supertipos de componentes para aqueles na extensão.
1. [Habilite o ](#enabling-amp) suporte ao AMP no nível do modelo ou em suas páginas individuais.
1. [Implante o ](#css-requirements) CSS incorporado, conforme necessário.

### Ativar o AMP para páginas {#enabling-amp}

Para habilitar a AMP para uma página, o **Modo AMP** deve ser selecionado na [Política de página.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer)

![Opções de política da página AMP](/help/assets/amp-policy.png)

* **Sem AMP**  - A página é entregue somente como HTML padrão.
* **AMP emparelhado**  - A página é fornecida como AMP e HTML.
* **AMP Somente**  - A página é entregue somente como AMP.

As configurações da AMP para uma página também podem ser substituídas nas [Propriedades da página](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) para uma página individual.

![Propriedades da página AMP](/help/assets/amp-page-properties.png)

* **Herdar do modelo da página**  - Esse é o valor padrão, que permite que a configuração seja retirada da política do modelo da página.
* **Sem AMP**  - A página é entregue somente como HTML padrão.
* **AMP emparelhado**  - A página é fornecida como AMP e HTML.
* **AMP Somente**  - A página é entregue somente como AMP.

### Requisitos de CSS {#css-requirements}

Ao usar a AMP com os Componentes principais, a principal diferença é que a AMP requer que todos os [CSS sejam incorporados](including-clientlibs.md#inlining) no elemento `<head>`, bem como otimizados.

Para dar suporte a isso, um componente de página personalizado é usado, que carrega apenas o CSS específico da AMP para os componentes presentes na página.

>[!NOTE]
>
>Devido às limitações de design da AMP, o Adobe não suporta o uso da Grade responsiva com a versão da AMP de sua página.

Para obter mais requisitos e detalhes técnicos, consulte a [documentação do desenvolvedor do GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
