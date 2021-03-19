---
title: Componente de compartilhamento em redes sociais
description: O Componente principal de compartilhamento social é um widget de compartilhamento de Pinterest e Facebook.
role: Arquiteto, Desenvolvedor, Administrador, Praticante de negócios
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 7%

---


# Componente de compartilhamento em redes sociais{#social-sharing-component}

O Componente principal de compartilhamento social é um widget de compartilhamento de Pinterest e Facebook.

## Uso {#usage}

O Componente de compartilhamento em redes sociais adiciona links do Facebook e do Pinterest para a página. Geralmente é incluído em cabeçalhos ou rodapés da página.

Diferentemente de outros componentes, as configurações do Componente de compartilhamento em redes sociais são feitas pelo autor do modelo por meio de [Propriedades da página inicial](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) e pelo autor de conteúdo por meio de [Propriedades da página](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de compartilhamento em redes sociais é a v1, que foi introduzida com a versão 1.0.0 dos Componentes principais, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente e as versões de AEM com as quais as versões do componente são compatíveis.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de compartilhamento em redes sociais e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_sharing).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de compartilhamento [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Editar Caixa de Diálogo {#edit-dialog}

![Caixa de diálogo de edição do Componente de compartilhamento](/help/assets/sharing-edit.png)

* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

Como o compartilhamento requer cabeçalhos de página especiais, qualquer compartilhamento deve ser ativado no nível da página. Portanto, para o autor de conteúdo, opções de edição adicionais para o componente de compartilhamento estão disponíveis na guia de compartilhamento, as [propriedades da página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Caixa de diálogo Design {#design-dialog}

Como o compartilhamento requer cabeçalhos de página especiais, qualquer compartilhamento deve ser ativado no nível da página. Portanto, para o autor do modelo, as opções de design para o componente de compartilhamento estão disponíveis por meio das [propriedades da página inicial](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).
