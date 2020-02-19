---
title: Componente de texto do formulário (v1)
description: O componente principal de texto do formulário do componente permite a entrada do texto do formulário para envio.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Form Text Component (v1) {#form-text-component-v}

O componente principal de texto do formulário do componente permite a entrada do texto do formulário para envio.

## Uso {#usage}

O Componente de texto do formulário permite o envio de diferentes tipos de texto e se destina a ser usado junto com o componente [de contêiner do](form-container-v1.md)formulário.

O tipo de validação de texto, rótulos e mensagens de ajuda podem ser definidos pelo editor de conteúdo na caixa de diálogo [](#configure-dialog)configurar.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente de texto do formulário, originalmente introduzido com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade de v1 do Componente de texto do formulário.

| Versão do AEM | Componente de texto do formulário v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do Componente de texto do formulário.
>
>Para obter detalhes sobre a versão atual do Componente de texto do formulário, consulte o documento Componente [de texto do](/help/components/forms/form-text.md) formulário.

## Exemplo de saída de componente {#sample-component-output}

A seguir está uma amostra retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>A exportação JSON dos Componentes principais exige a versão 1.1.0 dos Componentes principais. Consulte as informações de [compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o tipo de texto a ser inserido, bem como valores e rótulos padrão.

### Principal {#main}

![](/help/assets/chlimage_1-23.png)

* **Restrição** - O tipo de texto a ser inserido e será validado em relação

   * **Texto**
   * **Área de texto**
   * **E-mail**
   * **Telefone**
   * **Data**
   * **Número**
   * **Senha**

* **Linhas** de texto - Número de linhas a serem exibidas na área de texto (exibidas somente quando **Restrição** estiver definida como Área **de** texto)

* **Rótulo** - O rótulo que será exibido para o campo
* **Ocultar a etiqueta de ser exibida** - Necessário se a etiqueta for exigida somente para fins de acessibilidade e não fornecer nenhuma informação visual adicional sobre o campo
* **Nome** do elemento - o nome do campo enviado com os dados do formulário
* **Valor** - Valor padrão pré-preenchido no campo

### Sobre {#about}

![](/help/assets/chlimage_1-24.png)

* **Mensagem** de ajuda - uma dica para o usuário do que pode ser inserido no campo
* **Exibir mensagem de ajuda como espaço reservado** - Para exibir a mensagem de ajuda dentro da entrada do formulário quando ela estiver vazia e não focalizada

### Restrições {#constraints}

![](/help/assets/chlimage_1-25.png)

* **Mensagem de restrição**

   * Se o valor não validar o Tipo escolhido, a mensagem será exibida como uma dica de ferramenta ao enviar o formulário
   * Não exibido para tipos de restrição de **Texto** e Área **de** texto

* **Obrigatório** - se selecionado, o usuário deve preencher um valor antes de enviar o formulário
* **Tornar somente** leitura - Se selecionado, o usuário não poderá modificar o valor do campo

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo de design para o componente de Texto do formulário.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de texto do formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

Todo o projeto de componentes principais pode ser baixado do GitHub.

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.
