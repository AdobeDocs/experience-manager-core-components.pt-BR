---
title: Configurações sensíveis ao contexto do Sling e Componentes principais
description: Os Componentes principais usam as configurações sensíveis ao contexto do Sling para determinados recursos
role: Architect, Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: ht
source-wordcount: '198'
ht-degree: 100%

---

# Configurações sensíveis ao contexto do Sling e Componentes principais {#sling-context-aware-configurations}

As configurações sensíveis ao contexto são um [recurso do Sling](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html). São configurações relacionadas a um recurso de conteúdo ou a uma árvore de recursos e são aproveitadas pelos Componentes principais para permitir configurações em todo o site.

## Configurações Sling sensíveis ao contexto {#context-aware-configurations}

Seu site pode precisar de configurações diferentes para regiões de sites diferentes, por exemplo, onde alguns parâmetros podem ser compartilhados, o que requer herança para contextos aninhados e valores de fallback global. O AEM usa configurações sensíveis ao contexto do Sling, que permitem essa possibilidade.

Para obter detalhes sobre as configurações no AEM, [consulte as Configurações e a documentação do Navegador de configurações](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/configurations.html?lang=pt-BR).

## Uso dos Componentes principais {#core-components}

Vários recursos dos Componentes principais usam configurações sensíveis ao contexto. Todas essas configurações estão localizadas no seguinte nó:

* `/conf/<my-site>/sling:configs/<my-configuration>`

As configurações individuais dependem do componente ou do recurso específico. Os recursos dos Componentes principais que usam configurações sensíveis ao contexto são:

* [Componente Visualizador de PDF](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md#installation-activation)
* [Suporte ao AMP](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
