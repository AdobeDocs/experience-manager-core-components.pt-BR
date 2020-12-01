---
title: Componente do botão de formulário
description: O componente principal Formulário oculto do componente permite a inclusão de um campo oculto em um formulário.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---


# Componente do botão de formulário {#form-button-component}

O Componente principal do botão de formulário permite a inclusão de um botão para acionar uma ação em uma página.

## Uso {#usage}

O componente de Botão de formulário do componente principal permite a criação do campo de botão, geralmente para acionar a submissão do formulário e é destinado a ser usado junto com o [componente de Container de formulário](form-container.md).

As propriedades do botão podem ser definidas pelo editor de conteúdo na caixa de diálogo [configure](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do botão de formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-button-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente do botão de formulário e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_button).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do botão de formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina os parâmetros do botão.

### Guia Propriedades {#properties-tab}

![Caixa de diálogo de edição do componente do botão de formulário](/help/assets/form-button-edit.png)

* **Tipo**

   * **Botão**
   * **Enviar**

* **Título**  - O texto exibido no botão

   * Se nenhum fornecido, o padrão será o tipo de botão

* **Nome**  - O nome do botão, que é enviado com os dados do formulário
* **Valor**  - O valor do botão, que é enviado com os dados do formulário

* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [ de ](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente do botão de formulário suporta o AEM [Sistema de estilo](/help/get-started/authoring.md#component-styling).
