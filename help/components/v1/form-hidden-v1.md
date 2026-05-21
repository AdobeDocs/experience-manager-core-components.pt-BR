---
title: Componente Formulário oculto (v1)
description: O componente Formulário oculto, dos Componentes principais, possibilita a exibição de um campo oculto.
index: false
role: Developer, Admin, User
exl-id: 8e30dac0-5b4b-4fc7-af99-5791c98c90bf
TQID: https://experienceleague.adobe.com/rMf4285S77F8hsmwcgo24Bd39eDl13nozM6KZFCuPqY
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 344
ht-degree: 100%

---

# Componente Formulário oculto (v1) {#form-hidden-component-v}

O componente Formulário oculto, dos Componentes principais, possibilita a exibição de um campo oculto.

## Uso {#usage}

O componente Formulário oculto, dos Componentes principais, possibilita a criação de campos ocultos para transmitir informações sobre a página atual de volta ao AEM. Ele deve ser usado com o [componente Contêiner de Formulário](form-container-v1.md).

As propriedades do campo podem ser definidas pelo editor de conteúdo na [caixa de diálogo de configuração](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a versão v1 do componente Formulário oculto, originalmente introduzido com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da versão v1 do componente Formulário oculto.

| Versão do AEM | Componente Formulário oculto v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a versão v1 do componente Formulário oculto.
>
>Para mais detalhes sobre a versão atual do componente Formulário oculto, consulte o documento [Componente Formulário oculto](/help/components/forms/form-hidden.md).

## Exemplo de saída do componente {#sample-component-output}

O exemplo a seguir foi retirado do [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=pt-BR).

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
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md#release-history-and-compatibility) para mais informações.

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina os parâmetros do campo oculto.

![](/help/assets/chlimage_1-26.png)

* **Nome** - O nome do campo, que é enviado com os dados de formulário
* **Valor** - O valor do campo, que é enviado com os dados de formulário
* **Identificador** - O identificador deve ser exclusivo na página e pode ser usado para vincular scripts nesse campo de formulário

## Caixa de diálogo de design {#design-dialog}

Não há caixa de diálogo de design para o componente Formulário oculto.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Formulário Oculto [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

Todo o projeto dos Componentes principais pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
