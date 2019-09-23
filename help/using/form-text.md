---
title: Componente de texto do formulário
seo-title: Componente de texto do formulário
description: 'null'
seo-description: O componente principal de texto do formulário do componente permite a entrada do texto do formulário para envio.
uuid: f2418d55-0b59-4c7c-a541-d12dda4db4cf
contentOwner: Usuário
content-type: referência
topic-tags: autoria
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 3a970c4b-806b-4a0a-b6b8-b3dca4e9f136
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
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Componente de texto do formulário{#form-text-component}

O componente principal de texto do formulário do componente permite a entrada do texto do formulário para envio.

## Uso {#usage}

O componente de Texto do formulário permite o envio de diferentes tipos de texto e se destina a ser usado junto com o componente [de contêiner do](form-container.md)formulário. O tipo de validação de texto, rótulos e mensagens de ajuda podem ser definidos pelo editor de conteúdo na caixa de diálogo [](#configure-dialog)configurar.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de texto do formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatível | Compatível | Compatível |
| [v1](form-text-v1.md) | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

A seguir está uma amostra retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="text aem-GridColumn aem-GridColumn--default--12">
   <div class="cmp-form-text">
      <label for="form-text-2146967">How many pieces of toast would you like?
      </label>
   <input class="cmp-form-text__text" type="number" id="form-text-2146967" name="pieces">
   </div>
</div>
```

### JSON {#json}

```
"text":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "id":"form-text-2146967",
                     "title":"How many pieces of toast would you like?",
                     "name":"pieces",
                     "value":"",
                     "helpMessage":"",
                     "type":"number",
                     "readOnly":false,
                     "required":false,
                     "requiredMessage":"",
                     "constraintMessage":"",
                     "rows":2,
                     "defaultValue":"",
                     ":type":"core/wcm/components/form/text/v2/text"
                  }
```

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de texto do formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o tipo de texto a ser inserido, bem como valores e rótulos padrão.

### Guia Principal {#main-tab}

![](assets/chlimage_1-23.png)

* **Restrição** O tipo de texto a ser inserido e será validado em relação
   * **Text**
   * **Área de texto**
   * **E-mail**
   * **Telefone**
   * **Data**
   * **Número**
   * **Senha**
* **Linhas** de textoNúmero de linhas a serem exibidas na área de texto (somente exibidas quando **Restrição** estiver definida como Área **de** texto)
* **Rótulo** O rótulo que será exibido para o campo
* **Ocultar a etiqueta de ser exibida** Necessário se a etiqueta for exigida somente para fins de acessibilidade e não fornecer nenhuma informação visual adicional sobre o campo
* **Nome** do elementoO nome do campo enviado com os dados do formulário
* **Valor** padrão que é pré-preenchido no campo

### Guia Sobre {#about-tab}

![](assets/chlimage_1-24.png)

* **Mensagem** de ajudaUma dica para o usuário do que pode ser inserido no campo
* **Exibir mensagem de ajuda como espaço reservado** Para exibir a mensagem de ajuda dentro da entrada do formulário quando ela estiver vazia e não focalizada

### Guia de restrições {#constraints-tab}

![](assets/chlimage_1-25.png)

* **Mensagem de restrição**
   * Se o valor não validar o Tipo escolhido, a mensagem será exibida como uma dica de ferramenta ao enviar o formulário
   * Não exibido para tipos de restrição de **Texto** e Área **de** texto
* **Obrigatório** Se selecionado, o usuário deve preencher um valor antes de enviar o formulário
* **Tornar somente** leitura Se selecionado, o usuário não poderá modificar o valor do campo

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo de design para o componente de Texto do formulário.