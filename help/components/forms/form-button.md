---
title: Componente do botão de formulário
description: O componente principal Formulário oculto do componente permite a inclusão de um campo oculto em um formulário.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Componente do botão de formulário {#form-button-component}

O Componente principal do botão de formulário permite a inclusão de um botão para acionar uma ação em uma página.

## Uso {#usage}

O componente de Botão de formulário do componente principal permite a criação do campo de botão, geralmente para acionar a submissão do formulário e deve ser usado junto com o componente [Contêiner de](form-container.md)formulário.

As propriedades do botão podem ser definidas pelo editor de conteúdo na caixa de diálogo [](#configure-dialog)configurar.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do botão de formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-button-v1.md) | Compatível | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](/help/versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente do botão de formulário e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_form_button)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do botão de formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina os parâmetros do botão.

### Guia Propriedades {#properties-tab}

![](/help/assets/screen_shot_2018-01-12at120433.png)

* **Tipo**

   * **Botão**
   * **Enviar**

* **Título** - O texto exibido no botão

   * Se nenhum fornecido, o padrão será o tipo de botão

* **Nome** - o nome do botão, que é enviado com os dados do formulário
* **Valor** - O valor do botão, que é enviado com os dados do formulário

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente de botão de formulário suporta o AEM [Style System](/help/get-started/authoring.md#component-styling).
