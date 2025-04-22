---
title: Componente de Contêiner de formulário
description: O componente de Contêiner de formulário, dos Componentes principais, permite a criação de formulários de envio simples.
role: Architect, Developer, Admin, User
exl-id: 552f9dd5-6a3a-42d9-9969-e62a1f36e811
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 99%

---

# Componente de Contêiner de formulário {#form-container-component}

O componente de Contêiner de formulário, dos Componentes principais, permite a criação de formulários de envio simples.

## Uso {#usage}

O componente de Contêiner de formulário permite a criação de formulários e recursos simples de envio de informações, com o suporte a formulários WCM simples e o uso de uma estrutura aninhada para permitir componentes de formulário adicionais.

Ao usar a [caixa de diálogo de configuração](#configure-dialog), o editor de conteúdo pode definir a ação acionada pelo envio do formulário, o URL que deve lidar com o envio e se um fluxo de trabalho deve ser acionado. O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir os componentes permitidos e seus mapeamentos, semelhantes à caixa de diálogo de design para o [contêiner de layout padrão no editor de modelo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR).

>[!NOTE]
>
>O componente de Contêiner de formulário, dos Componentes principais, suporta somente o uso de outros componentes de formulário dos componente principais (botão, texto, oculto etc.). Não há suporte para o uso de componentes de formulários de [componentes de base](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html?lang=pt-BR) dentro do componente de contêiner de formulário (e vice-versa).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Contêiner de formulário é a v2, introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Compatível com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-container-v1.md) | Compatível | Compatível | - | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Contêiner de Formulário, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_form_container_br).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Contêiner de formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina que ações serão executadas quando o componente for enviado.

Dependendo do **Tipo de ação** selecionado, as opções disponíveis no contêiner serão alteradas. Os tipos de ação disponíveis são:

* [Publicar dados de formulário](#post-data)
* [Email](#mail)
* [Armazenar conteúdo](#store-content)

Independentemente do tipo, há [configurações gerais](#general-settings) que se aplicam a cada ação.

### Publicar dados de formulário {#post-data}

Quando o formulário for enviado, o tipo de ação pós-formulário de dados passará os dados enviados para terceiros como JSON para processamento.

![Opções Publicar dados do formulário, na caixa de diálogo de edição do componente Contêiner de formulário](/help/assets/form-container-edit-post.png)

* **Endpoint** - O serviço HTTPS totalmente qualificado que processará os dados
* **Mensagem de erro** - Mensagem a ser exibida se o envio não for bem-sucedido

>[!TIP]
>Há opções de tempo limite adicionais que um administrador de sistema pode ajustar para lidar com o processamento de dados de formulário encaminhados. [Consulte a documentação técnica no GitHub para obter informações.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### Email {#mail}

Quando o formulário for enviado, o tipo de ação de email enviará um email para os destinatários designados.

![Opções de email na caixa de diálogo de edição do componente do Contêiner de formulário](/help/assets/form-container-edit-mail.png)

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

![Armazenar opções de conteúdo na caixa de diálogo de edição do Contêiner de formulário](/help/assets/form-container-edit-store.png)

* **Caminho de conteúdo** - Caminho do repositório do conteúdo repositório onde o conteúdo enviado está armazenado
* **Exibir dados** - Toque ou clique para exibir os dados enviados armazenados como JSON
* **Iniciar fluxo de trabalho** - Configurar para iniciar um fluxo de trabalho com o conteúdo armazenado como carga útil no envio do formulário

>[!NOTE]
>
>Para tornar o gerenciamento de dados de usuários mais simples e impor a separação de preocupações, geralmente não é recomendado armazenar conteúdo gerado pelo usuário no repositório.
>
>Em vez disso, use o tipo de ação [Postar dados do formulário](#post-data) para passar o conteúdo do usuário para um provedor de serviços dedicado.

### Configurações gerais {#general-settings}

Independentemente do tipo de ação selecionada, uma página de agradecimento sempre pode ser definida.

![Opções gerais na caixa de diálogo de edição do componente de Contêiner de formulário](/help/assets/form-container-edit-general.png)

* **Página de agradecimento** - O usuário será redirecionado para a página especificada após a conclusão do envio do formulário.
   * Use a caixa de diálogo de seleção para selecionar um recurso dentro do AEM.
   * Se a página de agradecimento não estiver no AEM, especifique o URL absoluto. URLs não absolutos serão interpretados de acordo com o AEM.
   * Deixe em branco para exibir o formulário novamente após o envio.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os componentes permitidos e seus mapeamentos para o contêiner semelhante à caixa de diálogo de design para o [contêiner de layout padrão no editor de modelo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR).

### Guia Estilos {#styles-tab}

O componente de Contêiner de formulário é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
