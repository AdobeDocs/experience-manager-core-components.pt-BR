---
title: Componente do contêiner de formulário
description: O Componente de contêiner de formulário do componente principal permite a criação de formulários de envio simples.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 2%

---


# Componente do contêiner de formulário {#form-container-component}

O Componente de contêiner de formulário do componente principal permite a criação de formulários de envio simples.

## Uso {#usage}

O Componente de contêiner de formulário permite a criação de formulários e recursos simples de envio de informações, com o suporte a formulários WCM simples e o uso de uma estrutura aninhada para permitir componentes de formulário adicionais.

Ao usar o [configure dialog](#configure-dialog), o editor de conteúdo pode definir a ação acionada pelo envio do formulário, o URL que deve lidar com o envio e se um workflow deve ser acionado. O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir os componentes permitidos e seus mapeamentos semelhantes à caixa de diálogo de design para o [contêiner de layout padrão no editor de modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Os componentes principais do Componente do contêiner de formulário são compatíveis apenas com o uso dos componentes principais do formulário (botão, texto, oculto, etc.). Não há suporte para o uso de [componentes de base](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) nos componentes principais do contêiner de formulário (e vice-versa).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do contêiner de formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-container-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente do contêiner de formulário, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_container).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do contêiner de formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina quais ações serão executadas quando o componente for enviado.

Dependendo do **Tipo de ação** selecionado, as opções disponíveis no contêiner serão alteradas. Os tipos de ação disponíveis são:

* [Dados do formulário de postagem](#post-data)
* [Email](#mail)
* [Armazenar conteúdo](#store-content)

Independentemente do tipo , há [configurações gerais](#general-settings) que se aplicam a cada ação.

### Dados do formulário posterior {#post-data}

Quando o formulário for enviado, o tipo de ação pós-formulário de dados passará os dados enviados para terceiros como JSON para processamento.

![Opções Publicar dados do formulário na caixa de diálogo Editar do componente Contêiner de formulário](/help/assets/form-container-edit-post.png)

* **Endpoint**  — O serviço HTTPS totalmente qualificado que processará os dados
* **Mensagem de erro**  - Mensagem a ser exibida se o envio não for bem-sucedido

>[!TIP]
>Há opções de tempo limite adicionais que um administrador de sistema pode ajustar para lidar com o processamento de dados de formulário encaminhados. [Consulte a documentação técnica no GitHub para obter mais informações.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### Email {#mail}

Quando o formulário for enviado, o tipo de ação de email enviará um email para os recipients designados.

![Opções de email na caixa de diálogo de edição do Componente do contêiner de formulário](/help/assets/form-container-edit-mail.png)

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

![Armazenar opções de conteúdo na caixa de diálogo de edição do Contêiner de formulário](/help/assets/form-container-edit-store.png)

* **Caminho do conteúdo**  - Caminho do repositório do conteúdo onde o conteúdo enviado é armazenado
* **Exibir dados**  - Toque ou clique para exibir os dados enviados armazenados como JSON
* **Iniciar fluxo de trabalho**  - Configurar para iniciar um fluxo de trabalho com o conteúdo armazenado como carga útil no envio do formulário

>[!NOTE]
>
>Para tornar o gerenciamento de dados de usuários mais simples e impor a separação de preocupações, geralmente não é recomendado armazenar conteúdo gerado pelo usuário no repositório.
>
>Em vez disso, use o tipo de ação [Postar dados do formulário](#post-data) para passar o conteúdo do usuário para um provedor de serviços dedicado.

### Configurações gerais {#general-settings}

Independentemente do tipo de ação selecionada, uma página de agradecimento sempre pode ser definida.

![Opções gerais na caixa de diálogo de edição do Componente do contêiner de formulário](/help/assets/form-container-edit-general.png)

* **Página de agradecimento**  - O usuário será redirecionado para a página especificada após a conclusão do envio do formulário.
   * Use a caixa de diálogo de seleção para selecionar um recurso dentro do AEM.
   * Se a página de agradecimento não estiver em AEM, especifique o URL absoluto. URLs não absolutos serão interpretados de acordo com AEM.
   * Deixe em branco para exibir novamente o formulário após o envio.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os componentes permitidos e seus mapeamentos para o contêiner semelhante à caixa de diálogo de design para o [contêiner de layout padrão no editor de modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Guia Estilos {#styles-tab}

O Componente do contêiner de formulário oferece suporte ao AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).
