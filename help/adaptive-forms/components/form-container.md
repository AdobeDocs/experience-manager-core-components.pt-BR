---
title: 'Componente principal de formulários adaptáveis: container de formulário'
description: Adicionar um formulário adaptável a uma página da web.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 8bba79956a04020647d5d04f9fe6fa674affedf1
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 97%

---

# Contêiner de formulário {#form-container-adaptive-forms-core-component}

O Forms permite que os visitantes do site interajam com o site fornecendo informações valiosas, que podem aumentar o engajamento e a satisfação do usuário. No Adobe Experience Manager Sites (AEM Sites), um container de formulário adaptável permite que os proprietários de sites adicionem formulários facilmente a suas páginas. Isso ajuda a facilitar a comunicação entre os visitantes do site e o proprietário ou a organização, oferecendo uma maneira simplificada para que os visitantes forneçam feedback, façam consultas e realizem outras ações.

## Uso {#reasons-to-use-forms-container}

Há vários motivos pelos quais um formulário pode ser adicionado a um site:
- **Coleção de dados**: o Forms pode ser usado para coletar dados de visitantes do site para vários propósitos, como pesquisa de mercado, análise de comportamento dos usuários e muito mais.

- **Geração de clientes potenciais**: um formulário pode ser usado para coletar informações de clientes potenciais, como nome e endereço de email, a fim de gerar leads para as iniciativas de vendas e marketing.

- **Comércio eletrônico**: o Forms pode ser usado para compras online, permitindo que os clientes façam pedidos e pagamentos por meio do site.

- **Contato**: um formulário de contato permite que os visitantes do site entrem em contato com o proprietário ou a organização de maneira fácil.

- **Pesquisas e votações**: o Forms pode ser usado para coletar comentários e opiniões de visitantes do site por meio de pesquisas e votações.

- **Registro em evento**: o Forms pode ser usado para o registro em eventos, permitindo que os visitantes do site se inscrevam em eventos ou webinários.

- **Assinaturas**: o Forms pode ser usado para assinaturas de sites, permitindo que os visitantes se inscrevam em boletins informativos ou outras comunicações regulares.

- **Autenticação de usuários**: o Forms pode ser usado para a autenticação de usuários, permitindo que os visitantes do site criem contas e façam logon para acessar conteúdo ou recursos exclusivos.

- **Aumentar a taxa de conversão**: um formulário bem projetado pode aumentar a taxa de conversão, tornando fácil para os usuários concluírem uma ação desejada, como comprar um produto ou se inscrever em um serviço.

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

- **Título**: Com o Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Serviços de preenchimento prévio**: essa opção permite que o usuário selecione um serviço de preenchimento prévio para recuperar dados quando o formulário adaptável for renderizado. Saiba mais sobre [como criar e configurar um serviço de preenchimento prévio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=pt-BR#aem-forms-custom-prefill-service).

- **Categoria de biblioteca do cliente**: o usuário pode configurar uma biblioteca JavaScript personalizada por formulário adaptável. É recomendável manter somente as funções reutilizáveis na biblioteca, que dependem das bibliotecas de terceiros de jquery e underscore.js.
Às vezes, se houver **regras de validação complexas**, o script de validação exato residirá em funções personalizadas, e os usuários chamam essas funções personalizadas a partir da expressão de validação do campo. Para tornar essa biblioteca de funções personalizadas conhecida e disponível ao executar validações no servidor, usuários do formulário podem configurar o nome da biblioteca do cliente do AEM na guia **[!UICONTROL Básico]** das propriedades de container de formulários adaptáveis, conforme mostrado abaixo.

Usuários podem configurar a biblioteca customJavaScript para cada formulário adaptável. Na biblioteca, mantenha somente as funções reutilizáveis, que dependem de bibliotecas de terceiros de jquery e underscore.js.

### Guia Modelo de dados {#data-model-tab}

![Guia Enviar](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Você pode usar o modelo de dados do formulário e conectar um formulário a uma fonte de dados para enviar e receber dados com base nas ações do usuário. Também é possível conectar um formulário a um esquema JSON para receber os dados enviados em um formato predefinido. De acordo com os requisitos, conecte o formulário a um esquema JSON ou modelo de dados do formulário:
- Crie um esquema JSON e faça upload para o seu ambiente
- Criar um modelo de dados do formulário

### Guia Enviar {#submission-tab}

Os usuários podem configurar ações diferentes para o envio de um formulário adaptável.

- **URL/caminho de redirecionamento**: essa opção permite que o usuário configure uma página em cada formulário, para a qual os usuários do formulário são redirecionados após enviar o formulário adaptável. Clique aqui para obter mais informações sobre [como configurar páginas de redirecionamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=pt-BR).

![Guia Enviar](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Mostrar mensagem**: essa opção permite que os usuários adicionem uma mensagem que é exibida quando o formulário adaptável é enviado com sucesso. O texto predefinido é incluído na caixa de diálogo e pode ser modificado pelo usuário. A caixa de diálogo Mostrar mensagem é compatível com as ferramentas de formatação de rich text que permitem que os usuários formatem o texto adicionado.

![Guia Mostrar mensagem](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Ação de envio**: uma ação de envio é acionada quando um usuário clica no botão Enviar em um formulário adaptável. Na lista suspensa, os usuários podem selecionar ações de envio que são compatíveis de fábrica. Saiba como [configurar uma ação de envio na guia Enviar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=pt-BR#supporting-custom-functions-in-validation-expressions-br).

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar estilos CSS do componente de Container do formulário.

### Guia Componentes permitidos {#allowed-components-tab}

![Guia Componentes permitidos da caixa de diálogo de design](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

A variável **Componentes permitidos** permite que o editor de modelo defina os componentes que podem ser adicionados como itens aos painéis no componente no editor Forms adaptável.

### Guia Componentes padrão {#default-components-tab}

![Guia Componentes padrão da caixa de diálogo de design](/help/adaptive-forms/assets/formcontainer-defaultcomponents.png)

A guia **Componentes padrão** permite que o editor de modelos especifique os componentes que estarão visíveis por padrão como itens no componente de container do formulário no editor de formulários adaptáveis.

### Guia Configurações responsivas {#responsive-tab}

![Guia Configurações responsivas da caixa de diálogo de design](/help/adaptive-forms/assets/formcontainer-responsivestyle.png)

A guia **Configurações responsivas** permite que o editor de modelos especifique o número de colunas na grade do componente de container do formulário no editor de formulários adaptáveis.

### Guia Estilos {#styles-tab}

O componente principal de anexo de arquivo de formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **Classes padrão do CSS**: você pode fornecer uma classe padrão do CSS ao componente principal container para formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Guia Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de chave e valor) a um componente principal de formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: toque ou clique e arraste para alterar a ordem do nome e do valor da propriedade personalizada.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}