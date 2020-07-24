---
title: Suporte AMP para os componentes principais
description: Os componentes principais suportam AMP - Páginas móveis aceleradas
translation-type: tm+mt
source-git-commit: 905096d909d4fbf624152ba3b5cbc1d80637245f
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---


# Suporte AMP para os componentes principais {#amp-support}

Desde a [versão 2.11.0](/help/versions.md) dos Componentes principais, o [AMP - Accelerated Mobile Pages](https://developers.google.com/amp) - é totalmente compatível.

Este documento fornece uma visão geral de como a AMP é suportada, bem como de como ativá-la para seus sites. No entanto, para obter todos os detalhes técnicos, consulte a documentação do desenvolvedor do [GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## O que é AMP? {#what-is-amp}

Accelerated Mobile Pages ou AMP é uma estrutura de código aberto originalmente projetada pelo Google para otimizar páginas para navegação móvel. Geralmente, as páginas AMP carregam muito mais rapidamente do que as páginas da Web padrão, oferecendo melhores experiências móveis.

## AMP nos componentes principais {#amp-in-core-components}

O suporte para AMP nos Componentes principais é [totalmente configurável.](#enabling-amp) As versões AMP das páginas podem ser fornecidas exclusivamente, juntamente com as versões HTML padrão, ou de modo algum.

Os Componentes principais usam `amp` como seletor Sling para renderizar uma página AMP. Por exemplo, `example.html` renderizaria a página normal e `example.amp.html` seria a versão AMP.

### Requisitos {#requirements}

Ao usar a AMP com os componentes principais, a principal diferença é que a AMP exige que todos os CSS sejam incorporados no `<head>` elemento e otimizados.

Para suportar isso, um componente de página personalizado é usado, que carrega apenas o CSS específico da AMP para componentes presentes na página.

Para obter mais requisitos e detalhes técnicos, consulte a documentação do desenvolvedor do [GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

### Uso da AMP nos componentes principais {#using-amp}

Projetos individuais podem decidir se devem ou não alavancar a AMP. Na verdade, como a AMP e as páginas HTML padrão podem ser entregues em paralelo, um projeto pode optar por usar a AMP somente em determinadas páginas do projeto.

### Instalação do suporte AMP {#installing-amp}

Como a AMP é opcional, ela é fornecida como uma extensão para os Componentes principais.

* Para o AEM como um projeto Cloud Service, a extensão fica automaticamente disponível.
* Para projetos no local e AMS, a extensão deve ser explicitamente instalada ao instalar os Componentes principais.

Depois que a extensão for instalada, o autor do componente deverá simplesmente apontar os supertipos do componente para os da extensão.

### Ativação da AMP para páginas {#enabling-amp}

Para habilitar a AMP para uma página, o Modo **** AMP deve estar selecionado na Política [de página.](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/templates.html#editingatemplatepagepolicies)

![Opções de política de página AMP](/help/assets/amp-policy.png)

* **Sem AMP** - A página é entregue somente como HTML padrão.
* **AMP** emparelhada - A página é entregue como AMP e HTML.
* **Somente** AMP - A página é entregue somente como AMP.

As configurações AMP de uma página também podem ser substituídas nas Propriedades [da](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/authoring/editing-page-properties.html) página para uma página individual.

![Propriedades da página AMP](/help/assets/amp-page-properties.png)

* **Herdar do modelo** de página - Esse é o valor padrão, que permite que a configuração seja retirada da política do modelo de página.
* **Sem AMP** - A página é entregue somente como HTML padrão.
* **AMP** emparelhada - A página é entregue como AMP e HTML.
* **Somente** AMP - A página é entregue somente como AMP.
