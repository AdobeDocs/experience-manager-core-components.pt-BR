---
title: Componente de Contêiner de formulário v1
description: O componente de Contêiner de formulário, dos Componentes principais, permite a criação de formulários de envio simples.
index: n
role: Architect, Developer, Admin, User
exl-id: 1e34219f-fa82-494e-82e2-1b4d63d37fea
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 100%

---


# Componente de Contêiner de formulário v1 {#form-container-component-v1}

O componente de Contêiner de formulário, dos Componentes principais, permite a criação de formulários de envio simples.

## Uso {#usage}

O componente de Contêiner de formulário possibilitou a criação de formulários e recursos simples de envio de informações, ao oferecer suporte a formulários WCM simples e ao usar uma estrutura aninhada para permitir componentes de formulário adicionais.

Usando a [caixa de diálogo de configuração](#settings-dialog), o editor de conteúdo pode definir que tipo de ação de envio de formulário aciona, onde o conteúdo enviado deve ser armazenado e se um fluxo de trabalho deve ser acionado. O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir os componentes de permissão e seus mapeamentos semelhantes à caixa de diálogo de design para o [contêiner de layout padrão no editor de modelo](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/siteandpage/templates.html?lang=pt-BR).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do componente de Contêiner de formulário, introduzido originalmente com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do componente de Contêiner de formulário.

| Versão do AEM | Componente de Contêiner de formulário v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do componente de Contêiner de formulário.
>
>Para obter detalhes sobre a versão atual do componente do Contêiner de formulário, consulte o documento [componente do Contêiner de formulário](/help/components/forms/form-container.md).

## Caixa de diálogo de configurações {#settings-dialog}

A caixa de diálogo de configurações permite que o autor de conteúdo defina quais ações serão executadas quando o componente for enviado.

![](/help/assets/chlimage_1.png)

Dependendo do **Tipo de ação** selecionado, as opções disponíveis no contêiner serão alteradas. Os tipos de ação disponíveis são:

* [Email](#mail)
* [Armazenar conteúdo](#store-content)
* [Enviar Ordem](#submit-order)
* [Atualizar a ordem](#update-order)

Independentemente do tipo, há [configurações gerais](#general-settings) que se aplicam a cada ação.

### Email {#mail}

Quando o formulário for enviado, o tipo de ação de email enviará um email para os destinatários designados.

![](/help/assets/chlimage_1-1.png)

* **Assunto** - O assunto do email que será enviado no envio do formulário
* **De** - O endereço de email da origem do email que será enviado no envio do formulário
* **Para** - Os endereços dos destinatários que receberão um email no envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar mais endereços
   * Toque ou clique no botão **Excluir** para remover um endereço de email
* **CC** - Os endereços dos destinatários que receberão uma cópia do email enviado após o envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar mais endereços
   * Toque ou clique no botão **Excluir** para remover um endereço de email

### Armazenar conteúdo {#store-content}

Quando o formulário for enviado, o conteúdo será armazenado em um local de repositório designado.

![](/help/assets/chlimage_1-2.png)

* **Caminho de conteúdo** - Caminho do repositório do conteúdo repositório onde o conteúdo enviado está armazenado
* **Exibir dados** - Toque ou clique para exibir os dados enviados armazenados como JSON
* **Iniciar fluxo de trabalho** - Configurar para iniciar um fluxo de trabalho com o conteúdo armazenado como carga útil no envio do formulário

### Enviar Ordem {#submit-order}

Quando o formulário for enviado, a ordem será enviada.

![](/help/assets/chlimage_1-3.png)

### Atualizar a ordem {#update-order}

Quando o formulário for enviado, a ordem será atualizada.

![](/help/assets/chlimage_1-4.png)

### Configurações gerais {#general-settings}

Independentemente do tipo de ação selecionada, uma página de agradecimento sempre pode ser definida.

![](/help/assets/chlimage_1-5.png)

O usuário será redirecionado para a página especificada após a conclusão do envio do formulário.

* Use a caixa de diálogo de seleção para selecionar um recurso dentro do AEM.
* Se a página de agradecimento não estiver no AEM, especifique o URL absoluto. URLs não absolutos serão interpretados de acordo com o AEM.
* Deixe em branco para exibir novamente o formulário após o envio.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os componentes permitidos e seus mapeamentos para o contêiner semelhante à caixa de diálogo de design para o [contêiner de layout padrão no editor de modelo](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/siteandpage/templates.html?lang=pt-BR).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Contêiner de formulário [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

Todo o projeto dos Componentes principais pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
