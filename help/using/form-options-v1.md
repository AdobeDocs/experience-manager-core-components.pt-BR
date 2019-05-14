---
title: Componente de opções de formulário (v 1)
seo-title: Componente de opções de formulário (v 1)
description: 'null'
seo-description: O componente de opções de Formulário de componente principal permite a seleção de opções predefinidas em vários formatos.
uuid: a 22 ed 77 c-c 9 f 3-46 f 4-8 afe-e 478383 c 1251
content-type: referência
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: e 1975 bfe -2 bda -409 a -998 e -1 ff 4 f 9 f 23 b 94
disttype: dist5
gnavtheme: light
groupsectionnavitems: não
hidemerchandisingbar: herdar
hidepromocomponent: herdar
modalsize: 426x240
noindex: verdadeiro
index: n
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Componente de opções de formulário (v 1){#form-options-component-v}

O componente de opções de Formulário de componente principal permite a seleção de opções predefinidas em vários formatos.

## Uso {#usage}

O Componente de opções de formulário do componente principal permite o envio de diferentes tipos de opções apresentadas de várias formas diferentes e destina-se a ser usado junto com [o componente do contêiner de formulário](form-container.md).

A apresentação das opções, rótulos e opções individuais pode ser definida pelo editor de conteúdo na caixa de diálogo [Configurar](form-options-v1.md#main-pars_title).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve v 1 do Componente de opções de formulário, originalmente introduzido com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v 1 do Componente de opções de formulário.

| Versão do componente | AEM 6.3 | AEM 6.4 |
|--- |--- |--- |
| v2 | Compatível | Compatível |
| v1 | Compatível | Compatível |

>[!CAUTION]
>
>Este documento descreve v 1 do componente de opções de formulário.
>
>Para obter detalhes sobre a versão atual do Componente de opções de formulário, consulte o [documento Componente](form-options.md) de opções de formulário.

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/chlimage_1-89.png)

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
>A exportação JSON dos componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade para Componentes principais v 1](versions.md#main-pars_title_236368006) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo defina o tipo de opções que devem ser apresentadas, rótulos e quais opções estão disponíveis.

![](assets/chlimage_1-90.png)

* **Tipos**
como as opções serão apresentadas

   * **Caixas de seleção**
   * **Botões de opção**
   * **Suspenso**
   * **Lista suspensa de multisseleção**

* **Título** - o título que será exibido como rótulo para as opções
* **Nome** - o nome do campo enviado com os dados do formulário
* **Fonte** - Onde as opções são definidas

   * **Local** - definido no componente
      * Toque ou clique no **botão Adicionar** para adicionar um valor, **Excluir** para remover um valor
      * **Valor** - o valor salvo quando essa opção é selecionada quando o formulário é enviado
      * **Texto** - O rótulo da opção exibida no formulário
      * **Ativo** - A opção é marcada como selecionada quando o formulário é carregado
      * **Desativado** - A opção não é selecionável, mas ainda exibe
      * **Lista** - Uma lista estática definida em outro lugar no AEM é usada para a opção
         * **Lista** - o caminho da lista estática no AEM
            * Use o botão Procurar para localizar o recurso da lista
      * **Fonte de dados** - Uma fonte de dados é usada para as opções
         * **Fonte de dados** - tipo de recurso da fonte de dados
* **Mensagem de ajuda** - Uma dica para o usuário do que pode ser inserido no campo

## Caixa de diálogo de design {#design-dialog}

Não há diálogo de design para o componente Opções de formulário.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de opções de formulário [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options).

Todo o projeto de componentes principais pode ser baixado de github.

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).
