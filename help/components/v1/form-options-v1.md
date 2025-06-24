---
title: Componente Opções de formulário v1
description: O componente Opções de formulário, dos Componentes principais, permitem a seleção de opções predefinidas em vários formatos.
index: n
role: Architect, Developer, Admin, User
exl-id: a5e8656b-eddd-48ec-876b-39bbaa70edf6
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 100%

---


# Componente Opções de formulário v1 {#form-options-component-v}

O componente Opções de formulário, dos Componentes principais, permitem a seleção de opções predefinidas em vários formatos.

## Uso {#usage}

O componente Opções de formulário, dos Componentes principais, permite o envio de diferentes tipos de opções apresentadas de várias maneiras diferentes e deve ser usado junto com o [componente de Contêiner de formulário](form-container-v1.md).

A apresentação das opções, rótulos e opções individuais pode ser definida pelo editor de conteúdo na [caixa de diálogo de configuração](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do componente Opções de formulário, introduzido originalmente com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do componente Opções de formulário.

| Versão do componente | AEM 6.3 | AEM 6.4 |
|--- |--- |--- |
| v2 | Compatível | Compatível |
| v1 | Compatível | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do componente Opções de formulário.
>
>Para obter detalhes sobre a versão atual do componente Opções de formulário, consulte o documento [Componente Opções de formulário](/help/components/forms/form-options.md).

## Exemplo de saída do componente {#sample-component-output}

O exemplo a seguir foi retirado do [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=pt-BR).

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
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para mais informações.

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o tipo de opções que devem ser apresentadas, rótulos e quais opções estão disponíveis.

![](/help/assets/chlimage_1-90.png)

* **Tipos**
Como as opções serão apresentadas

   * **Caixas de seleção**
   * **Botões de opção**
   * **Suspenso**
   * **Lista suspensa de multisseleção**

* **Título** - O título que será exibido como o rótulo das opções
* **Nome** - O nome do campo enviado com os dados de formulário
* **Origem** - Onde as opções são definidas

   * **Local** - Definido no componente
      * Toque ou clique no botão **Adicionar** para adicionar um valor, **Excluir** para remover um valor
      * **Valor** - O valor salvo quando essa opção é selecionada no envio do formulário
      * **Texto** - O rótulo para a opção exibida no formulário
      * **Ativo** - A opção é marcada como selecionada quando o formulário é carregado
      * **Desativado** - A opção não é selecionável, mas ainda é exibida
      * **Lista** - Uma lista estática definida no AEM é usada para a opção
         * **Lista** - O caminho da lista estática no AEM
            * Use o botão Procurar para localizar o recurso da lista
      * **Fonte de dados** - Uma fonte de dados é usada para as opções
         * **Fonte de dados** - Tipo de recurso da fonte de dados
* **Mensagem de ajuda** - Uma dica para o usuário sobre o que pode ser inserido no campo

## Caixa de diálogo de design {#design-dialog}

Não há caixa de diálogo de design para o componente Opções de formulário.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Opções de formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options).

Todo o projeto dos Componentes principais pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
