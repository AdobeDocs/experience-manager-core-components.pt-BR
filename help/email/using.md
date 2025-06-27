---
title: Utilização dos Componentes principais de email
description: 'Saiba mais sobre a instalação básica, a configuração e o uso dos Componentes principais de email. '
role: Architect, Developer, Admin, User
exl-id: 0e79ca8f-eb0a-4519-b1e8-a9d3b0b99987
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '610'
ht-degree: 100%

---


# Utilização dos Componentes principais de email {#using}

Saiba mais sobre a instalação básica, a configuração e o uso dos Componentes principais de email. 

## Instalar os Componentes principais de email {#installation}

Os Componentes principais de email podem ser utilizados com o AEM 6.5. Consulte a [seção de requisitos do documento de Introdução aos componentes principais de email](introduction.md#requirements) para obter mais informações.

### Instalar os Componentes principais {#core-components}

Os Componentes principais de email são criados por meio dos Componentes principais do AEM. Visto que os componentes principais não são fornecidos com o AEM 6.5, você deve instalar os componentes principais do AEM antes de instalar os componentes principais de email.

Consulte a seção [Baixar e instalar](/help/get-started/using.md#download-and-install) do documento Uso dos componentes principais para obter detalhes sobre como instalar os componentes principais.

### Instalar os componentes principais de email {#email-core-components}

Após instalar os componentes principais em sua instância, você também deve instalar os componentes principais de email. Os componentes principais de email ainda não fazem parte do Arquétipo de projeto do AEM, portanto, você precisará adicioná-los manualmente ao seu projeto. Siga a documentação do [wiki do GitHub sobre os componentes principais de email para a instalação.](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)

Você pode seguir estas mesmas instruções se desejar adaptar um projeto existente para utilizar os componentes principais de email.

## Configuração {#configuration}

Após instalar os componentes principais, você deve concluir duas etapas de configuração importantes.

### Configurar o Campaign {#configure-campaign}

Você deve configurar a integração do AEM com o Adobe Campaign para que as duas soluções se comuniquem.

* Configurar sua integração do Adobe Campaign
   * Adobe Campaign Classic: [Integração com o Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html?lang=pt-BR) 
   * Adobe Campaign Standard: [Integração com o Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=pt-BR) 
* [Vincule a configuração de integração do Adobe Campaign](/help/email/components/page.md#cloud-services-tab) à página de conteúdo na qual você usará os componentes principais de email

### Adicionar um Filtro de tipo de recurso do AEM para componentes de email {#aem-resource-filter}

Para que o Adobe Campaign possa renderizar emails com base nos componentes principais de email, um filtro deve ser configurado no Campaign.

1. Faça logon no Adobe Campaign como administrador usando o console do cliente.

1. Selecione **Ferramentas** -> **Explorador** na barra de menus.

1. No explorador, navegue até o nó **Administração** > **Plataforma** > **Opções**.

1. Selecione a opção `AEMResourceTypeFilter` na lista.

1. No campo **Valor**, adicione `core/email/components/page/<v1>/page`, se ainda não estiver presente.

   * Substitua `<v1>` pela versão atual do [Componente de página](/help/email/components/page.md) dos componentes principais de email, como a `v1`.
   * Observe que os valores no campo **Valores** devem ser delimitados com vírgulas.

1. Clique em **Salvar**.

## Utilização dos Componentes principais de email {#using-components}

Após instalar os componentes de email e configurar a integração com o Adobe Campaign, você pode usar os componentes de email para criar conteúdo de email no AEM e depois enviar esse conteúdo aos destinatários usando o Adobe Campaign. Veja a seguir uma visão geral do fluxo de trabalho. 

| Etapa | Descrição | Solução |
|---|---|---|
| 1 | Os autores criam uma estrutura hierárquica livre de pastas e conteúdo de email no formato de páginas. | AEM |
| 2 | Ao utilizar o [editor de modelos,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR) os autores configuram um cabeçalho e/ou rodapé de email que pode ser compartilhado entre todas as páginas de email resultantes deste modelo de página. | AEM |
| 3 | Os autores utilizam o [editor de páginas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html?lang=pt-BR) para criar conteúdo de email com o editor de texto, onde é possível escolher variáveis do Adobe Campaign e usar o componente de segmentação para exibir informações condicionais se o destinatário atender a determinados requisitos. | AEM |
| 4 | Quando a criação do conteúdo de email é concluída, [um fluxo de trabalho é executado](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html?lang=pt-BR) para aprovar o conteúdo e enviar para o Campaign. | AEM |
| 5 | Uma entrega é criada e uma lista de destinatários é definida. | Campaign |
| 6 | O conteúdo criado no AEM é selecionado como o conteúdo da entrega. | Campaign |
| 7 | O conteúdo é enviado para os destinatários, substituindo as variáveis do Adobe Campaign pelas informações personalizadas dos destinatários. | Campaign |

Para obter um exemplo do processo de criação de conteúdo de email no AEM e entrega no Adobe Campaign, consulte os seguintes recursos.

* AEM 6.5: [Trabalho com o Adobe Campaign Classic e Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html?lang=pt-BR)
