---
title: Componente de título (v1)
description: O Componente principal de título do componente é um componente de cabeçalho de seção que apresenta edição no local.
index: n
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---


# Componente de título (v1) {#title-component-v}

O Componente principal de título do componente é um componente de cabeçalho de seção que apresenta edição no local.

## Uso {#usage}

O Componente de título deve ser usado como o título ou cabeçalho de uma seção de conteúdo.

Os níveis de cabeçalho disponíveis podem ser definidos pelo autor do modelo na caixa de diálogo [design](#design-dialog). O editor de conteúdo pode selecionar a partir dos níveis de cabeçalho disponíveis no [diálogo de edição](#edit-dialog). Para maior conveniência, a edição simples no local do texto do cabeçalho também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente de título, originalmente introduzido com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do Componente de título.

| Versão do AEM | Componente de título v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a versão 1 do Componente de título.
>
>Para obter detalhes sobre a versão atual do Componente de título, consulte o documento [Componente de título](/help/components/title.md).

## Saída de componente de exemplo {#sample-component-output}

A amostra a seguir é retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](/help/assets/chlimage_1-36.png)

### HTML {#html}

```
<div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
     <h2>Welcome! This is our finest equipment!</h2>
</div>
```

### JSON {#json}

```
"title": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/title",
              "jcr:title": "Welcome! This is our finest equipment!",
              "type": "h2"
            }
```

>[!NOTE]
>
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Editar Caixa de Diálogo {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo defina o texto do título, bem como selecione o nível do cabeçalho.

>[!NOTE]
>
>Um valor vazio para o título fará com que o título da página seja exibido.

![](/help/assets/chlimage_1-91.png)

O editor local também pode ser usado para editar o texto do componente de título.

![](/help/assets/chlimage_1-37.png)

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o nível de cabeçalho padrão que os componentes de título terão quando criados pelos autores de conteúdo.

![](/help/assets/chlimage_1-92.png)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de título [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title).

O projeto de componentes principais inteiro pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
