---
title: Componente de texto de formulário
seo-title: Componente de texto de formulário
description: 'null'
seo-description: O componente de Texto do formulário de componente principal permite a entrada do texto do formulário para envio.
uuid: f 2418 d 55-0 b 59-4 c 7 c-a 541-d 12 dda 4 db 4 cf
contentOwner: Usuário
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 3 a 970 c 4 b -806 b -4 a 0 a-b 6 b 8-b 3 dca 4 e 9 f 136
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


# Componente de texto de formulário{#form-text-component}

O componente de Texto do formulário de componente principal permite a entrada do texto do formulário para envio.

## Uso {#usage}

O componente de Texto de formulário permite o envio de diferentes tipos de texto e deve ser usado junto com o componente do contêiner [de formulário](form-container.md). O tipo de validação de texto, rótulos e mensagens de ajuda pode ser definido pelo editor de conteúdo na caixa de diálogo [Configurar](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de texto de formulário é v 2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatível | Compatível | Compatível |
| [v1](form-text-v1.md) | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

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

A documentação técnica mais recente sobre o Componente de texto de formulário [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo defina o tipo de texto a ser inserido, bem como valores e rótulos padrão.

### Guia Principal {#main-tab}

![](assets/chlimage_1-23.png)

* **Restrição**
O tipo de texto a ser inserido e será validado em comparação a
   * **Text**
   * **Área de texto**
   * **E-mail**
   * **Telefone**
   * **Data**
   * **Número**
   * **Senha**
* **Linhas
de texto** Número de linhas a serem exibidas na área de texto (somente exibidas quando **a Restrição** está definida como **Área de texto**)
* **Rótulo**
O rótulo que será exibido para o campo
* **Ocultar o rótulo a ser exibido**
Necessário se o rótulo for necessário apenas para fins de acessibilidade e não fizer a api supart additional informações adicionais sobre o campo
* **Nome
do elemento** O nome do campo que é enviado com os dados do formulário
* **Valor**padrão de valor
pré-preenchido no campo

### Sobre tabulação {#about-tab}

![](assets/chlimage_1-24.png)

* **Mensagem
de ajuda** Uma dica para o usuário do que pode ser inserido no campo
* **Exibir mensagem de ajuda como espaço reservado**
Para exibir a mensagem de ajuda dentro da entrada do formulário quando estiver vazia e não focada

### Guia de restrições {#constraints-tab}

![](assets/chlimage_1-25.png)

* **Mensagem de restrição**
   * Se o valor não validar o Tipo escolhido, a mensagem será exibida como uma dica de ferramenta ao enviar o formulário
   * Não exibido para **os tipos de restrição de Texto** e **Área** de texto
* **Obrigatório**
Se selecionado o usuário deve preencher um valor antes de enviar o formulário
* **Faça a leitura somente** se selecionado o usuário não puder modificar o valor do campo

## Caixa de diálogo de design {#design-dialog}

Não há diálogo de design para o componente Texto de formulário.