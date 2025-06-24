---
title: 'Componente principal de formulários adaptáveis: container de formulário'
description: Adicionar um formulário adaptável a uma página da web.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '1524'
ht-degree: 97%

---


# Container de formulário {#form-container-adaptive-forms-core-component}

<span class="preview"> Este artigo discute o recurso **Rascunhos** <!--and **Hamburger Menu Support** -->, que é um recurso de pré-lançamento. O recurso de pré-lançamento pode ser acessado somente por meio do [canal de pré-lançamento](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/prerelease#new-features).</span>

O Forms permite que os visitantes do site interajam com o site fornecendo informações valiosas, que podem aumentar o engajamento e a satisfação do usuário. No Adobe Experience Manager Sites (AEM Sites), um container de formulário adaptável permite que os proprietários de sites adicionem formulários facilmente a suas páginas. Isso ajuda a facilitar a comunicação entre os visitantes do site e o proprietário ou a organização, oferecendo uma maneira simplificada para que os visitantes forneçam feedback, façam consultas e realizem outras ações

{{traditional-aem}}

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

O componente principal Adaptive Forms Accordion foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM Forms 6.5.16.0 ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_br). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal de container de formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Para obter mais informações sobre o desenvolvimento dos componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do container de formulário para visitantes com a caixa de diálogo de configuração. Você também pode definir opções de container de formulário com facilidade para uma experiência de usuário perfeita.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **Título**: o título permite identificar facilmente um componente em um formulário; por padrão, ele aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Serviços de preenchimento prévio**: essa opção permite que o usuário selecione um serviço de preenchimento prévio para recuperar dados quando o formulário adaptável for renderizado. Saiba mais sobre [como criar e configurar um serviço de pré-preenchimento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=pt-BR#aem-forms-custom-prefill-service).

- **Função**: a função é um atributo HTML usado para especificar a finalidade de um elemento HTML para tecnologias de assistência, como leitores de tela. O atributo de função é usado para fornecer contexto e significado semântico adicionais a um elemento, facilitando a interpretação e o anúncio do conteúdo pelos leitores de tela. Por exemplo, no AEM Forms, o rótulo de um campo de formulário pode ter a função de “rótulo” e seu campo de entrada pode ter a função de “caixa de texto”. Isso ajuda o leitor de tela a entender a relação entre o rótulo e o campo de entrada e anunciá-los corretamente ao usuário.

- **Categoria de biblioteca do cliente**: o usuário pode configurar uma biblioteca JavaScript personalizada por formulário adaptável. É recomendável manter somente as funções reutilizáveis na biblioteca, que dependem das bibliotecas de terceiros de jquery e underscore.js.
Às vezes, se houver **regras de validação complexas**, o script de validação exato residirá em funções personalizadas, e os usuários chamam essas funções personalizadas a partir da expressão de validação do campo. Para tornar esta biblioteca de funções personalizadas conhecida e disponível durante a execução de validações do lado do servidor, o usuário do formulário pode configurar o nome da biblioteca do cliente do AEM na guia **[!UICONTROL Básico]** das propriedades do Container de formulários adaptáveis.
Usuários podem configurar a biblioteca customJavaScript para cada formulário adaptável. Na biblioteca, mantenha somente as funções reutilizáveis, que dependem de bibliotecas de terceiros de jquery e underscore.js.

<!--
- **Enable the hamburger menu for mobile view** - Select the checkbox to integrate a hamburger menu into your form for mobile view. Represented by three horizontal lines stacked vertically, this menu provides a clear and uncluttered display for panels on smaller devices, especially on mobile devices. For more information about the hamburger menu, refer to the [Learn more about the hamburger menu](#learn-more-about-the-hamburger-menu) section. -->


### Guia Modelo de dados {#data-model-tab}

![Guia Enviar](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Você pode usar o modelo de dados do formulário e conectar um formulário a uma fonte de dados para enviar e receber dados com base nas ações do usuário. Também é possível conectar um formulário a um esquema JSON para receber os dados enviados em um formato predefinido. De acordo com os requisitos, conecte o formulário a um esquema JSON ou modelo de dados do formulário:
- Crie um esquema JSON e faça upload para o seu ambiente
- Criar um modelo de dados do formulário

### Rascunhos

![Guia Enviar](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **Salvar rascunhos automaticamente**: marque a caixa de seleção **Salvar rascunhos automaticamente** para habilitar o salvamento de formulários como rascunhos.
- **Salvar preferência**: Configure a opção **Salvar preferência** como **Salvar rascunhos em intervalos regulares** para salvar automaticamente o formulário após um intervalo de tempo específico.
  **Frequência do intervalo de salvamento (segundos)**: especifique o intervalo de tempo (em segundos) para definir a duração que aciona o salvamento automático do formulário no intervalo definido.

### Guia Enviar {#submission-tab}

Os usuários podem configurar ações diferentes para o envio de um formulário adaptável.

- **URL/caminho de redirecionamento**: essa opção permite que o usuário configure uma página em cada formulário, para a qual os usuários do formulário são redirecionados após enviar o formulário adaptável. Clique aqui para obter mais informações sobre [como configurar páginas de redirecionamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=pt-BR).

![Guia Enviar](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Mostrar mensagem**: essa opção permite que os usuários adicionem uma mensagem que é exibida quando o formulário adaptável é enviado com sucesso. O texto predefinido é incluído na caixa de diálogo e pode ser modificado pelo usuário. A caixa de diálogo Mostrar mensagem é compatível com as ferramentas de formatação de rich text que permitem que os usuários formatem o texto adicionado.

![Guia Mostrar mensagem](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Ação de envio**: uma ação de envio é acionada quando um usuário clica no botão Enviar em um formulário adaptável. Na lista suspensa, os usuários podem selecionar ações de envio que são compatíveis de fábrica. Saiba como [configurar uma ação de envio na guia Enviar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=pt-BR#supporting-custom-functions-in-validation-expressions-br).

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar estilos CSS do componente de Container do formulário.

### Guia Componentes permitidos {#allowed-components-tab}

![Guia Componentes permitidos da caixa de diálogo de design](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

A guia **Componentes permitidos** permite que o editor de modelo defina os componentes que podem ser adicionados como itens aos painéis do componente no editor de formulários adaptáveis.

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
## Learn more about the hamburger menu

A hamburger menu, often referred to as a mobile menu or navigation drawer, is a popular design element in mobile user interfaces. It features three horizontal lines stacked vertically, resembling a hamburger. The design efficiently conserves screen space by hiding secondary navigation options until they are needed, especially on smaller devices such as mobile. AEM forms can be efficiently organized within the hamburger menu, enabling users to access various panels within a form without overwhelming the main interface.

Consider a scenario, where a financial institution offers an online loan application form that requires users to provide detailed information across several panels, such as personal details, financial information, loan preferences, and supporting documents. The form includes multiple panels and options that can clutter the interface, especially on mobile devices. Users need an organized way to navigate through these panels without feeling overwhelmed. The hamburger menu is implemented to enhance the user experience on mobile devices.

### Components of hamburger menu

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A. Hamburger menu**: The hamburger menu features a navigation panel that slides out or drops down when the hamburger icon is clicked or tapped. The menu displays the panel headings, and selecting a panel shifts the focus to that panel. It allows users to easily navigate between different panels.

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B. Breadcrumb**: Breadcrumbs indicate the user’s current location within the form. They offer a hierarchical trail that shows the user’s navigation path and helps them understand their position in the form.

**C. Active panel**: The active panel refers to the section or part of the form that is currently being displayed. When a user selects an option from the hamburger menu, the corresponding panel becomes the active panel, showing the relevant fields and information for that section.

### Points to consider while working with the hamburger menu

- The hamburger menu displays only the names of the panels. Here are different scenarios illustrating how the panel name appears in the navigation pane of the hamburger menu based on the configuration properties of the panel:  
  
  - If you set the properties of the panel to hidden, the panel's name does not appear in the navigation pane of the hamburger menu. For example, if you configure the properties of the `Financial Information` panel as `hidden`, the panel name does not appear in the navigation pane of the hamburger menu.
    
    ![Hidden panel](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

  - If you set the properties of the panel to `disabled`, its name appears in the navigation pane of the hamburger menu, but you cannot select or edit it. For example, if you configure the properties of the `Financial Information` panel as `disabled`, the panel name appears in the navigation pane, but it cannot be selected or edited. 
     
    ![Disabled panel](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

  - If you hide the  title of the panel, it does not appear in the navigation pane of the hamburger menu. A blank space shows up instead, but you can navigate to the fields of the panel by clicking on that space. For example, if you hide the title of the `Financial Information` panel, the blank space appears in its place in the navigation pane of the hamburger menu. You can navigate to the fields of the panel by clicking on the blank space.
    
    ![Hidden title panel](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- By default, the navigation pane in the breadcrumb component supports up to three levels of navigation. However, with the custom component, you can configure the navigation hierarchy to accommodate as many levels as needed.
- When using the hamburger menu, the user can navigate between panels using arrows. However, once a panel is selected, the menu automatically closes, and focus shifts to the fields within the chosen panel.

### Advantages to use hamburger menu

- **Space efficiency**: By hiding form navigation options until needed, the hamburger menu maximizes screen space, which is especially beneficial on smaller devices.

- **Clutter reduction**: It minimizes visual clutter by consolidating various form navigation links into a single, collapsible menu.

- **Improved focus**: With fewer visible navigation elements, users can concentrate on the main content of the form without being distracted by secondary options.

- **Simplified design**: It creates a more streamlined user interface, resulting in a cleaner and more organized form layout.

- **Enhanced mobile experience**: On mobile devices, where screen space is limited, the hamburger menu offers an efficient way to access all form navigation options without overwhelming the user.

### How to enable hamburger menu for your form?

To enable hamburger menu for form, perform the following steps:

1. Open form in an edit mode.
1. Open the Content browser, and select the **[!UICONTROL Guide Container]** component of your Adaptive Form. 
1. Click the Guide Container properties ![Guide properties](/help/adaptive-forms/assets/configure_icon.png) icon. The Adaptive Form Container dialog box opens. 
1. Click the  **[!UICONTROL Basic]** tab. 
1. Select the **[!UICONTROL Add hamburger menu support]** checkbox.
1. Click **[!UICONTROL Done]**.

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab.png)
-->

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}