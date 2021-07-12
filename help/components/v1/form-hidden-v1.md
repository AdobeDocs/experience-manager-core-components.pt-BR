---
title: Componente oculto do formulário (v1)
description: O componente Componente principal Formulário oculto permite a exibição de um campo oculto.
index: n
role: Architect, Developer, Admin, User
exl-id: 8e30dac0-5b4b-4fc7-af99-5791c98c90bf
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 2%

---

# Componente oculto do formulário (v1) {#form-hidden-component-v}

O componente Componente principal Formulário oculto permite a exibição de um campo oculto.

## Uso {#usage}

O Componente principal de formulário oculto permite que a criação de campos ocultos transmita informações sobre a página atual de volta ao AEM e deve ser usado junto com o [componente do contêiner de formulário](form-container-v1.md).

As propriedades do campo podem ser definidas pelo editor de conteúdo na caixa de diálogo [configurar](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente de formulário oculto, originalmente introduzido com a versão 1.0.0 dos Componentes principais com a AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do Componente de formulário oculto.

| Versão do AEM | Componente oculto do formulário v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do Componente de formulário oculto.
>
>Para obter detalhes sobre a versão atual do Componente de formulário oculto, consulte o documento [Componente oculto do formulário](/help/components/forms/form-hidden.md).

## Saída de componente de exemplo {#sample-component-output}

A amostra a seguir é retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
  <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
   <div class="visible aem-GridColumn aem-GridColumn--default--12">
    <input type="hidden" id="ghostToast" name="Invisible Toast" value="ghostToast">
   </div>
 </form>
</div>
```

### JSON  {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "hidden": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/hidden",
                  "name": "Invisible Toast",
                  "id": "ghostToast",
                  "value": "ghostToast"
                }
              },
              ":itemsOrder": [
                "hidden"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md#release-history-and-compatibility) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo configurar permite que o autor de conteúdo defina os parâmetros do campo oculto.

![](/help/assets/chlimage_1-26.png)

* **Nome**  - O nome do campo, que é enviado com os dados do formulário
* **Valor**  - O valor do campo, que é enviado com os dados do formulário
* **Identificador**  - o identificador deve ser exclusivo na página e pode ser usado para vincular scripts a este campo de formulário

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo de design para o componente Formulário oculto.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de formulário oculto [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

O projeto de componentes principais inteiro pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
