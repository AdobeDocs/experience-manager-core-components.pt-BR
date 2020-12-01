---
title: Componente de Container de formulário (v1)
description: O Componente principal de Container de formulário permite a criação de formulários simples de envio.
index: n
translation-type: tm+mt
source-git-commit: 68472ab548fb6ebb443a06c12e7b37797a0c1302
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 3%

---


# Componente de Container de formulário (v1) {#form-container-component-v1}

O Componente principal de Container de formulário permite a criação de formulários simples de envio.

## Uso {#usage}

O Componente de Container de formulário permitiu a criação de formulários e recursos simples de envio de informações ao suportar formulários WCM simples e ao usar uma estrutura aninhada para permitir componentes de formulário adicionais.

Usando a caixa de diálogo [de configuração](#settings-dialog), o editor de conteúdo pode definir que tipo de ação o envio do formulário aciona, onde o conteúdo enviado deve ser armazenado e se um fluxo de trabalho deve ser acionado. O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir os componentes de permissão e seus mapeamentos semelhantes à caixa de diálogo de design para o [container de layout padrão no editor de modelo](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente do Container de formulário, originalmente introduzido com a versão 1.0.0 dos Componentes principais com a AEM 6.3.

A tabela a seguir lista a compatibilidade de v1 do Componente do Container de formulário.

| Versão do AEM | Componente de Container de formulário v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do Componente do Container de formulário.
>
>Para obter detalhes sobre a versão atual do Componente de Container de formulário, consulte o documento [Componente de Container de formulário](/help/components/forms/form-container.md).

## Caixa de diálogo Configurações {#settings-dialog}

A caixa de diálogo de configurações permite que o autor do conteúdo defina quais ações serão executadas quando o componente for enviado.

![](/help/assets/chlimage_1.png)

Dependendo do **Tipo de ação** selecionado, as opções disponíveis no container serão alteradas. Os tipos de ação disponíveis são:

* [Email](#mail)
* [Armazenar conteúdo](#store-content)
* [Enviar pedido](#submit-order)
* [Atualizar pedido](#update-order)

Independentemente do tipo, existem [definições gerais](#general-settings) que se aplicam a cada ação.

### Email {#mail}

Quando o formulário for enviado, o tipo de ação de email enviará um email para os recipient designados.

![](/help/assets/chlimage_1-1.png)

* **Assunto**  - O assunto do e-mail que será enviado no envio do formulário
* **De** - O endereço de email de formulário do email que será enviado no envio do formulário
* **Para**  - Os endereços dos recipient que receberão um email após o envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais
   * Toque ou clique no botão **Excluir** para remover um endereço de email
* **CC** - Os endereços dos recipient que receberão uma cópia de carbono do e-mail enviado após o envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais
   * Toque ou clique no botão **Excluir** para remover um endereço de email

### Armazenar conteúdo {#store-content}

Quando o formulário for enviado, o conteúdo do formulário será armazenado em um local de repositório designado.

![](/help/assets/chlimage_1-2.png)

* **Caminho**  do conteúdo - Caminho do repositório do conteúdo no qual o conteúdo enviado é armazenado
* **Dados**  de visualização - Toque ou clique para visualização de dados enviados armazenados como JSON
* **Fluxo de trabalho**  do start - Configure para start de um fluxo de trabalho com o conteúdo armazenado como carga após o envio do formulário

### Enviar pedido {#submit-order}

Quando o formulário for submetido, a ordem será enviada.

![](/help/assets/chlimage_1-3.png)

### Atualizar pedido {#update-order}

Quando o formulário for enviado, o pedido será atualizado.

![](/help/assets/chlimage_1-4.png)

### Configurações gerais {#general-settings}

Independentemente do tipo de ação selecionado, uma página de agradecimento sempre pode ser definida.

![](/help/assets/chlimage_1-5.png)

O usuário será redirecionado para a página especificada após a conclusão do envio do formulário.

* Use a caixa de diálogo Seleção para selecionar um recurso dentro do AEM.
* Se a página de agradecimento não estiver em AEM, especifique o URL absoluto. URLs não absolutos serão interpretados em relação ao AEM.
* Deixe em branco para exibir novamente o formulário após o envio.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os componentes permitidos e seus mapeamentos para o container de forma semelhante à caixa de diálogo de design para o container de layout padrão [no editor de modelo](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de Container de formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

Todo o projeto de componentes principais pode ser baixado do GitHub.

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
