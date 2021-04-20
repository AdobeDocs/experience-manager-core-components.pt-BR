---
title: Componente do botão de formulário (v1)
description: O componente Componente principal Formulário oculto permite a inclusão de um campo oculto em um formulário.
index: n
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 3%

---


# Componente do botão de formulário (v1) {#form-button-component-v}

O componente do botão de formulário do componente principal permite a inclusão de um campo de botão em um formulário para acionar uma ação.

## Uso {#usage}

O componente de Botão de formulário do componente principal permite a criação de campo de botão, muitas vezes para acionar o envio do formulário e deve ser usado junto com o [componente de contêiner de formulário](form-container-v1.md).

As propriedades do botão podem ser definidas pelo editor de conteúdo na caixa de diálogo [configurar](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente do botão de formulário, introduzido originalmente com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do Componente do botão de formulário.

| Versão do AEM | Componente do botão de formulário v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do Componente do botão de formulário.
>
>Para obter detalhes sobre a versão atual do Componente do botão de formulário, consulte o documento [Componente do botão de formulário](/help/components/forms/form-button.md).

## Saída de componente de exemplo {#sample-component-output}

A amostra a seguir é retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](/help/assets/chlimage_1-48.png)

### HTML {#html}

```
<div class="cmp cmp-button aem-GridColumn aem-GridColumn--default--12">
    <div class="cmp cmp-button">
        <button type="BUTTON" class="btn btn-action btn-primary" name="loveToast" value="ILoveToast">
            Click here if you love toast!
        </button>
    </div>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "button": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/button",
                  "name": "loveToast",
                  "jcr:title": "Click here if you love toast!",
                  "type": "submit",
                  "value": "ILoveToast"
                }
              },
              ":itemsOrder": [
                "button"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo configurar permite que o autor de conteúdo defina os parâmetros do botão.

![](/help/assets/chlimage_1-49.png)

* **Tipo**
   * **Botão**
   * **Enviar**

* **Título**  - O texto exibido no botão
   * Se nenhum fornecido, o padrão será o tipo de botão

* **Nome**  - O nome do botão, que é enviado com os dados do formulário
* **Valor**  - O valor do botão, que é enviado com os dados do formulário

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo de design para o componente Botão de formulário.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do botão de formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

O projeto de componentes principais inteiro pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
