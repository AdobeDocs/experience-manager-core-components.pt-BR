---
title: Componente oculto do formulário
description: O componente principal Formulário oculto do componente permite a exibição de um campo oculto.
translation-type: tm+mt
source-git-commit: 60df01ca9efe59b67bad57610d04496a2cdded9e

---


# Componente oculto do formulário{#form-hidden-component}

O componente principal Formulário oculto do componente permite a exibição de um campo oculto.

## Uso {#usage}

O componente principal Oculto do formulário permite que a criação de campos ocultos transmita informações sobre a página atual para o AEM e deve ser usado junto com o componente [do contêiner de](form-container.md)formulário.

As propriedades de campo podem ser definidas pelo editor de conteúdo na caixa de diálogo [](form-hidden.md)configurar.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente oculto do formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como um serviço em nuvem |
|--- |--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível | Compatível |
| [v1](form-hidden-v1.md) | Compatível | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

A seguir está uma amostra retirada de [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

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

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente oculto do formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina os parâmetros do campo oculto.

![](assets/chlimage_1-26.png)

* **Nome** O nome do campo, que é enviado com os dados do formulário
* **Valor** O valor do campo, que é submetido com os dados do formulário
* **Identificador** O identificador deve ser exclusivo na página e pode ser usado para vincular scripts a esse campo de formulário

Como o componente Form Oculto normalmente não tem atributos visíveis, o espaço reservado do componente no editor exibe os valores dos campos **Nome** e **Valor** se eles forem atribuídos para ajudar o autor a identificar o componente Form Oculto apropriado.

![](assets/screenshot_2018-10-19at094927.png)

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo de design para o componente Form Hidden.
