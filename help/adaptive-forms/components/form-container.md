---
title: 'Componente principal de formulários adaptáveis: container de formulário'
description: Adicionar um formulário adaptável a uma página da web.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 100%

---

# Container de formulário {#form-container-adaptive-forms-core-component}

O Forms permite que os visitantes do site interajam com o site fornecendo informações valiosas, que podem aumentar o engajamento e a satisfação do usuário. No Adobe Experience Manager Sites (AEM Sites), um container de formulário adaptável permite que os proprietários de sites adicionem formulários facilmente a suas páginas. Isso ajuda a facilitar a comunicação entre os visitantes do site e o proprietário ou a organização, oferecendo uma maneira simplificada para que os visitantes forneçam feedback, façam consultas e realizem outras ações.

## Uso {#reasons-to-use-forms-container}

Há vários motivos pelos quais um formulário pode ser adicionado a um site:

* **Coleção de dados**: o Forms pode ser usado para coletar dados de visitantes do site para vários propósitos, como pesquisa de mercado, análise de comportamento dos usuários e muito mais.

* **Geração de clientes potenciais**: um formulário pode ser usado para coletar informações de clientes potenciais, como nome e endereço de email, a fim de gerar leads para as iniciativas de vendas e marketing.

* **Comércio eletrônico**: o Forms pode ser usado para compras online, permitindo que os clientes façam pedidos e pagamentos por meio do site.

* **Contato**: um formulário de contato permite que os visitantes do site entrem em contato com o proprietário ou a organização de maneira fácil.

* **Pesquisas e votações**: o Forms pode ser usado para coletar comentários e opiniões de visitantes do site por meio de pesquisas e votações.

* **Registro em evento**: o Forms pode ser usado para o registro em eventos, permitindo que os visitantes do site se inscrevam em eventos ou webinários.

* **Assinaturas**: o Forms pode ser usado para assinaturas de sites, permitindo que os visitantes se inscrevam em boletins informativos ou outras comunicações regulares.

* **Autenticação de usuários**: o Forms pode ser usado para a autenticação de usuários, permitindo que os visitantes do site criem contas e façam logon para acessar conteúdo ou recursos exclusivos.

* **Aumentar a taxa de conversão**: um formulário bem projetado pode aumentar a taxa de conversão, tornando fácil para os usuários concluírem uma ação desejada, como comprar um produto ou se inscrever em um serviço.


## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal de container de formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Para obter mais informações sobre o desenvolvimento dos componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do container de formulário para visitantes com a caixa de diálogo de configuração. Você também pode definir opções de container de formulário com facilidade para uma experiência de usuário perfeita.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/formcontainer_basictab.png)

* **Serviços de preenchimento prévio**: essa opção permite que o usuário selecione um serviço de preenchimento prévio para recuperar dados quando o formulário adaptável for renderizado. Saiba mais sobre [como criar e configurar um serviço de preenchimento prévio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=pt-BR#aem-forms-custom-prefill-service).

* **Categoria de biblioteca do cliente**: o usuário pode configurar uma biblioteca JavaScript personalizada por formulário adaptável. É recomendável manter somente as funções reutilizáveis na biblioteca, que dependem das bibliotecas de terceiros de jquery e underscore.js.

### Guia Enviar {#submission-tab}

![Guia Enviar](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

Os usuários podem configurar ações diferentes para o envio de um formulário adaptável.

* **URL/caminho de redirecionamento**: essa opção permite que o usuário configure uma página em cada formulário, para a qual os usuários do formulário são redirecionados após enviar o formulário adaptável. Clique aqui para obter mais informações sobre [como configurar páginas de redirecionamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=pt-BR).

![Guia Mostrar mensagem](/help/adaptive-forms/assets/formconatiner_showmessage.png)

* **Mostrar mensagem**: essa opção permite que os usuários adicionem uma mensagem que é exibida quando o formulário adaptável é enviado com sucesso. O texto predefinido é incluído na caixa de diálogo e pode ser modificado pelo usuário. A caixa de diálogo Mostrar mensagem é compatível com as ferramentas de formatação de rich text que permitem que os usuários formatem o texto adicionado.

* **Ação de envio**: uma ação de envio é acionada quando um usuário clica no botão Enviar em um formulário adaptável. Na lista suspensa, os usuários podem selecionar ações de envio que são compatíveis de fábrica. Saiba como [configurar uma ação de envio na guia Enviar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=pt-BR#supporting-custom-functions-in-validation-expressions-br).

## Artigo relacionado {#related-article}

* [Criar um formulário adaptável em uma página do AEM Sites ou fragmento de experiência](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=pt-BR)

* [Criar um formulário adaptável independente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=pt-BR)


>[!MORELIKETHIS]
>
>* [Acordeão](/help/adaptive-forms/components/accordion.md)
>* [Botão](/help/adaptive-forms/components/button.md)
>* [Grupo de Caixa de seleção](/help/adaptive-forms/components/checkbox-group.md)
>* [Seletor de data](/help/adaptive-forms/components/date-picker.md)
>* [Lista suspensa](/help/adaptive-forms/components/drop-down.md)
>* [Entrada de email](/help/adaptive-forms/components/email-input.md)
>* [Anexo de arquivo](/help/adaptive-forms/components/file-attachment.md)
>* [Rodapé](/help/adaptive-forms/components/footer.md)
>* [Cabeçalho](/help/adaptive-forms/components/header.md)
>* [Guias horizontais](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Imagem](/help/adaptive-forms/components/image.md)
>* [Entrada de número](/help/adaptive-forms/components/number-input.md)
>* [Container do painel](/help/adaptive-forms/components/panel-container.md)
>* [Botão de opção](/help/adaptive-forms/components/radio-button.md)
>* [Botão Redefinir](/help/adaptive-forms/components/reset-button.md)
>* [Botão Enviar](/help/adaptive-forms/components/submit-button.md)
>* [Entrada de telefone](/help/adaptive-forms/components/telephone-input.md)
>* [Entrada de texto](/help/adaptive-forms/components/text-input.md)
>* [Texto](/help/adaptive-forms/components/text.md)
>* [Título](/help/adaptive-forms/components/title.md)
>* [Assistente](/help/adaptive-forms/components/wizard.md)

## Consulte também {#see-also}

{{see-also}}