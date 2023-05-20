---
title: Componente de Texto de formulário (v1)
description: O componente de Texto de formulário, dos Componentes principais, permite a entrada do texto de formulário para envio.
index: n
role: Architect, Developer, Admin, User
exl-id: d6fbc596-cb42-4478-8a3c-aa5aead3be0a
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 100%

---

# Componente de Texto de formulário (v1) {#form-text-component-v}

O componente de Texto de formulário, dos Componentes principais, permite a entrada do texto de formulário para envio.

## Uso {#usage}

O componente de Texto de formulário permite o envio de diferentes tipos de texto e deve ser usado junto com o [componente de Contêiner de formulário](form-container-v1.md).

O tipo de validação de texto, rótulos e mensagens de ajuda pode ser definido pelo editor de conteúdo na [caixa de diálogo de configuração](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do componente de Texto de formulário, introduzido originalmente com a versão 1.0.0 dos Componentes principais, com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do componente de Texto de formulário.

| Versão do AEM | Componente de Texto de formulário (v1) |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do componente de Texto de formulário.
>
>Para obter detalhes sobre a versão atual do componente de Texto de formulário, consulte o documento [Componente de Texto de formulário](/help/components/forms/form-text.md).

## Exemplo de saída do componente {#sample-component-output}

O exemplo a seguir foi retirado do [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=pt-BR).

### Captura de tela {#screenshot}

![](/help/assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
     <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
     <div class="cmp cmp-form-field aem-GridColumn aem-GridColumn--default--12">
   <div class="form-group">
       <label for="form-text-978484744">How many pieces of toast would you like?</label>
          <input type="number" id="form-text-978484744" name="pieces">
   </div>
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
                "text": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/text",
                  "name": "piecesOfToast",
                  "jcr:title": "How many pieces of toast would you like?",
                  "type": "number",
                  "rows": "2"
                }
              },
              ":itemsOrder": [
                "text"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para mais informações.

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o tipo de texto a ser inserido, bem como valores e rótulos padrão.

### Principal {#main}

![](/help/assets/chlimage_1-23.png)

* **Restrição** - O tipo de texto a ser inserido e em relação ao qual será validado

   * **Texto**
   * **Área de texto**
   * **Email**
   * **Telefone**
   * **Data**
   * **Número**
   * **Senha**

* **Linhas de texto** - Número de linhas a serem exibidas na área de texto (exibidas somente quando a **Restrição** é definida como **Área de texto**)

* **Rótulo** - O rótulo que será exibido para o campo
* **Impedir o rótulo de ser exibido** - Necessário se o rótulo for necessário somente para fins de acessibilidade e não imprimir nenhuma informação visual adicional sobre o campo
* **Nome do elemento** - O nome do campo enviado com os dados de formulário
* **Valor** - Valor padrão pré-preenchido no campo

### Sobre {#about}

![](/help/assets/chlimage_1-24.png)

* **Mensagem de ajuda** - Uma dica para o usuário sobre o que pode ser inserido no campo
* **Exibir mensagem de ajuda como espaço reservado** -Para exibir a mensagem de ajuda dentro da entrada de formulário quando ela estiver vazia e não focalizada

### Restrições {#constraints}

![](/help/assets/chlimage_1-25.png)

* **Mensagem de restrição**

   * Se o valor não validar o Tipo escolhido, a mensagem será exibida como uma dica de ferramenta ao enviar o formulário
   * Não exibido para tipos de restrição de **Texto** e **Área de Texto**

* **Obrigatório** - Caso selecionado, o usuário deve preencher um valor antes de enviar o formulário
* **Tornar somente leitura** - Caso selecionado, o usuário não poderá modificar o valor do campo

## Caixa de diálogo de design {#design-dialog}

Não há caixa de diálogo de design para o componente Texto de formulário.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Texto do formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

Todo o projeto dos Componentes principais pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
