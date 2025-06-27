---
title: Componente Formulário oculto (v1)
description: O componente Formulário oculto, dos Componentes principais, possibilita a exibição de um campo oculto.
index: n
role: Architect, Developer, Admin, User
exl-id: 8e30dac0-5b4b-4fc7-af99-5791c98c90bf
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '316'
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

A documentação técnica mais recente sobre o componente Formulário oculto [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

Todo o projeto dos Componentes principais pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
