---
title: Componente oculto do formulário (v1)
description: O componente principal Formulário oculto do componente permite a exibição de um campo oculto.
index: n
translation-type: tm+mt
source-git-commit: fe8a121520000ffd56ae3347469590e89121eaf0
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 2%

---


# Componente oculto do formulário (v1) {#form-hidden-component-v}

O componente principal Formulário oculto do componente permite a exibição de um campo oculto.

## Uso {#usage}

O Componente principal de formulário oculto permite que a criação de campos ocultos transmita informações sobre a página atual para AEM e é destinado a ser usado junto com o [componente de container de formulário](form-container-v1.md).

As propriedades de campo podem ser definidas pelo editor de conteúdo na caixa de diálogo [configure](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do componente Form Hidden, originalmente introduzido com a versão 1.0.0 dos Componentes principais com a AEM 6.3.

A tabela a seguir lista a compatibilidade de v1 do componente Oculto do formulário.

| Versão do AEM | Componente oculto do formulário v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do componente Oculto do formulário.
>
>Para obter detalhes sobre a versão atual do Componente oculto do formulário, consulte o documento [Componente oculto do formulário](/help/components/forms/form-hidden.md).

## Exemplo de saída do componente {#sample-component-output}

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

### JSON {#json}

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
>A exportação JSON dos Componentes principais exige a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md#release-history-and-compatibility) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina os parâmetros do campo oculto.

![](/help/assets/chlimage_1-26.png)

* **Nome**  - O nome do campo, que é enviado com os dados do formulário
* **Valor**  - O valor do campo, que é submetido com os dados do formulário
* **Identificador**  - o identificador deve ser exclusivo na página e pode ser usado para vincular scripts a esse campo de formulário

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo de design para o componente Form Hidden.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente oculto do formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

Todo o projeto de componentes principais pode ser baixado do GitHub.

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
