---
title: Componente de Container de formulário
description: O Componente principal de Container de formulário permite a criação de formulários simples de envio.
translation-type: tm+mt
source-git-commit: 499047a8c15a6423a56b370f41fd020740481f80
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 2%

---


# Componente de Container de formulário {#form-container-component}

O Componente principal de Container de formulário permite a criação de formulários simples de envio.

## Uso {#usage}

O componente de Container de formulário permite a criação de formulários e recursos simples de envio de informações, ao suportar formulários WCM simples e ao usar uma estrutura aninhada para permitir componentes de formulário adicionais.

Ao usar a caixa de diálogo [](#configure-dialog) configurar, o editor de conteúdo pode definir a ação acionada pelo envio do formulário, o URL que deve lidar com o envio e se um fluxo de trabalho deve ser acionado. O autor do modelo pode usar a caixa de diálogo [de](#design-dialog) design para definir os componentes permitidos e seus mapeamentos semelhantes à caixa de diálogo de design para o container de layout [padrão no editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)de modelo.

>[!NOTE]
>
>Os componentes principais Componente do Container de formulário só oferecem suporte ao uso dos componentes principais do formulário (botão, texto, oculto etc.). Não há suporte para o uso de componentes [de](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) fundação e componentes de formulário dentro do container de formulário dos componentes principais (e vice-versa).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do Container de formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-container-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o componente Container de formulário e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_form_container)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Container de formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina quais ações serão tomadas quando o componente for enviado.

Dependendo do Tipo **de** ação selecionado, as opções disponíveis no container serão alteradas. Os tipos de ação disponíveis são:

* [Dados do formulário de publicação](#post-data)
* [Email](#mail)
* [Armazenar conteúdo](#store-content)

Independentemente do tipo, existem configurações [](#general-settings) gerais que se aplicam a cada ação.

### Dados do formulário de publicação {#post-data}

Quando o formulário for submetido, o tipo de ação de dados do formulário posterior transmitirá os dados enviados a terceiros como JSON para processamento.

![Opções de publicação de dados de formulário na caixa de diálogo de edição do componente Container de formulário](/help/assets/form-container-edit-post.png)

* **Endpoint** - o serviço HTTPS totalmente qualificado que processará os dados
* **Mensagem** de erro - mensagem a ser exibida se o envio não for bem-sucedido

>[!TIP]
>Há opções adicionais de tempo limite que um administrador do sistema pode ajustar para lidar com o processamento de dados de formulário encaminhados. [Consulte a documentação técnica do GitHub para obter mais informações.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### Email {#mail}

Quando o formulário for enviado, o tipo de ação de email enviará um email para os recipient designados.

![Opções de e-mail na caixa de diálogo de edição do Componente do Container de formulário](/help/assets/form-container-edit-mail.png)

* **Assunto** - O assunto do email que será enviado no envio do formulário
* **De** - O endereço de email de formulário do email que será enviado no envio do formulário
* **Para** - Os endereços dos recipient que receberão um email após o envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais
   * Toque ou clique no botão **Excluir** para remover um endereço de email
* **CC** - Os endereços dos recipient que receberão uma cópia de carbono do e-mail enviado após o envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais
   * Toque ou clique no botão **Excluir** para remover um endereço de email

### Armazenar conteúdo {#store-content}

Quando o formulário for enviado, o conteúdo do formulário será armazenado em um local de repositório designado.

![Armazenar opções de conteúdo na caixa de diálogo de edição do Container de formulário](/help/assets/form-container-edit-store.png)

* **Caminho** do conteúdo - Caminho do repositório do conteúdo no qual o conteúdo enviado é armazenado
* **Dados** de visualização - Toque ou clique para visualização de dados enviados armazenados como JSON
* **Fluxo de trabalho** do start - Configure para start de um fluxo de trabalho com o conteúdo armazenado como carga após o envio do formulário

>[!NOTE]
>
>Para tornar o gerenciamento de dados de usuários mais simples e impor a separação de preocupações, geralmente não é recomendado armazenar conteúdo gerado pelo usuário no repositório.
>
>Em vez disso, use o tipo de ação [Publicar dados](#post-data) do formulário para passar o conteúdo do usuário para um provedor de serviço dedicado.

### Configurações gerais {#general-settings}

Independentemente do tipo de ação selecionado, uma página de agradecimento sempre pode ser definida.

![Opções gerais na caixa de diálogo de edição do Componente do Container de formulário](/help/assets/form-container-edit-general.png)

* **Página** de agradecimento - o usuário será redirecionado para a página especificada após a conclusão do envio do formulário.
   * Use a caixa de diálogo Seleção para selecionar um recurso dentro do AEM.
   * Se a página de agradecimento não estiver em AEM, especifique o URL absoluto. URLs não absolutos serão interpretados em relação ao AEM.
   * Deixe em branco para exibir novamente o formulário após o envio.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os componentes permitidos e seus mapeamentos para o container de forma semelhante à caixa de diálogo de design para o container de layout [padrão no editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)de modelo.

### Guia Estilos {#styles-tab}

O componente Container de formulário suporta o sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
