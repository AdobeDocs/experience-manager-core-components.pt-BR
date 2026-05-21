---
title: Componente de Texto do formulário
description: O componente de Texto de formulário, dos Componentes principais, permite a entrada do texto de formulário para envio.
role: Developer, Admin, User
exl-id: e8fa3881-51fb-4726-9654-8f93acfb7464
TQID: https://experienceleague.adobe.com/9js-R-LzxStEKmgs59UvZBz-htCWyIx-PQIjpIKJAqc
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 581
ht-degree: 100%

---

# Componente de Texto do formulário{#form-text-component}

O componente de Texto de formulário, dos Componentes principais, permite a entrada do texto de formulário para envio.

## Uso {#usage}

O componente de Texto do formulário permite o envio de diferentes tipos de texto e deve ser usado junto com o [componente de Contêiner de formulário](form-container.md). O tipo de validação de texto, rótulos e mensagens de ajuda pode ser definido pelo editor de conteúdo na [caixa de diálogo de configuração](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Texto de formulário é a v2, introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Compatível com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-text-v1.md) | Compatível | Compatível | - | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Texto de Formulário, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_form_text_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Texto do formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o tipo de texto a ser inserido, bem como valores e rótulos padrão.

### Guia Propriedades {#properties-tab}

![Guia Propriedades](/help/assets/form-text-edit-properties.png)

* **Restrição** - O tipo de texto a ser inserido e em relação ao qual será validado
   * **Texto**
   * **Área de texto**
   * **Email**
   * **Telefone**
   * **Data**
   * **Número**
   * **Senha**
* **Linhas de texto** - Número de linhas a serem exibidas na área de texto (exibidas somente quando a **Restrição** é definida como **Área de texto**)
* **Rótulo** - O rótulo que será exibido para o campo
* **Impedir o rótulo de ser exibido** - Necessário se o rótulo for necessário somente para fins de acessibilidade e não imprimir nenhuma informação visual adicional sobre o campo
* **Nome do elemento** - O nome do campo enviado com os dados de formulário
* **Valor** - O valor padrão que é pré-preenchido no campo
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Sobre a guia {#about-tab}

![Sobre a guia](/help/assets/form-text-edit-about.png)

* **Mensagem de ajuda** - Uma dica para o usuário sobre o que pode ser inserido no campo
* **Exibir mensagem de ajuda como espaço reservado** -Para exibir a mensagem de ajuda dentro da entrada de formulário quando ela estiver vazia e não focalizada

### Guia de restrições {#constraints-tab}

![Guia de restrições](/help/assets/form-text-edit-constraints.png)

* **Mensagem de restrição**
   * Se o valor não validar o Tipo escolhido, a mensagem será exibida como uma dica de ferramenta ao enviar o formulário
   * Não exibido para tipos de restrição de **Texto** e **Área de Texto**
* **Obrigatório** - Caso selecionado, o usuário deve preencher um valor antes de enviar o formulário
   * **Mensagem obrigatória** - Mensagem exibida como uma dica de ferramenta se o campo ficar vazio
* **Tornar somente leitura** - Caso selecionado, o usuário não poderá modificar o valor do campo

## Caixa de diálogo de design {#design-dialog}

### Guia Estilos {#styles-tab}

O Componente de Texto de formulário é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
