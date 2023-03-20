---
title: Componente principal adaptável do Forms - Contêiner de formulário
description: Adicionar um formulário adaptável a uma página da Web.
role: Architect, Developer, Admin, User
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 2%

---


# Contêineres de formulário {#form-container-adaptive-forms-core-component}

O Forms permite que os visitantes do site interajam com o site, fornecendo informações valiosas, que podem aumentar a participação e a satisfação do usuário. Um Contêiner de formulário adaptável no Adobe Experience Manager (AEM) Sites permite que os proprietários de sites adicionem formulários facilmente a suas páginas. Isso ajuda a facilitar a comunicação entre os visitantes do site e o proprietário ou a organização do site, fornecendo uma maneira simplificada para que os visitantes forneçam feedback, façam consultas e concluam outra ação

## Uso {#reasons-to-use-forms-container}

Há vários motivos pelos quais um formulário pode ser adicionado a um site:

* **Coleta de dados**: O Forms pode ser usado para coletar dados de visitantes do site para vários propósitos, como pesquisa de mercado, análise de comportamento do usuário e muito mais.

* **Geração de leads**: Um formulário pode ser usado para coletar informações de clientes potenciais, como nome e endereço de email, para gerar leads para esforços de vendas e marketing.

* **Comércio eletrônico**: O Forms pode ser usado para compras online, permitindo que os clientes façam pedidos e façam pagamentos por meio do site.

* **Contato**: Um formulário de contato permite que os visitantes do site acessem facilmente o proprietário do site ou a organização.

* **Inquéritos e sondagens**: O Forms pode ser usado para coletar comentários e opiniões de visitantes do site por meio de pesquisas e pesquisas.

* **Registro de evento**: O Forms pode ser usado para o registro de eventos, permitindo que os visitantes do site se inscrevam para eventos ou webinars.

* **Subscrições**: O Forms pode ser usado para assinaturas de sites, permitindo que os visitantes se inscrevam para um boletim informativo ou outras comunicações regulares.

* **Autenticação do usuário**: O Forms pode ser usado para autenticação de usuário, permitindo que os visitantes do site criem contas e façam logon para acessar conteúdo ou recursos exclusivos.

* **Aumentar taxa de conversão**: Um formulário bem projetado pode aumentar a taxa de conversão, facilitando para os usuários concluírem uma ação desejada, como comprar um produto ou se inscrever em um serviço.


## Versão e compatibilidade {#version-and-compatibility}

O Componente principal Adaptive Forms Accordion foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, AEM compatibilidade e links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com<br>[versão 2.0.4](/help/adaptive-forms/version.md) e posterior | Compatível com<br>[versão 1.1.12](/help/adaptive-forms/version.md) e posterior, mas inferior a 2.0.0. |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/adaptive-forms/version.md) documento.
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal do contêiner adaptável Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do contêiner de formulário para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de contêiner de formulário com facilidade para uma experiência do usuário contínua.

### Guia básica {#basic-tab}

![Guia Básica](/help/adaptive-forms/assets/formcontainer_basictab.png)

* **Serviços de pré-preenchimento** - Essa opção permite que o usuário selecione um serviço de preenchimento prévio para recuperar dados quando o Formulário adaptável for renderizado. Saiba mais sobre [como criar e configurar um serviço de preenchimento prévio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=en#aem-forms-custom-prefill-service).

* **Categoria Biblioteca do cliente** - O usuário pode configurar uma biblioteca JavaScript personalizada por Formulário adaptável. É recomendável manter somente as funções reutilizáveis na biblioteca, que têm dependência em bibliotecas de terceiros jquery e underscore.js.

### Guia Submissão {#submission-tab}

![Guia Submissão](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

Os usuários podem configurar ações diferentes para os envios de um formulário adaptável.

* **Redirecionar URL/caminho** - Essa opção permite que o usuário configure uma página para cada formulário, para a qual os usuários do formulário são redirecionados após enviar um formulário adaptável. Clique aqui para obter mais informações sobre [como configurar páginas de redirecionamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html).

![Guia Mostrar mensagem](/help/adaptive-forms/assets/formconatiner_showmessage.png)

* **Mostrar mensagem** - Essa opção permite que os usuários adicionem uma mensagem exibida quando o formulário adaptável for enviado com sucesso. O texto predefinido é incluído na caixa de diálogo e pode ser modificado pelo usuário. A caixa de diálogo Mostrar mensagem oferece suporte a ferramentas de formatação de rich text que permitem que os usuários formatem o texto adicionado.

* **Enviar ação** - Uma ação Enviar é acionada quando um usuário clica no botão Enviar em um formulário adaptável. Os usuários podem selecionar Enviar ações na lista suspensa que são compatíveis imediatamente. Saiba como [configurar uma Ação de envio na guia Enviar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#supporting-custom-functions-in-validation-expressions-br).
