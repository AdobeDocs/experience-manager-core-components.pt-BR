---
title: Componente de texto do formulário (v1)
seo-title: Componente de texto do formulário (v1)
description: 'null'
seo-description: O componente principal de texto do formulário do componente permite a entrada do texto do formulário para envio.
uuid: 30123aba-57a8-4ed4-93cb-6a3d2edff9a7
content-type: referência
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: bd4e9930-4d81-49ae-a3d1-9a8740418dae
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Form Text Component (v1){#form-text-component-v}

The Core Component Form Text component allows the entry of form text for submission.

## Uso {#usage}

The Form Text Component allows for the submission of different types of text and is intended to be used along with the form container component.[](form-container.md)

The type of text validation, labels, and help messages can be defined by the content editor in the configure dialog.[](form-text-v1.md#main-pars_title)

## Version and Compatibility {#version-and-compatibility}

This document describes v1 of the Form Text Component, originally introduced with release 1.0.0 of the Core Components with AEM 6.3.

The following table lists the compatibility of v1 of the Form Text Component.

| Versão do AEM | Componente de texto do formulário v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>This document describes v1 of the Form Text Component.
>
>Para obter detalhes sobre a versão atual do Componente de texto do formulário, consulte o documento Componente [de texto do](form-text.md) formulário.

## Sample Component Output {#sample-component-output}

A seguir está uma amostra retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/chlimage_1-22.png)

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
>A exportação JSON dos Componentes principais exige a versão 1.1.0 dos Componentes principais. Consulte as informações de [compatibilidade dos Componentes principais v1](versions.md#main-pars_title_236368006) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o tipo de texto a ser inserido, bem como valores e rótulos padrão.

### Principal {#main}

![](assets/chlimage_1-23.png)

* **Restrição** - O tipo de texto a ser inserido e será validado em relação

   * **Text**
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

![](assets/chlimage_1-24.png)

* **Mensagem** de ajuda - uma dica para o usuário do que pode ser inserido no campo
* **Exibir mensagem de ajuda como espaço reservado** - Para exibir a mensagem de ajuda dentro da entrada do formulário quando ela estiver vazia e não focalizada

### Restrições {#constraints}

![](assets/chlimage_1-25.png)

* **Mensagem de restrição**

   * Se o valor não validar o Tipo escolhido, a mensagem será exibida como uma dica de ferramenta ao enviar o formulário
   * Não exibido para tipos de restrição de **Texto** e Área **de** texto

* **Obrigatório** - se selecionado, o usuário deve preencher um valor antes de enviar o formulário
* **Make read only - If selected the user cannot modify the value of the field**

## Design Dialog {#design-dialog}

There is no design dialog for the Form Text component.

## Technical Details {#technical-details}

A documentação técnica mais recente sobre o Componente de texto do formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

Todo o projeto de componentes principais pode ser baixado do GitHub.

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.
