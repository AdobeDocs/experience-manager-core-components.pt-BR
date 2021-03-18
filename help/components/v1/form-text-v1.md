---
title: Componente de texto do formulário (v1)
description: O componente de Texto do formulário do componente principal permite a entrada do texto do formulário para envio.
index: n
role: Arquiteto, Desenvolvedor, Administrador, Praticante de negócios
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 8%

---


# Componente de texto de formulário (v1) {#form-text-component-v}

O componente de Texto do formulário do componente principal permite a entrada do texto do formulário para envio.

## Uso {#usage}

O Componente de texto de formulário permite o envio de diferentes tipos de texto e deve ser usado junto com o [componente de contêiner de formulário](form-container-v1.md).

O tipo de validação de texto, rótulos e mensagens de ajuda pode ser definido pelo editor de conteúdo no [configurar diálogo](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente de texto de formulário, introduzido originalmente com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do Componente de texto de formulário.

| Versão do AEM | Componente de texto do formulário v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do Componente de texto de formulário.
>
>Para obter detalhes sobre a versão atual do Componente de texto de formulário, consulte o documento [Componente de texto de formulário](/help/components/forms/form-text.md).

## Saída de componente de exemplo {#sample-component-output}

A amostra a seguir é retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o tipo de texto a ser inserido, bem como valores e rótulos padrão.

### Principal {#main}

![](/help/assets/chlimage_1-23.png)

* **Restrição**  - O tipo de texto a ser inserido e será validado em relação a

   * **Texto**
   * **Área de texto**
   * **E-mail**
   * **Telefone**
   * **Data**
   * **Número**
   * **Senha**

* **Linhas de texto**  - Número de linhas a serem exibidas na área de texto (exibidas somente quando a  **** Restrição é definida como Área de  **texto**)

* **Rótulo**  - O rótulo que será exibido para o campo
* **Ocultar a exibição do rótulo**  - Necessário se o rótulo for necessário somente para fins de acessibilidade e não imprimir nenhuma informação visual adicional sobre o campo
* **Nome do elemento**  - O nome do campo que é enviado com os dados do formulário
* **Valor**  - Valor padrão pré-preenchido no campo

### Sobre {#about}

![](/help/assets/chlimage_1-24.png)

* **Mensagem de ajuda**  - Uma dica para o usuário do que pode ser inserido no campo
* **Exibir mensagem de ajuda como espaço reservado**  - Para exibir a mensagem de ajuda dentro da entrada do formulário quando estiver vazia e não focalizada

### Restrições {#constraints}

![](/help/assets/chlimage_1-25.png)

* **Mensagem de restrição**

   * Se o valor não validar o Tipo escolhido, a mensagem será exibida como uma dica de ferramenta ao enviar o formulário
   * Não exibido para tipos de restrição **Text** e **Área de Texto**

* **Obrigatório**  - Se selecionado, o usuário deve preencher um valor antes de enviar o formulário
* **Tornar somente leitura**  - Se selecionado, o usuário não poderá modificar o valor do campo

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo de design para o componente de Texto do formulário.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de texto do formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

O projeto de componentes principais inteiro pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
