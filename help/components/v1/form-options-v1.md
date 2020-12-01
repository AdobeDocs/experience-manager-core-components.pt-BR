---
title: Componente de opções de formulário (v1)
description: O componente de opções de Formulário de componente principal permite a seleção de opções predefinidas em vários formatos.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 3%

---


# Componente de opções de formulário (v1) {#form-options-component-v}

O componente de opções de Formulário de componente principal permite a seleção de opções predefinidas em vários formatos.

## Uso {#usage}

O Componente de opções de formulário do componente principal permite a submissão de diferentes tipos de opções apresentadas de várias maneiras diferentes e destina-se a ser usado junto com o [componente de container de formulário](form-container-v1.md).

A apresentação das opções, rótulos e opções individuais pode ser definida pelo editor de conteúdo na caixa de diálogo [configurar](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente de opções de formulário, originalmente introduzido com a versão 1.0.0 dos Componentes principais com a AEM 6.3.

A tabela a seguir lista a compatibilidade de v1 do Componente de opções de formulário.

| Versão do componente | AEM 6.3 | AEM 6.4 |
|--- |--- |--- |
| v2 | Compatível | Compatível |
| v1 | Compatível | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do Componente de opções de formulário.
>
>Para obter detalhes sobre a versão atual do Componente de opções de formulário, consulte o documento [Componente de opções de formulário](/help/components/forms/form-options.md).

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](/help/assets/chlimage_1-89.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="cmp cmp-options aem-GridColumn aem-GridColumn--default--12">

    <fieldset class="form-group checkbox">
        <legend>What is your favorite type of toast?</legend>
        
        <div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="dry">
              Plain dry toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="french">
              French toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="texas">
              Texas toast
            </label>
        </div>

    </fieldset>
    
</div>
    
</form></div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "options": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/options",
                  "name": "toastTypes",
                  "jcr:title": "What is your favorite type of toast?",
                  "source": "local",
                  "type": "checkbox"
                }
              },
              ":itemsOrder": [
                "options"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>A exportação JSON dos Componentes principais exige a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o tipo de opções que devem ser apresentadas, rótulos e quais opções estão disponíveis.

![](/help/assets/chlimage_1-90.png)

* ****
TiposComo as opções serão apresentadas

   * **Caixas de seleção**
   * **Botões de opção**
   * **Suspenso**
   * **Lista suspensa de multisseleção**

* **Título**  - o título que será exibido como o rótulo das opções
* **Nome**  - O nome do campo enviado com os dados do formulário
* **Origem**  - onde as opções são definidas

   * **Local**  - Definido no componente
      * Toque ou clique no botão **Adicionar** para adicionar um valor, **Eliminar** para remover um valor
      * **Valor**  - O valor salvo quando essa opção é selecionada quando o formulário é enviado
      * **Texto**  - O rótulo da opção exibida no formulário
      * **Ativo**  - A opção é marcada como selecionada quando o formulário é carregado
      * **Desativado**  - A opção não é selecionável, mas ainda é exibida
      * **Lista**  - Uma lista estática definida em outro lugar no AEM é usada para a opção
         * **Lista**  - O caminho da lista estática no AEM
            * Use o botão Procurar para localizar o recurso de lista
      * **Fonte**  de dados - uma fonte de dados é usada para as opções
         * **Fonte**  de dados - tipo de recurso da fonte de dados
* **Mensagem**  de ajuda - uma dica para o usuário do que pode ser inserido no campo

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo de design para o componente Opções de formulário.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de opções de formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options).

Todo o projeto de componentes principais pode ser baixado do GitHub.

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
