---
title: Componente oculto do formulário (v 1)
seo-title: Componente oculto do formulário (v 1)
description: O componente de Formulário de componente principal permite a exibição de um campo oculto.
seo-description: O componente de Formulário de componente principal permite a exibição de um campo oculto.
uuid: f 5005346-def 5-4 e 1 f -8 f 93-e 4 cfc 67 a 9329
content-type: referência
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: d 35 f 4 e 71-ec 7 f -4128-9123-b 997 dbb 5 f 0 cf
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Componente oculto do formulário (v 1){#form-hidden-component-v}

O componente de Formulário de componente principal permite a exibição de um campo oculto.

## Uso {#usage}

O componente oculto do formulário de componente principal permite que a criação de campos ocultos passe informações sobre a página atual de volta para o AEM e seja usada com o componente do contêiner [de formulário](form-container.md).

As propriedades de campo podem ser definidas pelo editor de conteúdo na caixa de diálogo [Configurar](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve v 1 do componente oculto do formulário, originalmente introduzido com a versão 1.0.0 dos componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v 1 do componente Oculto do formulário.

| Versão do AEM | Formulário oculto do componente v 1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve v 1 do componente oculto do formulário.
>
>Para obter detalhes sobre a versão atual do componente Oculto Formulário, consulte o [documento Componente](form-hidden.md) oculto do formulário.

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>A exportação JSON dos componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade para Componentes principais v 1](versions.md#release-history-and-compatibility) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo defina os parâmetros do campo oculto.

![](assets/chlimage_1-26.png)

* **Nome** - o nome do campo, que é enviado com os dados do formulário
* **Valor** - O valor do campo, que é enviado com os dados do formulário
* **Identificador** - o identificador deve ser exclusivo na página e pode ser usado para vincular scripts a esse campo de formulário

## Caixa de diálogo de design {#design-dialog}

Não há diálogo de design para o componente Formulário oculto.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente oculto do formulário [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

Todo o projeto de componentes principais pode ser baixado de github.

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).
