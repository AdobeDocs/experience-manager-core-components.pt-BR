---
title: Componente do contêiner de formulário (v1)
description: O Componente de contêiner de formulário do componente principal permite a criação de formulários de envio simples.
index: n
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 3%

---


# Componente do contêiner de formulário (v1) {#form-container-component-v1}

O Componente de contêiner de formulário do componente principal permite a criação de formulários de envio simples.

## Uso {#usage}

O Componente de contêiner de formulário possibilitou a criação de formulários e recursos simples de envio de informações, ao oferecer suporte a formulários WCM simples e ao usar uma estrutura aninhada para permitir componentes de formulário adicionais.

Usando a caixa de diálogo [de configuração](#settings-dialog), o editor de conteúdo pode definir que tipo de ação de envio de formulário aciona, onde o conteúdo enviado deve ser armazenado e se um fluxo de trabalho deve ser acionado. O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir os componentes de permissão e seus mapeamentos semelhantes à caixa de diálogo de design para o [contêiner de layout padrão no editor de modelo](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente do contêiner de formulário, introduzido originalmente com a versão 1.0.0 dos Componentes principais com a AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do Componente do Contêiner de formulário.

| Versão do AEM | Componente do contêiner de formulário v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do Componente do contêiner de formulário.
>
>Para obter detalhes sobre a versão atual do Componente do contêiner de formulário, consulte o documento [Componente do contêiner de formulário](/help/components/forms/form-container.md).

## Caixa de diálogo Configurações {#settings-dialog}

A caixa de diálogo de configurações permite que o autor de conteúdo defina quais ações serão executadas quando o componente for enviado.

![](/help/assets/chlimage_1.png)

Dependendo do **Tipo de ação** selecionado, as opções disponíveis no contêiner serão alteradas. Os tipos de ação disponíveis são:

* [Email](#mail)
* [Armazenar conteúdo](#store-content)
* [Enviar pedido](#submit-order)
* [Atualizar pedido](#update-order)

Independentemente do tipo , há [configurações gerais](#general-settings) que se aplicam a cada ação.

### Email {#mail}

Quando o formulário for enviado, o tipo de ação de email enviará um email para os recipients designados.

![](/help/assets/chlimage_1-1.png)

* **Assunto**  - O assunto do email que será enviado no envio do formulário
* **De**  - O endereço de email de formulário do email que será enviado no envio do formulário
* **To**  - Os endereços dos recipients que receberão um email no envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais
   * Toque ou clique no botão **Delete** para remover um endereço de email
* **CC**  - Os endereços dos recipients que receberão uma cópia em carbono do e-mail enviado após o envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais
   * Toque ou clique no botão **Delete** para remover um endereço de email

### Armazenar conteúdo {#store-content}

Quando o formulário for enviado, o conteúdo será armazenado em um local de repositório designado.

![](/help/assets/chlimage_1-2.png)

* **Caminho do conteúdo**  - Caminho do repositório do conteúdo onde o conteúdo enviado é armazenado
* **Exibir dados**  - Toque ou clique para exibir os dados enviados armazenados como JSON
* **Iniciar fluxo de trabalho**  - Configurar para iniciar um fluxo de trabalho com o conteúdo armazenado como carga útil no envio do formulário

### Enviar pedido {#submit-order}

Quando o formulário for enviado, a ordem será enviada.

![](/help/assets/chlimage_1-3.png)

### Atualizar pedido {#update-order}

Quando o formulário for enviado, a ordem será atualizada.

![](/help/assets/chlimage_1-4.png)

### Configurações gerais {#general-settings}

Independentemente do tipo de ação selecionada, uma página de agradecimento sempre pode ser definida.

![](/help/assets/chlimage_1-5.png)

O usuário será redirecionado para a página especificada após a conclusão do envio do formulário.

* Use a caixa de diálogo de seleção para selecionar um recurso dentro do AEM.
* Se a página de agradecimento não estiver em AEM, especifique o URL absoluto. URLs não absolutos serão interpretados de acordo com AEM.
* Deixe em branco para exibir novamente o formulário após o envio.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os componentes permitidos e seus mapeamentos para o contêiner semelhante à caixa de diálogo de design para o [contêiner de layout padrão no editor de modelo](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do contêiner de formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

O projeto de componentes principais inteiro pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
