---
title: Componente do botão de formulário (v1)
description: O componente principal Formulário oculto do componente permite a inclusão de um campo oculto em um formulário.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Form Button Component (v1) {#form-button-component-v}

O componente de Botão de formulário do componente principal permite a inclusão de um campo de botão em um formulário para acionar uma ação.

## Uso {#usage}

O componente de Botão de formulário do componente principal permite a criação do campo de botão, geralmente para acionar a submissão do formulário e deve ser usado junto com o componente [de contêiner de](form-container-v1.md)formulário.

As propriedades do botão podem ser definidas pelo editor de conteúdo na caixa de diálogo [](#configure-dialog)configurar.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente do botão de formulário, originalmente introduzido com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade de v1 do Componente do botão de formulário.

| Versão do AEM | Componente do botão de formulário v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do Componente do botão de formulário.
>
>Para obter detalhes sobre a versão atual do Componente do botão de formulário, consulte o documento Componente [do botão de](/help/components/forms/form-button.md) formulário.

## Exemplo de saída de componente {#sample-component-output}

A seguir está uma amostra retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>A exportação JSON dos Componentes principais exige a versão 1.1.0 dos Componentes principais. Consulte as informações de [compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina os parâmetros do botão.

![](/help/assets/chlimage_1-49.png)

* **Tipo**
   * **Botão**
   * **Enviar**

* **Título** - O texto exibido no botão
   * Se nenhum fornecido, o padrão será o tipo de botão

* **Nome** - o nome do botão, que é enviado com os dados do formulário
* **Valor** - O valor do botão, que é enviado com os dados do formulário

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo de design para o componente Botão de formulário.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do botão de formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

Todo o projeto de componentes principais pode ser baixado do GitHub.

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.
