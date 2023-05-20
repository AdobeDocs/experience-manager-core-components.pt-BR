---
title: Componente de Compartilhamento em redes sociais
description: O componente de Compartilhamento em redes sociais, dos Componentes principais, é um dispositivo de compartilhamento no Facebook e Pinterest.
role: Architect, Developer, Admin, User
exl-id: 8bd53c76-da91-479b-b416-f978682a3d43
source-git-commit: 327c239b02e0aecee878784c918bfa98d960530e
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 100%

---

# Componente de Compartilhamento em redes sociais {#social-sharing-component}

O componente de Compartilhamento em redes sociais, dos Componentes principais, é um dispositivo de compartilhamento no Facebook e Pinterest.

>[!NOTE]
>
>O componente de compartilhamento em redes sociais foi descontinuado na [versão 2.18.0](/help/versions.md) dos Componentes principais.

## Uso {#usage}

O componente de Compartilhamento em redes sociais adiciona links de compartilhamento do Facebook e Pinterest à página. Geralmente é incluído em cabeçalhos ou rodapés da página.

Diferente de outros componentes, as configurações do componente de Compartilhamento em redes sociais são feitas pelo autor do modelo por meio de [Propriedades da página inicial](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR), e pelo autor de conteúdo por meio de [Propriedades da página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=pt-BR).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Compartilhamento em redes sociais é a v1, introduzida com a versão 1.0.0 dos Componentes principais, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente e as versões de AEM com as quais as versões do componente são compatíveis.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível  com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível, descontinuado | Compatível, descontinuado |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Compartilhamento [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

![Caixa de diálogo de edição do componente de Compartilhamento](/help/assets/sharing-edit.png)

* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

Como o compartilhamento requer cabeçalhos de página especiais, qualquer compartilhamento deve ser ativado no nível da página. Portanto, para o autor de conteúdo, opções de edição adicionais para o componente de Compartilhamento estão disponíveis na guia de compartilhamento, as [Propriedades da página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=pt-BR).

## Caixa de diálogo de design {#design-dialog}

Como o compartilhamento requer cabeçalhos de página especiais, qualquer compartilhamento deve ser ativado no nível da página. Portanto, para o autor do modelo, as opções de design para o componente de compartilhamento estão disponíveis por meio das [propriedades da página inicial](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR).
