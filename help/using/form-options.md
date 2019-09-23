---
title: Componente Opções de formulário
seo-title: Componente Opções de formulário
description: O componente de opções de Formulário de componente principal permite a seleção de opções predefinidas em vários formatos.
seo-description: O componente de opções de Formulário de componente principal permite a seleção de opções predefinidas em vários formatos.
uuid: 7e8714df-75d1-4bb0-b1ee-b7c7450d806a
contentOwner: Usuário
content-type: referência
topic-tags: autoria
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 42289c2b-1671-463a-ac1d-457aa9aefa2a
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Componente Opções de formulário{#form-options-component}

O componente Opções de formulário do componente principal permite a seleção de opções predefinidas em vários formatos.

## Uso {#usage}

O componente Opções de formulário do componente principal permite o envio de diferentes tipos de opções apresentadas de várias maneiras diferentes e é destinado ao uso junto com o componente [Contêiner de](form-container.md)formulário.

A apresentação das opções, rótulos e opções individuais pode ser definida pelo editor de conteúdo na caixa de diálogo [](#configure-dialog)configurar.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de opções de formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatível | Compatível | Compatível |
| [v1](form-options-v1.md) | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

A seguir está uma amostra retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/screen_shot_2018-01-12at113648.png)

### HTML {#html}

```
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="cmp-form aem-Grid aem-Grid--12 aem-Grid--default--12">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-66464844" name="hidden">

</div>
<div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-858231075" name="hidden">

</div>
<div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-862566768" name="hidden">

</div>
<div class="container responsivegrid aem-GridColumn aem-GridColumn--default--12">

    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container/container">
    
    <div class="options aem-GridColumn aem-GridColumn--default--12">

    <fieldset class="cmp-form-options">
        
            <legend class="cmp-form-options__legend">What is your favorite type of toast?</legend>
            <label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="dryToast">
                Plain dry toast
            </label>
<label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="frenchToast">
                French Toast
            </label>
<label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="texasToast">
                Texas Toast
            </label>

    </fieldset>

</div>

</div></form>
```

### JSON {#json}

```
"container":{  
                           "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                           "columnCount":12,
                           "gridClassNames":"aem-Grid aem-Grid--12 aem-Grid--default--12",
                           ":items":{  
                              "options_816658469":{  
                                 "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                                 "id":"form-options-269951232",
                                 "title":"What is your favorite type of toast?",
                                 "name":"favToast",
                                 "type":"RADIO",
                                 "items":[  
                                    {  
                                       "value":"dryToast",
                                       "text":"Plain dry toast",
                                       "selected":false,
                                       "disabled":false
                                    },
                                    {  
                                       "value":"frenchToast",
                                       "text":"French Toast",
                                       "selected":false,
                                       "disabled":false
                                    },
                                    {  
                                       "value":"texasToast",
                                       "text":"Texas Toast",
                                       "selected":false,
                                       "disabled":false
                                    }
                                 ],
                                 ":type":"core/wcm/sandbox/components/form/options/v2/options"
                              }
                           },
                           ":itemsOrder":[  
                              "options_816658469"
                           ],
                           ":type":"core/wcm/sandbox/components/form/container/v2/container"
                        }
```

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de opções de formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o tipo de opções que devem ser apresentadas, rótulos e quais opções estão disponíveis.

![](assets/screen_shot_2018-01-12at113153.png)

* **Tipos** - Como as opções serão apresentadas
   * **Caixas de seleção**
   * **Botões de opção**
   * **Suspenso**
   * **Lista suspensa de multisseleção**
* **Título** O título que será exibido como o rótulo das opções
* **Nome** O nome do campo enviado com os dados do formulário
* **Origem** Onde as opções são definidas
   * **Local** Definido no componente
      * Toque ou clique no botão **Adicionar** para adicionar um valor, **Excluir** para remover um valor
      * **Valor** O valor salvo quando essa opção é selecionada quando o formulário é enviado
      * **Texto** O rótulo da opção exibida no formulário
      * **Ativo** A opção é marcada como selecionada quando o formulário é carregado
      * **Desativada** A opção não é selecionável, mas ainda é exibida
      * **Lista** Uma lista estática definida em outro lugar no AEM é usada para as opções
         * **Lista** O caminho da lista estática no AEM
            * Use o botão Procurar para localizar o recurso de lista
      * **Fonte** de dadosUma fonte de dados é usada para as opções
         * **Fonte** de dados Tipo de recurso da fonte de dados
* **Mensagem** de ajudaUma dica para o usuário do que pode ser inserido no campo

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente de opções de formulário suporta o AEM [Style System](authoring.md#component-styling).