---
title: Configurações Sling sensíveis ao contexto e componentes principais
description: Os Componentes principais aproveitam as configurações sensíveis ao contexto do Sling para determinados recursos
translation-type: tm+mt
source-git-commit: 11e2c6da0fa93084b601437fd45fd65dd8d73231
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# Configurações Sling sensíveis ao contexto e componentes principais {#sling-context-aware-configurations}

As configurações sensíveis ao contexto são um recurso do Sling e são configurações relacionadas a um recurso de conteúdo ou a uma árvore de recursos e são aproveitadas pelos Componentes principais para permitir configurações de todo o site.

## Configurações Sling sensíveis ao contexto {#context-aware-configurations}

Seu site pode precisar de configurações diferentes para regiões de sites diferentes, por exemplo, onde alguns parâmetros podem ser compartilhados, o que exige herança para contextos aninhados e valores de fallback globais. AEM aproveita as configurações sensíveis ao contexto Sling, que permitem essa possibilidade.

Para obter detalhes sobre configurações em AEM, [consulte a documentação do Navegador de configurações e configurações.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/configurations.html)

## Usar nos componentes principais {#core-components}

Vários recursos dos Componentes principais aproveitam as configurações sensíveis ao contexto. Todas essas configurações estão localizadas no seguinte nó:

* `/conf/<my-site>/sling:configs/<my-configuration>`

As configurações individuais dependem do componente ou do recurso específico. Os recursos dos Componentes principais que usam configurações sensíveis ao contexto são:

* [Componente do visualizador de PDF](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Camada de dados do cliente Adobe](/help/developing/data-layer/overview.md#installation-activation)
* [Suporte AMP](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
