---
title: 'Componente principal de formulários adaptáveis: container de formulário'
description: Adicionar um formulário adaptável a uma página da web.
role: Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
TQID: https://experienceleague.adobe.com/kMG6SKHisAUmKhOh9AFLI8NG6w0vH7tP4XimBKAMo-I
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 0af65c80f9cc58c4ba48d5b3dc7a026820bd2833
workflow-type: tm+mt
source-wordcount: 2555
ht-degree: 64%

---

# Container de formulário {#form-container-adaptive-forms-core-component}

<span class="preview"> Este artigo discute os recursos **Rascunhos** e **Suporte a Menu Hamburger**, que são recursos de pré-lançamento. O recurso de pré-lançamento pode ser acessado somente por meio do [canal de pré-lançamento](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/prerelease#new-features).</span>

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

O componente principal de acordeão de formulários adaptáveis foi lançado em fevereiro de 2023 como parte dos componentes principais 2.0.4 para serviços na nuvem e dos componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM Forms 6.5.16.0 ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).
<!--
## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_br). 
-->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal de container de formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Para obter mais informações sobre o desenvolvimento dos componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do container de formulário para visitantes com a caixa de diálogo de configuração. Você também pode definir opções de container de formulário com facilidade para uma experiência de usuário perfeita.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **Título**: o título permite identificar facilmente um componente em um formulário; por padrão, ele aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Serviços de preenchimento prévio**: essa opção permite que o usuário selecione um serviço de preenchimento prévio para recuperar dados quando o formulário adaptável for renderizado. Saiba mais sobre [como criar e configurar um serviço de pré-preenchimento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=pt-BR#aem-forms-custom-prefill-service).

- **Função**: a função é um atributo HTML usado para especificar a finalidade de um elemento HTML para tecnologias de assistência, como leitores de tela. O atributo de função é usado para fornecer contexto e significado semântico adicionais a um elemento, facilitando a interpretação e o anúncio do conteúdo pelos leitores de tela. Por exemplo, no AEM Forms, o rótulo de um campo de formulário pode ter a função de “rótulo” e seu campo de entrada pode ter a função de “caixa de texto”. Isso ajuda o leitor de tela a entender a relação entre o rótulo e o campo de entrada e anunciá-los corretamente ao usuário.

- **Categoria de biblioteca do cliente**: o usuário pode configurar uma biblioteca JavaScript personalizada por formulário adaptável. É recomendável manter somente as funções reutilizáveis na biblioteca, que dependem das bibliotecas de terceiros de jquery e underscore.js.Às vezes, se houver **regras de validação complexas**, o script de validação exato residirá em funções personalizadas, e os usuários chamam essas funções personalizadas a partir da expressão de validação do campo. Para tornar esta biblioteca de funções personalizadas conhecida e disponível durante a execução de validações do lado do servidor, o usuário do formulário pode configurar o nome da biblioteca do cliente do AEM na guia **[!UICONTROL Básico]** das propriedades do Container de formulários adaptáveis.Usuários podem configurar a biblioteca customJavaScript para cada formulário adaptável. Na biblioteca, mantenha somente as funções reutilizáveis, que dependem de bibliotecas de terceiros de jquery e underscore.js.

- **Habilitar o menu de hambúrguer para o modo de exibição móvel** - Marque a caixa de seleção para integrar um menu de hambúrguer ao seu formulário para modo de exibição móvel. Representado por três linhas horizontais empilhadas verticalmente, esse menu fornece uma exibição clara e organizada para painéis em dispositivos menores, especialmente em dispositivos móveis. Para obter mais informações sobre o menu de hambúrguer, consulte a seção [Saiba mais sobre o menu de hambúrguer](#learn-more-about-the-hamburger-menu).


### Guia Modelo de dados {#data-model-tab}

![Guia Modelo de Dados](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Você pode usar o modelo de dados de formulário e conectar um formulário a uma fonte de dados para enviar e receber dados com base nas ações do usuário. Também é possível conectar um formulário a um esquema JSON para receber os dados enviados em um formato predefinido. De acordo com os requisitos, conecte o formulário a um esquema JSON ou modelo de dados de formulário:
- **Nenhum** - Não associar o formulário a um modelo de dados.
- **Esquema** - Conecte o formulário a um esquema JSON carregado no seu ambiente.
- **Modelo de dados de formulário** - Conecte o formulário a um Modelo de dados de formulário para integrar a fontes de dados externas.
- **Conector** - Conecta o formulário a uma fonte de dados baseada em conector.
- **Modelos de Formulário** - Associe o formulário a um modelo de formulário.

### Guia Rascunhos {#drafts-tab}

![Guia Rascunhos](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **Salvar rascunhos automaticamente**: marque a caixa de seleção **Salvar rascunhos automaticamente** para habilitar o salvamento de formulários como rascunhos.
- **Salvar preferência**: Configure a opção **Salvar preferência** como **Salvar rascunhos em intervalos regulares** para salvar automaticamente o formulário após um intervalo de tempo específico.
  **Frequência do intervalo de salvamento (segundos)**: especifique o intervalo de tempo (em segundos) para definir a duração que aciona o salvamento automático do formulário no intervalo definido.

### Guia Enviar {#submission-tab}

Os usuários podem configurar ações diferentes para o envio de um formulário adaptável.

- **No envio** - Escolha **Redirecionar para URL** para enviar usuários de formulário para uma página configurada após o envio, ou **Mostrar Mensagem** para exibir uma mensagem de confirmação no formulário.

- **URL/caminho de redirecionamento**: essa opção permite que o usuário configure uma página em cada formulário, para a qual os usuários do formulário são redirecionados após enviar o formulário adaptável. Clique aqui para obter mais informações sobre [como configurar páginas de redirecionamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=pt-BR).

![Guia Enviar](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Mostrar mensagem**: essa opção permite que os usuários adicionem uma mensagem que é exibida quando o formulário adaptável é enviado com sucesso. O texto predefinido é incluído na caixa de diálogo e pode ser modificado pelo usuário. A caixa de diálogo Mostrar mensagem é compatível com as ferramentas de formatação de rich text que permitem que os usuários formatem o texto adicionado.

![Guia Mostrar mensagem](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Ação de envio**: uma ação de envio é acionada quando um usuário clica no botão Enviar em um formulário adaptável. Na lista suspensa, os usuários podem selecionar ações de envio que são compatíveis de fábrica. Saiba como [configurar uma ação de envio na guia Enviar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=pt-BR#supporting-custom-functions-in-validation-expressions-br).

- **Configuração de Ação** - Configure mapeamentos para transmitir valores de campo como parâmetros de solicitação para a Página de Agradecimento.

- **Habilitar solicitação POST** - Selecione esta opção para enviar dados de formulário usando uma solicitação POST HTTP.

### Guia Documento de registro {#document-of-record-tab}

![Guia Documento de Registro](/help/adaptive-forms/assets/formcontainer_dortab.png)

Um [Documento de Registro (DoR)](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components) é uma representação formal e imprimível dos dados enviados pelo formulário. Use a guia **Documento de Registro** para configurar como um DoR é gerado quando um usuário envia o formulário:

- **Nenhum** - Não gerar um Documento de Registro para o formulário.
- **Associar modelo de formulário como o documento de modelo de registro** - Use um modelo de formulário existente como o modelo do DoR.
- **Gerar documento de registro** - Gera automaticamente um DoR com base nos dados de formulário enviados.
- **Excluir anexos de arquivo do Documento de Registro** - Selecione esta opção para omitir anexos de arquivo do DoR gerado.

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

## Saiba mais sobre o menu de hambúrguer {#learn-more-about-the-hamburger-menu}

Um menu de hambúrguer, geralmente chamado de menu móvel ou gaveta de navegação, é um elemento de design popular em interfaces de usuário móveis. Possui três linhas horizontais empilhadas verticalmente, assemelhando-se a um hambúrguer. O design preserva o espaço da tela de forma eficiente, ocultando opções de navegação secundárias até que sejam necessárias, especialmente em dispositivos menores, como dispositivos móveis. Os formulários do AEM podem ser organizados com eficiência no menu de hambúrguer, permitindo que os usuários acessem vários painéis em um formulário sem sobrecarregar a interface principal.

Considere um cenário em que uma instituição financeira oferece um formulário de aplicativo de empréstimo online que requer que os usuários forneçam informações detalhadas em vários painéis, como detalhes pessoais, informações financeiras, preferências de empréstimo e documentos de suporte. O formulário inclui vários painéis e opções que podem desorganizar a interface, especialmente em dispositivos móveis. Os usuários precisam de uma maneira organizada de navegar por esses painéis sem se sentirem sobrecarregados. O menu de hambúrguer é implementado para aprimorar a experiência do usuário em dispositivos móveis.

### Componentes do menu de hambúrguer

![Menu Hamburger](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A Menu de hambúrguer**: o menu de hambúrguer apresenta um painel de navegação que desliza ou desce quando o ícone de hambúrguer é clicado ou tocado. O menu exibe os cabeçalhos do painel e selecionar um painel desloca o foco para esse painel. Ele permite que os usuários naveguem facilmente entre painéis diferentes.

![Menu Hamburger](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B Navegação estrutural**: as navegações estruturais indicam a localização atual do usuário dentro do formulário. Eles oferecem uma trilha hierárquica que mostra o caminho de navegação do usuário e os ajuda a entender sua posição no formulário.

**C Painel ativo**: o painel ativo se refere à seção ou parte do formulário que está sendo exibido no momento. Quando um usuário seleciona uma opção no menu de hambúrguer, o painel correspondente se torna o painel ativo, mostrando os campos e informações relevantes para essa seção.

### Pontos a serem considerados ao trabalhar com o menu de hambúrguer

- O menu de hambúrguer exibe somente os nomes dos painéis. Estes são diferentes cenários que ilustram como o nome do painel aparece no painel de navegação do menu de hambúrguer com base nas propriedades de configuração do painel:

   - Se você definir as propriedades do painel como oculto, o nome do painel não aparecerá no painel de navegação do menu de hambúrguer. Por exemplo, se você configurar as propriedades do painel `Financial Information` como `hidden`, o nome do painel não aparecerá no painel de navegação do menu de hambúrguer.

     ![Painel oculto](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

   - Se você definir as propriedades do painel como `disabled`, seu nome aparecerá no painel de navegação do menu de hambúrguer, mas você não poderá selecioná-lo ou editá-lo. Por exemplo, se você configurar as propriedades do painel `Financial Information` como `disabled`, o nome do painel aparecerá no painel de navegação, mas não poderá ser selecionado ou editado.

     ![Painel desabilitado](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

   - Se você ocultar o título do painel, ele não aparecerá no painel de navegação do menu de hambúrguer. Um espaço em branco é exibido no lugar dele, mas você pode navegar até os campos do painel clicando nesse espaço. Por exemplo, se você ocultar o título do painel `Financial Information`, o espaço em branco aparecerá em seu lugar no painel de navegação do menu de hambúrguer. Você pode navegar para os campos do painel clicando no espaço em branco.

     ![Painel de título oculto](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- Por padrão, o painel de navegação no componente de Navegação estrutural suporta até três níveis de navegação. No entanto, com o componente personalizado, você pode configurar a hierarquia de navegação para acomodar quantos níveis forem necessários.
- Ao usar o menu de hambúrguer, o usuário pode navegar entre painéis usando setas. No entanto, depois que um painel é selecionado, o menu é fechado automaticamente e o foco é deslocado para os campos dentro do painel escolhido.

<!--
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

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab1.png)
-->

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}