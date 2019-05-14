---
title: Componente do botão de formulário (v 1)
seo-title: Componente do botão de formulário (v 1)
description: 'null'
seo-description: O componente Oculto formulário de componente principal permite a inclusão de um campo oculto em um formulário.
uuid: 0525 e 70 f -294 f -4 d 35-bf 96-fc 0 e 4 ec 225 e 9
content-type: referência
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: ea 06 acc 0-38 e 2-4252-ac 29-07332835 b 7 c 4
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


# Componente do botão de formulário (v 1){#form-button-component-v}

O componente Botão de formulário de formulário principal permite a inclusão de um campo de botão em um formulário para acionar uma ação.

## Uso {#usage}

O componente de botão de formulário principal do componente permite a criação de um campo de botão, geralmente para acionar o envio do formulário e deve ser usado junto com o [componente do contêiner de formulário](form-container.md).

As propriedades do botão podem ser definidas pelo editor de conteúdo na caixa de diálogo [Configurar](form-button-v1.md#main-pars_title).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v 1 do componente de botão de formulário originalmente introduzido com a versão 1.0.0 dos componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v 1 do componente do botão de formulário.

| Versão do AEM | Componente do botão Form v 1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve v 1 do componente do botão de formulário.
>
>Para obter detalhes sobre a versão atual do componente do botão de formulário, consulte o [documento Componente](form-button.md) do botão de formulário.

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>A exportação JSON dos componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade para Componentes principais v 1](versions.md#main-pars_title_236368006) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo defina os parâmetros do botão.

![](assets/chlimage_1-49.png)

* **Tipo**
   * **Imagem**
   * **Enviar**

* **Título** - o texto exibido no botão
   * Se nenhum for o padrão, o tipo de botão será definido como padrão

* **Nome** - o nome do botão, que é enviado com os dados do formulário
* **Valor** - O valor do botão, que é enviado com os dados do formulário

## Caixa de diálogo de design {#design-dialog}

Não há diálogo de design para o componente do Botão de formulário.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente do botão de formulário [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

Todo o projeto de componentes principais pode ser baixado de github.

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).
