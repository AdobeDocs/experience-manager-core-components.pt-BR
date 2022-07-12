---
title: Componente Formulário Oculto
description: O componente Formulário Oculto, dos Componentes Principais, possibilita a exibição de um campo oculto.
role: Architect, Developer, Admin, User
exl-id: 0364cd3b-3c09-46db-9392-a67e3f9ea7a5
source-git-commit: 16930ccaa281f9d9c4ddbb890d4222e128557580
workflow-type: ht
source-wordcount: '433'
ht-degree: 100%

---

# Componente Formulário oculto {#form-hidden-component}

O componente Formulário Oculto, dos Componentes Principais, possibilita a exibição de um campo oculto.

## Uso {#usage}

O componente Formulário oculto, dos Componentes principais, possibilita a criação de campos ocultos para transmitir informações sobre a página atual de volta ao AEM. Ele deve ser usado com o [componente Contêiner de Formulário](form-container.md).

As propriedades do campo podem ser definidas pelo editor de conteúdo na [caixa de diálogo de configuração](form-hidden.md).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente Formulário Oculto é a v2, que foi introduzida com a versão 2.0.0 dos Componentes Principais em janeiro de 2018, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível  com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | Compatível |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatível | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Formulário Oculto e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_form_hidden_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Formulário Oculto [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina os parâmetros do campo oculto.

![Caixa de diálogo de edição do Formulário Oculto](/help/assets/form-hidden-edit.png)

* **Nome** - O nome do campo, que é enviado com os dados de formulário
* **Valor** - O valor do campo, que é enviado com os dados de formulário
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

Uma vez que o componente Formulário Oculto normalmente não tem atributos visíveis, o espaço reservado do componente no editor exibe os valores dos campos **Nome** e **Valor** se forem atribuídos para ajudar o autor a identificar o componente Formulário Oculto apropriado.

![Exemplo do componente Formulário Oculto](/help/assets/form-hidden-example.png)

## Caixa de diálogo de design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente Formulário Oculto é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
