---
title: Componente de texto de formulário (v 1)
seo-title: Componente de texto de formulário (v 1)
description: 'null'
seo-description: O componente de Texto do formulário de componente principal permite a entrada do texto do formulário para envio.
uuid: 30123 aba -57 a 8-4 ed 4-93 cb -6 a 3 d 2 edff 9 a 7
content-type: referência
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: bd 4 e 9930-4 d 81-49 ae-a 3 d 1-9 a 8740418 dae
index: n
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de texto de formulário (v 1){#form-text-component-v}

O componente de Texto do formulário de componente principal permite a entrada do texto do formulário para envio.

## Uso {#usage}

O Componente de texto de formulário permite o envio de diferentes tipos de texto e deve ser usado junto com o componente do contêiner [de formulário](form-container.md).

O tipo de validação de texto, rótulos e mensagens de ajuda pode ser definido pelo editor de conteúdo na caixa de diálogo [Configurar](form-text-v1.md#main-pars_title).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve v 1 do Componente de texto de formulário, originalmente introduzido com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v 1 do Componente de texto de formulário.

| Versão do AEM | Componente de texto de formulário v 1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve v 1 do componente de texto de formulário.
>
>Para obter detalhes sobre a versão atual do Componente de texto de formulário, consulte o [documento Componente](form-text.md) de texto de formulário.

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>A exportação JSON dos componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade para Componentes principais v 1](versions.md#main-pars_title_236368006) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo defina o tipo de texto a ser inserido, bem como valores e rótulos padrão.

### Principal {#main}

![](assets/chlimage_1-23.png)

* **Restrição** - o tipo de texto a ser inserido e será validado em comparação a

   * **Text**
   * **Área de texto**
   * **E-mail**
   * **Telefone**
   * **Data**
   * **Número**
   * **Senha**

* **Linhas de texto** - O número de linhas a serem exibidas na área de texto (somente exibido quando **a Restrição** está definida como **Área de texto**)

* **Rótulo** - O rótulo que será exibido para o campo
* **Ocultar a etiqueta a ser exibida** - Necessária se a etiqueta for exigida apenas para fins de acessibilidade e não contiver informações visuais adicionais sobre o campo
* **Nome do elemento** - o nome do campo que é enviado com os dados do formulário
* **Valor** - Valor padrão pré-preenchido no campo

### Sobre {#about}

![](assets/chlimage_1-24.png)

* **Mensagem de ajuda** - Uma dica para o usuário do que pode ser inserido no campo
* **Exibir mensagem de ajuda como espaço reservado** - Para exibir a mensagem de ajuda na entrada do formulário quando estiver vazia e não focada

### Restrições {#constraints}

![](assets/chlimage_1-25.png)

* **Mensagem de restrição**

   * Se o valor não validar o Tipo escolhido, a mensagem será exibida como uma dica de ferramenta ao enviar o formulário
   * Não exibido para **os tipos de restrição de Texto** e **Área** de texto

* **Obrigatório** - se selecionado, o usuário deve preencher um valor antes de enviar o formulário
* **Fazer somente leitura** - se selecionado, o usuário não poderá modificar o valor do campo

## Caixa de diálogo de design {#design-dialog}

Não há diálogo de design para o componente Texto de formulário.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de texto de formulário [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

Todo o projeto de componentes principais pode ser baixado de github.

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).
