---
title: Componente oculto do formulário
description: O componente principal Formulário oculto do componente permite a exibição de um campo oculto.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Componente oculto do formulário{#form-hidden-component}

O componente principal Formulário oculto do componente permite a exibição de um campo oculto.

## Uso {#usage}

O componente principal Oculto do formulário permite que a criação de campos ocultos transmita informações sobre a página atual para o AEM e deve ser usado junto com o componente [do contêiner de](form-container.md)formulário.

As propriedades de campo podem ser definidas pelo editor de conteúdo na caixa de diálogo [](form-hidden.md)configurar.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente oculto do formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatível | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](/help/versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o componente Oculto do formulário e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_form_hidden)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente oculto do formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina os parâmetros do campo oculto.

![](/help/assets/chlimage_1-26.png)

* **Nome** O nome do campo, que é enviado com os dados do formulário
* **Valor** O valor do campo, que é submetido com os dados do formulário
* **Identificador** O identificador deve ser exclusivo na página e pode ser usado para vincular scripts a esse campo de formulário

Como o componente Form Oculto normalmente não tem atributos visíveis, o espaço reservado do componente no editor exibe os valores dos campos **Nome** e **Valor** se eles forem atribuídos para ajudar o autor a identificar o componente Form Oculto apropriado.

![](/help/assets/screenshot_2018-10-19at094927.png)

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo de design para o componente Form Hidden.
