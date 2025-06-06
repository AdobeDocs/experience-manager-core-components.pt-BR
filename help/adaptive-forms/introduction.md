---
title: Introdução aos Componentes principais dos Formulários adaptáveis do AEM
description: Crie experiências de inscrição atraentes (formulários) usando a flexibilidade dos Componentes principais dos Formulários adaptáveis e as disponibilize com a eficiência do Adobe Experience Manager.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 12a829c164839fdcb2c98d52e409ec3ac2079c41
workflow-type: tm+mt
source-wordcount: '2123'
ht-degree: 100%

---

# Componentes principais dos formulários adaptáveis  {#adaptive-forms-core-components-introduction}

Usando os componentes principais dos formulários adaptáveis do Adobe Experience Manager, e possível criar experiências de inscrição atraentes.

## Componentes principais {#overview}

No Adobe Experience Manager (AEM), os componentes são os elementos usados para criar páginas e formulários. Eles fornecem uma maneira simples e eficiente para os autores criarem e gerenciarem conteúdo, além de fornecerem aos desenvolvedores a flexibilidade e a extensibilidade necessárias para criar componentes personalizados. Eles foram projetados para acelerar o tempo de desenvolvimento e reduzir os custos de manutenção de sites e formulários, ser flexíveis e poder ser facilmente personalizados para atender às necessidades específicas de um site e formulário.

Os Componentes principais também foram projetados para serem responsivos e oferecerem suporte a uma grande variedade de dispositivos, incluindo desktops, tablets e smartphones. Eles também seguem os padrões da Web e as práticas recomendadas mais recentes, tornando-os uma solução robusta e confiável para a criação de conteúdo da Web.

Em geral, os Componentes principais são uma ferramenta essencial para criar e gerenciar conteúdo da Web no AEM, fornecendo uma solução eficiente e flexível que pode ajudar a reduzir o tempo de desenvolvimento e os custos de manutenção, além de fornecer uma excelente experiência do usuário aos visitantes do site.

## Componentes principais dos formulários adaptáveis

Os Componentes principais dos formulários adaptáveis são um conjunto de 30 componentes de código aberto em conformidade com a metodologia BEM, criados com base nos componentes principais do WCM do Adobe Experience Manager. Eles foram especificamente projetados para serem usados na criação dos Formulários adaptáveis, que são formulários que se adaptam ao dispositivo, navegador e tamanho da tela do usuário.

Esses componentes podem ser usados para criar experiências excepcionais de captura e registro de dados, fornecendo uma grande variedade de opções de campos de formulário, incluindo campos de texto, caixas de seleção, menus suspensos e muito mais. Eles também incluem recursos como validação, lógica condicional e design responsivo, que podem ser usados para criar formulários fáceis de usar e intuitivos.

Além disso, como esses componentes são de código aberto, os desenvolvedores têm a capacidade de personalizar e estender facilmente os componentes para atender às necessidades específicas de sua organização. Além disso, esses componentes são criados com base na metodologia BEM, que garante sua capacidade de expansão e manutenção.

![imagem do formulário adaptável](assets/sample-adaptive-form.png)

## Recursos {#features}

|  |  |
|---|---|
| Prontos para produção | Os Componentes principais dos Formulários adaptáveis são 24 componentes WCM robustos. |
| Prontos para nuvem | Disponível para o [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=pt-BR). |
| Versáteis | Os componentes representam conceitos genéricos com os quais os autores do Forms podem reunir quase qualquer layout. |
| Configuráveis | As [políticas de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=pt-BR#content-policies) no nível do modelo definem quais recursos podem ser ou não usados. |
| Acessíveis | Eles fornecem rótulos ARIA, são compatíveis com a navegação por teclado e dão suporte a texto para tecnologias de assistência, como leitores de tela. |
| Tema | Os componentes implementam o [Sistema de Estilos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=pt-BR), e a marcação segue as [convenções de CSS de BEM.](https://getbem.com/) |
| Personalizáveis | Vários padrões permitem fácil personalização, desde o ajuste do HTML até a reutilização de funcionalidade avançada. |
| Versões | A [política de controle de versão](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garante que os Componentes principais não interrompam seu site ao melhorar coisas que podem afetar você. |
| Código aberto | Se algo não sair como deveria, contribua com melhorias. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Benefícios {#benefits}

As experiências de captura de dados são cruciais para a geração de leads e inscrição, e os Componentes principais dos Formulários adaptáveis fornecem uma solução eficiente para criar formulários otimizados para captura de dados. Alguns dos motivos para usar os Componentes principais para criar essas experiências em componentes de base são:

* **[Disponibilidade no GitHub](https://github.com/adobe/aem-core-forms-components)**: os componentes principais dos formulários adaptáveis do AEM são de código aberto e estão disponíveis no GitHub, juntamente com uma documentação abrangente. Isso facilita para os desenvolvedores compreender os componentes e como eles funcionam, além de contribuir para seu desenvolvimento. O site [aemcomponents.dev](https://www.aemcomponents.dev/) também é um recurso valioso, em que os desenvolvedores podem ver os componentes em ação e acessar a documentação detalhada.

* **[Modelo BEM para estilo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: os componentes principais seguem o modelo BEM (sigla em inglês para modificador de elementos de blocos) para estilo, que é uma metodologia bem-estabelecida e amplamente usada para organizar o CSS. Isso facilita para os desenvolvedores entender como os estilos são organizados e como modificá-los para atender às suas necessidades específicas.

* **Sem dependência de bibliotecas de terceiros**: uma das vantagens dos Componentes principais é que eles não têm dependência de bibliotecas JavaScript de terceiros, incluindo JQuery e Underscore. Isso torna os componentes mais rápidos e leves, além de facilitar a integração em uma implementação existente do AEM.

* **Foco no desempenho e na acessibilidade**: os Componentes principais são construídos pensando no desempenho e na acessibilidade, o que se reflete em suas altas pontuações do Google Lighthouse e Web Vitals. Isso facilita para os desenvolvedores criarem páginas da Web acessíveis e de alto desempenho, o que é cada vez mais importante no cenário digital atual.

* **Componentes de formulários no Modelo e Temas do Sites 30**: os Componentes principais fornecem suporte para componentes de formulário no modelo e temas do Sites 30, facilitando para os desenvolvedores criarem e personalizarem formulários no AEM.

* **[Mais fácil de criar estilo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: é mais fácil criar estilos nos componentes principais do que nos de de fundação. O processo de criação de temas é semelhante ao Sites, com a capacidade de herdar o mesmo tema/CSS da página principal do Sites. Além disso, o modelo BEM para estilo facilita a compreensão e a modificação dos estilos.

* **Acessibilidade**: os componentes principais dos formulários adaptáveis são compatíveis com padrões e diretrizes de acessibilidade para garantir que os formulários possam ser usados por pessoas com deficiência, inclusive quem usa tecnologias de assistência, como leitores de tela.

* **[Controle de versão](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/add-comments-annotations-versioning-adaptive-form-core-components)**: você pode criar e gerenciar várias versões de um formulário adaptável baseado em componentes principais, participar de discussões colaborativas por meio de comentários e anexar anotações a componentes de formulário específicos, aprimorando assim a experiência geral de criação de formulários.

## Componentes disponíveis: um detalhamento por tipo de componente

A versão atual do AEM Forms inclui os seguintes componentes principais: [componentes de fundação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/create-an-adaptive-form-on-forms-cs/introduction-forms-authoring#component-toolbar) e [componentes de blocos de formulário (Edge Delivery Services)](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/edge-delivery/build-forms/forms-references/form-components).

| Componentes | Componentes de fundação | Componentes principais | Componentes de bloco de formulário | Informações adicionais |
|------------|:---------------------:|:---------------:|:---------------------:|-----------------------|
| Bloco do Adobe Sign | ✔️ | | | A [integração do Adobe Sign](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/integrate/services/adobe-sign-integration-adaptive-forms#adobe-acrobat-sign-for-government) está disponível somente para os componentes de fundação. |
| Acordeão | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/accordion.md)</span> | | Para os componentes de fundação, é possível configurar o layout do acordeão nas [propriedades dos componentes do painel](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout). |
| Fragmento de formulário adaptável | ✔️ | ✔️ | | Para os componentes de fundação, é possível [adicionar um fragmento](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/forms/adaptive-forms-basic-authoring/adaptive-form-fragments#insert-a-fragment-in-an-adaptive-form) a partir do navegador de ativos. |
| reCAPTCHA de formulário adaptável | ✔️ | ✔️ | ✔️ | Para os componentes de fundação, use o componente Captcha para [adicionar o Google reCaptcha a um formulário](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms#google-reCAPTCHA). |
| Botão | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/button.md)</span> | ✔️ | |
| Gráfico | ✔️ | | | |
| Caixa de seleção | ✔️ | ✔️ | | |
| Grupo de caixas de seleção | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/checkbox-group.md)</span> | ✔️ | Para os componentes de fundação, use o componente caixa de seleção para adicionar várias caixas de seleção |
| Campo de entrada de data | ✔️ | | | Para os componentes principais, use o componente de [seletor de data](/help/adaptive-forms/components/date-picker.md). Também é possível adicionar componentes separados de [caixa de texto](/help/adaptive-forms/components/text-box.md) ou [caixa numérica](/help/adaptive-forms/components/numeric-box.md) para captar o dia, o mês e o ano. |
| Seletor de data | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/date-picker.md)</span> | ✔️ | |
| Lista suspensa | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/drop-down-list.md)</span> | ✔️ | |
| Email | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/email.md)</span> | ✔️ | |
| Anexo de arquivo | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/file-attachment.md)</span> | ✔️ | |
| Listagem do anexo de arquivo | ✔️ | | | |
| Rodapé | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/footer.md)</span> | ✔️ | |
| Espaço reservado para nota de rodapé | ✔️ | | | |
| Container de formulário | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/form-container.md)</span> | ✔️ | Para componentes de fundação, use o [componente do painel raiz](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/forms/create-first-af/configure-root-panel). |
| Título do formulário | ✔️ | ✔️ | | Para componentes de fundação, use o componente título. |
| hCaptcha | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/hcaptcha.md)</span> |  | É possível [conectar seus formulários adaptáveis com o hCaptcha](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile) para formulários baseados em componentes de fundação. |
| Cabeçalho | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/header.md)</span> | ✔️ | |
| Guias horizontais | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/horizontal-tabs.md)</span> | | Para os componentes de fundação, é possível configurar o [layout de guias na parte superior (guias horizontais)](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) nas propriedades dos componentes do painel. |
| Imagem | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/image.md)</span> | ✔️ | |
| Botão Próximo | ✔️ | ✔️ | | Use o [componente assistente](/help/adaptive-forms/components/wizard.md) para os botões de próximo e anterior para mover-se entre vários painéis. |
| Caixa numérica | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/numeric-box.md)</span> | ✔️ | |
| Escalonador numérico | ✔️ | | | |
| Painel | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/panel.md)</span> | ✔️ | |
| Telefone / Celular | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/phone.md)</span> | ✔️ | |
| Botão Anterior | ✔️ | ✔️ | | Use o [componente assistente](/help/adaptive-forms/components/wizard.md) para os botões de próximo e anterior para mover-se entre vários painéis. |
| Grupo de botões de opção | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/radio-button.md)</span> | ✔️ | |
| Botão Redefinir | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> | ✔️ | |
| Revisar |  | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> |  | |
| Rabiscar a assinatura | ✔️ | | | |
| Separador | ✔️ | | | Usar componente [Separador](/help/components/separator.md) do WCM |
| Botão Enviar | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/submit-button.md)</span> | ✔️ | |
| Etapa de resumo | ✔️ | | | |
| Interruptor | ✔️ | <span style="color:blue"> [✔️](/help/adaptive-forms/components/adaptive-form-switch.md) | | |
| Tabela | ✔️ | | | |
| Termos e condições | ✔️ | ✔️ | | |
| Texto | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text.md)</span> | ✔️ | |
| Caixa de texto | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text-box.md)</span> | ✔️ | |
| Captcha Turnstile | ✔️ | | | O [Captcha Turnstile](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile) está disponível somente para componentes de fundação. |
| Guias verticais | ✔️ | ✔️ | | Para os componentes de fundação, é possível configurar o [layout de guias à esquerda (guias verticais)](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) nas propriedades dos componentes do painel |
| Assistente | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/wizard.md)</span> | ✔️ | Para os componentes de fundação, é possível configurar o [layout do assistente](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) nas propriedades dos componentes do painel |

<!--| Password Box | ✔️ | ✔️| ✔️ | |
| Image Choice | ✔️ | | | |
-->


>[!NOTE]
>
>
> * Além dos componentes listados acima, o bloco de formulários é compatível com todos os [tipos de entrada HTML5](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/input#input_types) e [área de texto](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/textarea) válidos como componentes.
> * Precisa de um componente não listado acima? Solicite-o enviando um email para aem-forms-ea@adobe.com do seu endereço oficial.


<!-- >
* [Accordion](/help/adaptive-forms/components/accordion.md)
* [Adaptive Form Fragment](/help/adaptive-forms/components/adaptive-form-fragment.md)
* [Adaptive Form Switch](/help/adaptive-forms/components/adaptive-form-switch.md)
* [Button](/help/adaptive-forms/components/button.md)
* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
* [Date Picker](/help/adaptive-forms/components/date-picker.md)
* [Drop-down list](/help/adaptive-forms/components/drop-down-list.md)
* [Email](/help/adaptive-forms/components/email.md)
* [Form Container](/help/adaptive-forms/components/form-container.md)
* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
* [Footer](/help/adaptive-forms/components/footer.md)
* [Header](/help/adaptive-forms/components/header.md)
* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Numeric Box](/help/adaptive-forms/components/numeric-box.md)
* [Panel](/help/adaptive-forms/components/panel.md)
* [Phone](/help/adaptive-forms/components/phone.md)
* [Radio Button](/help/adaptive-forms/components/radio-button.md)
* [Adaptive Form reCAPTCHA](/help/adaptive-forms/components/adaptive-form-recaptcha.md)
* [Reset Button](/help/adaptive-forms/components/reset-button.md)
* [Submit Button](/help/adaptive-forms/components/submit-button.md)
* [Text Box](/help/adaptive-forms/components/text-box.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Form Title](/help/adaptive-forms/components/form-title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

-->

## Editor de formulários fácil de usar

O editor dos formulários adaptáveis baseados em componentes principais é semelhante ao que você já usa para criar páginas do AEM Sites. Veja o que você leva:


* **Elementos e configurações de interface familiares**: ao configurar as propriedades dos componentes de formulários, você verá que a caixa de diálogo de propriedades se parece com as que você está usando para os componentes principais do WCM. Isso torna mais rápido encontrar as opções que você precisa. Como nos componentes principais do WCM, nos componentes de formulários, a caixa de diálogo de propriedades é exibida no centro do editor com guias claras separando as opções básicas e avançadas, o texto de ajuda e as informações de acessibilidade. Tudo isso em um formato de guias para facilitar a navegação.

* **[Editor de regras](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/rule-editor-core-components)**: é possível adicionar recursos lógicos e dinâmicos a seus formulários sem escrever código. Você pode usar o editor de regras integrado para:
   * Mostrar ou ocultar campos com base nas opções escolhidas
   * Habilitar ou desabilitar um objeto
   * Definir um valor para um objeto
   * Realizar cálculos
   * Definir a propriedade de um objeto
   * Validar entrada de dados
   * Chamar um serviço (chamar funcionalidade externa)
   * Usar funções integradas (funções predefinidas para tarefas comuns)
   * Usar funções personalizadas (seu próprio código para necessidades específicas)
   * Validar campos e painéis (garantir que os dados satisfaçam os requisitos)
   * Validar o valor de um objeto
   * Executar funções para calcular o valor de um objeto
   * Chamar um serviço de modelo de dados de formulário (FDM) e executar uma operação
   * Adicionar estilos dinamicamente (alterar a aparência com base nas condições)
   * Criar outras regras (ações em cadeia e lógica)
   * e muito mais.

  O editor de regras não tem o editor de código. Você pode usar [funções personalizadas](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-and-use-custom-functions) para adicionar o seu próprio código ao editor de regras para suprir necessidades específicas.



* **Preenchimento prévio de formulários**: é possível preencher automaticamente determinados campos em um formulário com dados já existentes ao abri-lo. Isso economiza tempo e esforço, eliminando a necessidade de inserir manualmente informações que podem já estar disponíveis. O editor de componentes principais fornece um serviço de preenchimento prévio pronto para uso para preencher campos de formulário com a ajuda de um modelo de dados de formulário. Você também pode criar serviços de preenchimento prévio personalizados para cenários mais complexos.

* **[Documento de registro (DoR)](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components)**: um documento de registro (DoR) se refere a uma representação formal e imprimível dos dados enviados por meio do formulário. Isso serve como um registro permanente das informações inseridas, fornecendo um instantâneo dos dados enviados em um formato intuitivo, normalmente, um documento PDF. Você pode usar o editor para configurar facilmente um modelo personalizado ou usar um modelo pronto para uso para gerar um DoR.

* **[Modelo de dados de formulário](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)**: um modelo de dados de formulários adaptáveis (FDM) atua como uma ponte entre os formulários adaptáveis e as fontes de dados. Esse modelo define basicamente a estrutura e a organização dos dados que seus formulários coletam e interagem. É possível usar o editor para conectar facilmente seu formulário a um modelo de dados de formulário (FDM).

* **[Envios de formulário](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form)**: o envio de um formulário refere-se ao processo de envio dos formulários preenchidos. Isso aciona uma série de ações definidas na configuração do formulário, levando ao armazenamento ou processamento dos dados enviados. O editor de formulários adaptáveis oferece uma variedade de opções para configurar envios de formulários. Algumas das ações comuns de envio são:

   * [Enviar email](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form.)
   * [Chamar um fluxo do Power Automate](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/integrate/services/forms-microsoft-power-automate-integration)
   * [Enviar para o SharePoint](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-sharepoint)
   * [Chamar um Workfront Fusion](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20a%20Workfront%20Fusion)
   * [Enviar usando um modelo de dados de formulário (FDM)](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)
   * [Enviar para o Armazenamento de blob do Azure](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Submit%20to%20Azure%20Blob%20Storage)
   * [Enviar para o ponto de acesso REST](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-restpoint)
   * [Enviar para o OneDrive](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=to%20REST%20endpoint-,Submit%20to%20OneDrive,-Invoke%20an%20AEM)
   * [Chamar um fluxo de trabalho do AEM](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20an%20AEM%20Workflow)


* [Componentes principais dos formulários adaptáveis no editor de páginas do Sites](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page): é possível habilitar e usar os componentes principais dos formulários adaptáveis no editor de páginas do AEM e nos fragmentos de experiência do AEM para criar diretamente a experiência de captura de dados, juntamente com a criação de uma página do Sites.

  >[!VIDEO](https://video.tv.adobe.com/v/3419284?quality=12&learn=on)


<!-- 
* **Preview Forms**: You can use the editor to  simulates how the form would appear on various devices like desktops, tablets, and smartphones.
-->



## Habilitar os componentes principais dos formulários adaptáveis

A ativação dos Componentes principais dos formulários adaptáveis no AEM Forms as a Cloud Service permite criar, publicar e fornecer os Componentes principais baseados em formulários, adaptáveis e headless, usando as instâncias do AEM Forms Cloud Service para vários canais. Para obter instruções detalhadas sobre como habilitar os Componentes principais dos formulários adaptáveis, consulte [Habilitar componentes principais de formulários adaptáveis no AEM Forms as a Cloud Service e no ambiente de desenvolvimento local](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=pt-BR).

Os Componentes principais dos Formulários adaptáveis têm os seguintes requisitos.

| Versão do AEM | Complemento do AEM Forms | Componentes principais dos formulários adaptáveis |
|---|---|---|
| AEM as a Cloud Service | Forms - Inscrição digital | [Versão 2.0.10](version.md)+ |
| AEM 6.5 | Complemento do Forms | [Versão 1.1.12](version.md)+ |

Se sua versão do SDK do AEM Cloud Service for anterior à 2023.02.0, [certifique-se de que o sinalizador `prerelease` esteja habilitado em seu ambiente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=pt-BR#new-features), pois os Componentes principais de formulários adaptáveis faziam parte do pré-lançamento antes da versão 2023.02.0.


## Criar um formulário adaptável baseado nos Componentes principais

É possível executar as seguintes ações nos ambientes do AEM Forms as a Cloud Service ou do AEM Forms 6.5:

| Ação | Versão do AEM Forms |
|--------|------------------|
| Criar um formulário adaptável independente | [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=pt-BR) |
| Criar um formulário adaptável em uma página do AEM Sites | [AEM Forms 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=pt-BR#create-an-adaptive-form-in-sites-editor-or-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=pt-BR#create-an-adaptive-form-in-sites-editor-or-experience-fragment) |
| Criar um formulário adaptável em um fragmento de experiência do AEM | [AEM Forms 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=pt-BR#create-an-adaptive-form-in-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=pt-BR#create-an-adaptive-form-in-experience-fragment) |
| Converter um formulário adaptável em um fragmento de experiência | [AEM Forms 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=pt-BR#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=pt-BR#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment) |





<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->

## Consulte também {#see-also}

{{see-also}}
