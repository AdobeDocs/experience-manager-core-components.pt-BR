---
title: Componente Botão de formulário (v1)
description: O componente Formulário Oculto, dos Componentes Principais, possibilita a inclusão de um campo oculto em um formulário.
index: n
role: Architect, Developer, Admin, User
exl-id: 2c06a942-7ac5-4847-9d11-7bbcd0ea51bd
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '342'
ht-degree: 100%

---

# Componente Botão de formulário (v1) {#form-button-component-v}

O componente Botão de formulário, dos Componentes Principais, permite a inclusão de um campo de botão em um formulário para acionar uma ação.

## Uso {#usage}

O componente Botão de formulário, dos Componentes Principais, permite a criação de um campo de botão, muitas vezes para acionar o envio do formulário. Ele deve ser usado com o [componente Contêiner de formulário](form-container-v1.md).

As propriedades do botão podem ser definidas pelo editor de conteúdo na [caixa de diálogo de configuração](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a versão v1 do componente Botão de formulário, introduzido originalmente com a versão 1.0.0 dos Componentes Principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do componente Botão de Formulário.

| Versão do AEM | Componente Botão de Formulário (v1) |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do componente Botão de formulário.
>
>Para mais detalhes sobre a versão atual do componente Botão de formulário, consulte o documento [Componente Botão de Formulário](/help/components/forms/form-button.md).

## Exemplo de saída do componente {#sample-component-output}

O exemplo a seguir foi retirado do [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=pt-BR).

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
>A exportação JSON dos Componentes Principais requer a versão 1.1.0 dos Componentes Principais. Consulte as [informações de compatibilidade dos Componentes Principais v1](/help/versions.md) para mais informações.

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina os parâmetros do botão.

![](/help/assets/chlimage_1-49.png)

* **Tipo**
   * **Botão**
   * **Enviar**

* **Título** - O texto exibido no botão
   * Se nenhum for fornecido, o padrão será o tipo de botão

* **Nome** - O nome do botão, que é enviado com os dados de formulário
* **Valor** - O valor do botão, que é enviado com os dados de formulário

## Caixa de diálogo de design {#design-dialog}

Não há caixa de diálogo de design para o componente Botão de formulário.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Botão de Formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

Todo o projeto de Componentes Principais pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes Principais podem ser encontrados na [documentação do desenvolvedor dos Componentes Principais](/help/developing/overview.md).
