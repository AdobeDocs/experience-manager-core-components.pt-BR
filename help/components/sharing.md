---
title: Componente de compartilhamento em redes sociais
description: O Componente principal de compartilhamento em redes sociais é um widget de compartilhamento de Pinterest e Facebook.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Componente de compartilhamento em redes sociais{#social-sharing-component}

O Componente principal de compartilhamento em redes sociais é um widget de compartilhamento de Pinterest e Facebook.

## Uso {#usage}

O Componente de compartilhamento em redes sociais adiciona links de compartilhamento do Facebook e Pinterest à página. Geralmente é incluído nos cabeçalhos ou rodapés da página.

Diferentemente de outros componentes, as configurações do Componente de compartilhamento em redes sociais são feitas pelo autor do modelo por meio das propriedades [da Página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) inicial e pelo autor do conteúdo por meio das Propriedades [da](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html)página.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de compartilhamento em redes sociais é a v1, que foi introduzida com a versão 1.0.0 dos Componentes principais e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente e as versões AEM com as quais as versões do componente são compatíveis.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de compartilhamento em redes sociais e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_sharing)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de compartilhamento [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Edit Dialog {#edit-dialog}

![Caixa de diálogo de edição do Componente de compartilhamento](/help/assets/sharing-edit.png)

* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

Como o compartilhamento requer cabeçalhos de página especiais, qualquer compartilhamento deve ser ativado no nível da página. Portanto, para o autor do conteúdo, opções de edição adicionais para o componente de compartilhamento estão disponíveis na guia compartilhamento das propriedades [da](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html)página.

## Caixa de diálogo Design {#design-dialog}

Como o compartilhamento requer cabeçalhos de página especiais, qualquer compartilhamento deve ser ativado no nível da página. Portanto, para o autor do modelo, as opções de design para o componente de compartilhamento estão disponíveis nas propriedades [da página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)inicial.
