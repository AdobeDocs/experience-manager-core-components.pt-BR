---
title: Componente do contêiner de formulário
description: O Componente principal do contêiner de formulário permite a criação de formulários simples de envio.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Componente do contêiner de formulário {#form-container-component}

O Componente principal do contêiner de formulário permite a criação de formulários simples de envio.

## Uso {#usage}

O componente de contêiner de formulário permite a criação de formulários e recursos simples de envio de informações, ao suportar formulários WCM simples e ao usar uma estrutura aninhada para permitir componentes de formulário adicionais.

Usando a caixa de diálogo [](#configure-dialog) configurar, o editor de conteúdo pode definir a ação acionada pelo envio do formulário, onde o conteúdo enviado deve ser armazenado e se um fluxo de trabalho deve ser acionado. O autor do modelo pode usar a caixa de diálogo [de](#design-dialog) design para definir os componentes permitidos e seus mapeamentos semelhantes à caixa de diálogo de design para o contêiner de layout [padrão no editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)de modelo.

>[!NOTE]
>
>Os componentes principais Componente do contêiner de formulário só oferecem suporte ao uso dos componentes principais do formulário (botão, texto, oculto etc.). Não há suporte para o uso de componentes [de](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) alicerce no contêiner de formulário dos componentes principais (e vice-versa).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do contêiner de formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-container-v1.md) | Compatível | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](/help/versions.md)principais.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do contêiner de formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina quais ações serão tomadas quando o componente for enviado.

![](/help/assets/screen_shot_2018-01-12at122046.png)

Dependendo do Tipo **de** ação selecionado, as opções disponíveis no contêiner serão alteradas. Os tipos de ação disponíveis são:

* [Email](#mail)
* [Armazenar conteúdo](#store-content)
* [Enviar pedido](#submit-order)
* [Atualizar pedido](#update-order)

Independentemente do tipo, existem configurações [](#general-settings) gerais que se aplicam a cada ação.

### Email {#mail}

Quando o formulário for enviado, o tipo de ação de email enviará um email aos destinatários designados.

![](/help/assets/screen_shot_2018-01-12at122554.png)

* **Assunto** O assunto do email que será enviado no envio do formulário
* **De** O endereço de email de formulário do email que será enviado no envio do formulário
* **Para** Os endereços dos destinatários que receberão um email após o envio do formulário

   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais
   * Toque ou clique no botão **Excluir** para remover um endereço de email
* **CC** Os endereços dos destinatários que receberão uma cópia de carbono do e-mail enviado após o envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais
   * Toque ou clique no botão **Excluir** para remover um endereço de email

### Armazenar conteúdo {#store-content}

Quando o formulário for enviado, o conteúdo do formulário será armazenado em um local de repositório designado.

![](/help/assets/screen_shot_2018-01-12at122538.png)

* **Caminho** do conteúdo Caminho do repositórioO conteúdo enviado é armazenado
* **Exibir** Toque em Dados ou clique para exibir dados enviados armazenados como JSON
* **Iniciar fluxo de trabalho** Configurar para iniciar um fluxo de trabalho com o conteúdo armazenado como carga após o envio do formulário

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

* Use a caixa de diálogo de seleção para selecionar um recurso no AEM.
* Se a página de agradecimento não estiver no AEM, especifique o URL absoluto. URLs não absolutos serão interpretados em relação ao AEM.
* Deixe em branco para exibir novamente o formulário após o envio.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os componentes permitidos e seus mapeamentos para o contêiner de forma semelhante à caixa de diálogo de design para o contêiner de layout [padrão no editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)de modelo.
