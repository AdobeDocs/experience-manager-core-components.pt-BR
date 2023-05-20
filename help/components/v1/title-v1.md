---
title: Componente de Título (v1)
description: O componente de Título, dos Componentes principais, é um componente de cabeçalho de seção que apresenta edição no local.
index: n
role: Architect, Developer, Admin, User
exl-id: 79549ac0-82f2-4ea0-9cce-d534d0b47b5c
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 100%

---

# Componente de Título (v1) {#title-component-v}

O componente de Título, dos Componentes principais, é um componente de cabeçalho de seção que apresenta edição no local.

## Uso {#usage}

O componente de Título deve ser usado como o título ou cabeçalho de uma seção de conteúdo.

Os níveis de cabeçalho disponíveis podem ser definidos pelo autor do modelo na [caixa de diálogo design](#design-dialog). O editor de conteúdo pode selecionar a partir dos níveis de cabeçalho disponíveis na [caixa de diálogo de edição](#edit-dialog). Para maior conveniência, a edição simples no local do texto do cabeçalho também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do componente de Título, originalmente introduzido com a versão 1.0.0 dos Componentes principais, com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do componente de Título.

| Versão do AEM | Componente de Título v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a versão 1 do componente de Título.
>
>Para detalhes sobre a versão atual do componente de Título, consulte o documento [Componente de Título](/help/components/title.md).

## Exemplo de saída do componente {#sample-component-output}

O exemplo a seguir foi retirado do [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=pt-BR).

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
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para mais informações.

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo defina o texto do título, e selecione o nível do cabeçalho.

>[!NOTE]
>
>Um valor vazio para o título fará com que o título da página seja exibido.

![](/help/assets/chlimage_1-91.png)

O editor local também pode ser usado para editar o texto do componente de Título.

![](/help/assets/chlimage_1-37.png)

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o nível de cabeçalho padrão que os componentes de título terão quando criados pelos autores de conteúdo.

![](/help/assets/chlimage_1-92.png)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Título [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title).

Todo o projeto dos Componentes principais pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
