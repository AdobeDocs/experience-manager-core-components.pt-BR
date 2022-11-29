---
title: Usar os componentes principais de email
description: Saiba mais sobre a instalação básica, a configuração e o uso dos Componentes principais de email.
role: Architect, Developer, Admin, User
exl-id: 0e79ca8f-eb0a-4519-b1e8-a9d3b0b99987
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 7%

---


# Usar os componentes principais de email {#using}

Saiba mais sobre a instalação básica, a configuração e o uso dos Componentes principais de email.

## Instalar os componentes principais de email {#installation}

Os Componentes principais de email podem ser usados com o AEM 6.5. Consulte o [Seção Requisitos do documento Introdução dos componentes principais de email](introduction.md#requirements) para obter mais informações.

### Instalar os componentes principais {#core-components}

Os Componentes principais de email são criados nos Componentes principais do AEM. Como os Componentes principais não são fornecidos com o AEM 6.5, primeiro instale os Componentes principais do AEM antes de instalar os Componentes principais de email.

Consulte a seção [Baixe e instale](/help/get-started/using.md#download-and-install) seção do documento Uso de componentes principais para obter detalhes sobre como instalar os componentes principais.

### Instalar os Componentes principais de email {#email-core-components}

Depois que os Componentes principais forem instalados em sua instância, você também deverá instalar os Componentes principais de email. Os Componentes principais do email ainda não fazem parte do Arquétipo de projeto do AEM, portanto, será necessário adicioná-los manualmente ao projeto. Siga a documentação em [o wiki do GitHub dos componentes principais de email para instalar.](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)

Você pode seguir essas mesmas instruções se desejar adaptar um projeto existente para usar os Componentes principais de email.

## Configuração {#configuration}

Depois de instalar os Componentes principais, você deve concluir duas etapas de configuração importantes.

### Configurar Campanha {#configure-campaign}

Você deve configurar a integração AEM-Adobe Campaign para que as duas soluções se comuniquem.

* Configurar a integração do Adobe Campaign
   * Adobe Campaign Classic: [Integração com o Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html)
   * Adobe Campaign Standard: [Integração com o Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html)
* [Vincular a configuração de integração do Adobe Campaign](/help/email/components/page.md#cloud-services-tab) na página de conteúdo, onde você usará os Componentes principais de email

### Adicionar AEM Filtro de Tipo de Recurso para Componentes de Email {#aem-resource-filter}

Para que o Adobe Campaign possa renderizar emails com base nos Componentes principais de email, um filtro deve ser ajustado no Campaign.

1. Faça logon no Adobe Campaign como administrador usando o console do cliente.

1. Selecione **Ferramentas** -> **Explorador** na barra de menus.

1. No explorador, navegue até o **Administração** -> **Plataforma** -> **Opções** nó .

1. Selecione o `AEMResourceTypeFilter` na lista.

1. No **Valor** campo, anexar `core/email/components/page/<v1>/page` se ainda não estiver presente.

   * Substituir `<v1>` com a versão atual dos Componentes principais de email [Componente de página](/help/email/components/page.md) como `v1`.
   * Observe que os valores na variável **Valores** O campo deve ser delimitado por vírgulas.

1. Clique em **Salvar**.

## Usar os componentes principais de email {#using-components}

Depois que os Componentes de email forem instalados e a integração com o Adobe Campaign for configurada, você poderá usar os Componentes de email para criar conteúdo de email no AEM e enviar esse conteúdo para os recipients usando o Adobe Campaign. Veja a seguir uma visão geral do fluxo de trabalho.

| Etapa | Descrição | Solução |
|---|---|---|
| 1 | Os autores criam uma estrutura hierárquica livre de pastas e conteúdo de email como páginas. | AEM |
| 2 | Usar o [editor de modelos,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR) os autores configuram um cabeçalho e/ou rodapé de email que seria compartilhado entre todas as páginas de email resultantes desse modelo de página. | AEM |
| 3 | Os autores usam o [editor de páginas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html) para criar conteúdo de email usando o editor de texto, onde é possível escolher variáveis do Adobe Campaign e usar o Componente de segmentação para exibir informações condicionais se o recipient atender a determinados critérios. | AEM |
| 4 | Quando o conteúdo do email for concluído, [um workflow é executado](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html) para aprovar o conteúdo e enviar para o Campaign. | AEM |
| 5 | Um delivery é criado, definindo uma lista de recipients. | Campaign |
| 6 | O conteúdo criado no AEM é selecionado como o conteúdo do delivery. | Campanha |
| 7 | O conteúdo é enviado para os recipients, substituindo as variáveis do Adobe Campaign pelas informações personalizadas dos recipients. | Campanha |

Para obter um exemplo de criação de conteúdo de email no AEM e entrega no Adobe Campaign, consulte os seguintes recursos.

* AEM 6.5: [Trabalhar com o Adobe Campaign Classic e o Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html)
