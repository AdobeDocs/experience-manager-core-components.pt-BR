---
title: Configurações sensíveis ao contexto do Sling e Componentes principais
description: Os Componentes principais usam as configurações sensíveis ao contexto do Sling para determinados recursos
role: Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
TQID: https://experienceleague.adobe.com/jCBeHjuqLJzIxggeZxpusUkv9ZAyE-Ktr5N-gakWK18
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 257
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

As configurações individuais dependem do componente ou do recurso específico. Os recursos dos componentes principais que usam configurações sensíveis ao contexto incluem:

* [O componente de página](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/page/v3/page#loading-of-context-aware-cssjs) depende de configuração sensível ao contexto ao renderizar tags `link`, `script` e `meta`.
* [Componente de Visualizador de PDF](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md#installation-activation)
* [Suporte ao AMP](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
