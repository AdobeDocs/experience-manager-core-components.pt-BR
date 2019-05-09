---
title: Componente do botão de formulário
seo-title: Componente do botão de formulário
description: 'null'
seo-description: O componente Oculto formulário de componente principal permite a inclusão de um campo oculto em um formulário.
uuid: 22 c 53 cd 0-d 0 bc -4 e 5 d -89 f 3-5 ac 4 f 61 a 9100
contentOwner: Usuário
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: a -2e 74 a -243 f -40 ab -903 c-c 7 d 3 e 8615 bcc
disttype: dist5
gnavtheme: light
groupsectionnavitems: não
hidemerchandisingbar: herdar
hidepromocomponent: herdar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente do botão de formulário{#form-button-component}

O componente de botão de formulário principal do componente permite a inclusão de um botão para acionar uma ação em uma página.

## Uso {#usage}

O componente Botão de formulário de formulário principal permite a criação de um campo de botão, geralmente para acionar o envio do formulário e deve ser usado junto com o componente do contêiner [de formulário](form-container.md).

As propriedades do botão podem ser definidas pelo editor de conteúdo na caixa de diálogo [Configurar](form-button.md).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente do botão de formulário é v 2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatível | Compatível | Compatível |
| [v1](form-button-v1.md) | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/screen_shot_2018-01-12at120021.png)

### HTML {#html}

```
<div class="container responsivegrid aem-GridColumn aem-GridColumn--default--12">
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="cmp-form aem-Grid aem-Grid--12 aem-Grid--default--12">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="button aem-GridColumn aem-GridColumn--default--12">
<button type="BUTTON" class="cmp-form-button" name="loveToast" value="ILoveToast">Click here if you love toast!</button>
</div>

</form>
</div>
```

### JSON {#json}

```
"button":{  
                           "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                           ":type":"core/wcm/sandbox/components/form/button/v2/button",
                           "name":"loveToast",
                           "jcr:title":"Click here if you love toast!",
                           "type":"button",
                           "value":"ILoveToast"
                        }
```

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente do botão de formulário [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo defina os parâmetros do botão.

### Guia Propriedades {#properties-tab}

![](assets/screen_shot_2018-01-12at120433.png)

* **Tipo**

   * **Imagem**
   * **Enviar**

* **Título** - o texto exibido no botão

   * Se nenhum for o padrão, o tipo de botão será definido como padrão

* **Nome** - o nome do botão, que é enviado com os dados do formulário
* **Valor** - O valor do botão, que é enviado com os dados do formulário

## Caixa de diálogo de design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente de botão de formulário é compatível com o Sistema [de estilo do AEM](authoring.md#component-styling).