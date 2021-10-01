---
title: Suporte AMP para os Componentes principais
description: Os Componentes principais são compatíveis com AMP - Páginas para Dispositivos Móveis Aceleradas
role: Architect, Developer, Admin
exl-id: 1fd9b6b5-0e4d-48c7-8faa-42e0d4a6bbd0
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 96%

---

# Suporte AMP para os Componentes principais {#amp-support}

Desde a [versão 2.11.0](/help/versions.md) dos Componentes principais, as [AMP - Páginas para Dispositivos Móveis Aceleradas](https://developers.google.com/amp) - são totalmente compatíveis.

Este documento fornece uma visão geral de como as AMPs são compatíveis, bem como habilitá-las para seus sites. No entanto, para obter detalhes técnicos completos, consulte a [documentação do desenvolvedor do GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp).

## O que é AMP? {#what-is-amp}

Páginas para Dispositivos Móveis Aceleradas ou AMP é uma estrutura de código aberto originalmente projetada pelo Google para otimizar páginas para navegação móvel. As AMP normalmente carregam muito mais rapidamente do que as páginas padrão da Web, oferecendo melhores experiências móveis.

## AMP nos Componentes principais {#amp-in-core-components}

O suporte para AMP nos Componentes principais é [totalmente configurável.](#enabling-amp) As versões das AMP podem ser fornecidas exclusivamente, junto com as versões HTML padrão, ou não são fornecidas.

Os Componentes principais usam `amp` como um seletor do Sling para renderizar uma AMP. Por exemplo, `example.html` renderizaria a página normal e `example.amp.html` seria a versão de AMP.

Projetos individuais podem decidir se utilizam ou não AMP. Na verdade, como as AMP e as páginas HTML padrão podem ser entregues em paralelo, um projeto pode optar por usar AMP em apenas determinadas páginas do projeto.

## Introdução ao suporte AMP no seu projeto {#getting-started}

Embora o suporte a AMP ofereça muita flexibilidade, para começar a usá-las rapidamente, algumas etapas simples são necessárias:

1. Instale a extensão de suporte AMP, se necessário.
   * Para projetos do AEM as a Cloud Service, a extensão é disponibilizada automaticamente com os Componentes principais e nenhuma instalação é necessária.
   * Para projetos no local e do AMS, a extensão deve ser explicitamente instalada ao instalar os Componentes principais.
1. Quando a extensão AMP estiver instalada, o autor do componente deverá simplesmente apontar os supertipos de componentes para aqueles na extensão.
1. [Habilite o suporte AMP](#enabling-amp) no nível do modelo ou em suas páginas individuais.
1. [Implante o CSS incorporado](#css-requirements), conforme necessário.

### Ativar AMP para páginas {#enabling-amp}

Para habilitar AMP para uma página, o **Modo AMP** deve ser selecionado na [Política da página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer).

![Opções de política da página de AMP](/help/assets/amp-policy.png)

* **Sem AMP** - A página é entregue somente como HTML padrão.
* **AMP emparelhado** - A página é fornecida como AMP e HTML.
* **Somente AMP** - A página é entregue somente como AMP.

As configurações das AMP para uma página também podem ser substituídas nas [Propriedades da página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) para uma página individual.

![Propriedades da página de AMP](/help/assets/amp-page-properties.png)

* **Herdar do modelo da página** - Esse é o valor padrão, que permite que a configuração seja retirada da política do modelo da página.
* **Sem AMP** - A página é entregue somente como HTML padrão.
* **AMP emparelhado** - A página é fornecida como AMP e HTML.
* **Somente AMP** - A página é entregue somente como AMP.

### Requisitos de CSS {#css-requirements}

Ao usar AMP com os Componentes principais, a principal diferença é que a AMP requer que todos os [CSS sejam incorporados](including-clientlibs.md#inlining) no elemento `<head>`, bem como otimizados.

Para dar suporte a isso, um componente de página personalizado é usado, que carrega apenas o CSS específico de AMP para os componentes presentes na página.

>[!NOTE]
>
>Devido às limitações de design das AMP, a Adobe não é compatível com o uso da Grade responsiva com a versão das AMP da sua página.

Para mais requisitos e detalhes técnicos, consulte a [documentação do desenvolvedor do GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp).
