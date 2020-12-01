---
title: Suporte AMP para os componentes principais
description: Os componentes principais suportam AMP - Páginas móveis aceleradas
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---


# Suporte AMP para os componentes principais {#amp-support}

A partir de [versão 2.11.0](/help/versions.md) dos Componentes principais, [AMP - Accelerated Mobile Pages](https://developers.google.com/amp) - há suporte total.

Este documento fornece uma visão geral de como a AMP é suportada, bem como de como ativá-la para seus sites. No entanto, para obter todos os detalhes técnicos, consulte a documentação do [desenvolvedor do GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## O que é AMP? {#what-is-amp}

Accelerated Mobile Pages ou AMP é uma estrutura de código aberto originalmente projetada pelo Google para otimizar páginas para navegação móvel. Geralmente, as páginas AMP carregam muito mais rapidamente do que as páginas da Web padrão, oferecendo melhores experiências móveis.

## AMP nos componentes principais {#amp-in-core-components}

O suporte para AMP nos Componentes principais é [totalmente configurável.](#enabling-amp) As versões AMP das páginas podem ser fornecidas exclusivamente, juntamente com as versões HTML padrão, ou de modo algum.

Os Componentes principais usam `amp` como seletor Sling para renderizar uma página AMP. Por exemplo, `example.html` renderizaria a página normal e `example.amp.html` seria a versão AMP.

Projetos individuais podem decidir se devem ou não alavancar a AMP. Na verdade, como a AMP e as páginas HTML padrão podem ser entregues em paralelo, um projeto pode optar por usar a AMP somente em determinadas páginas do projeto.

## Introdução ao suporte da AMP em seu projeto {#getting-started}

Embora o suporte AMP tenha ofertas de grande flexibilidade, para começar a usá-lo rapidamente, são necessárias apenas algumas etapas simples:

1. Instale a extensão de suporte AMP, se necessário.
   * Para AEM como um Cloud Service, a extensão é disponibilizada automaticamente com os Componentes principais e nenhuma instalação é necessária.
   * Para projetos no local e AMS, a extensão deve ser explicitamente instalada ao instalar os Componentes principais.
1. Depois que a extensão AMP estiver instalada, o autor do componente deve simplesmente apontar os supertipos do componente para os da extensão.
1. [Ative o suporte ](#enabling-amp) AMP no nível do modelo ou em suas páginas individuais.
1. [Implante ](#css-requirements) CSS incorporado, conforme necessário.

### Habilitar AMP para páginas {#enabling-amp}

Para habilitar a AMP para uma página, o **AMP Mode** deve ser selecionado na [Política de Página.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer)

![Opções de política de página AMP](/help/assets/amp-policy.png)

* **Sem AMP**  - A página é entregue somente como HTML padrão.
* **AMP**  emparelhada - A página é entregue como AMP e HTML.
* **Somente**  AMP - A página é entregue somente como AMP.

As configurações AMP de uma página também podem ser substituídas em [Propriedades da página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) para uma página individual.

![Propriedades da página AMP](/help/assets/amp-page-properties.png)

* **Herdar do modelo**  de página - Esse é o valor padrão, que permite que a configuração seja retirada da política do modelo de página.
* **Sem AMP**  - A página é entregue somente como HTML padrão.
* **AMP**  emparelhada - A página é entregue como AMP e HTML.
* **Somente**  AMP - A página é entregue somente como AMP.

### Requisitos de CSS {#css-requirements}

Ao usar a AMP com os Componentes principais, a principal diferença é que a AMP exige que todos os [CSS sejam incorporados](including-clientlibs.md#inlining) no elemento `<head>`, bem como otimizados.

Para suportar isso, um componente de página personalizado é usado, que carrega apenas o CSS específico da AMP para componentes presentes na página.

Para obter mais requisitos e detalhes técnicos, consulte a [documentação do desenvolvedor do GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
