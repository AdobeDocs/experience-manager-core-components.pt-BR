---
title: Componente do botão de formulário (v1)
seo-title: Componente do botão de formulário (v1)
description: 'null'
seo-description: O componente principal Formulário oculto do componente permite a inclusão de um campo oculto em um formulário.
uuid: 0525e70f-294f-4d35-bf96-fc0e4ec225e9
content-type: referência
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: ea06acc0-38e2-4252-ac29-07332835b7c4
disttype: dist5
gnavtheme: light
groupsectionnavitems: não
hidemerchandisingbar: herdar
hidepromocomponent: herdar
modalsize: 426x240
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Form Button Component (v1){#form-button-component-v}

O componente de Botão de formulário do componente principal permite a inclusão de um campo de botão em um formulário para acionar uma ação.

## Uso {#usage}

O componente de Botão de formulário do componente principal permite a criação do campo de botão, geralmente para acionar a submissão do formulário e deve ser usado junto com o componente [de contêiner de](form-container.md)formulário.

As propriedades do botão podem ser definidas pelo editor de conteúdo na caixa de diálogo [](form-button-v1.md#main-pars_title)configurar.

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
>Para obter detalhes sobre a versão atual do Componente do botão de formulário, consulte o documento Componente [do botão de](form-button.md) formulário.

## Exemplo de saída de componente {#sample-component-output}

A seguir está uma amostra retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/chlimage_1-48.png)

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
>A exportação JSON dos Componentes principais exige a versão 1.1.0 dos Componentes principais. Consulte as informações de [compatibilidade dos Componentes principais v1](versions.md#main-pars_title_236368006) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina os parâmetros do botão.

![](assets/chlimage_1-49.png)

* **Tipo**
   * **Imagem**
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

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.
