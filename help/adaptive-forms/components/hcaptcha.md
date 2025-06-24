---
title: hCaptcha nos formulários adaptáveis do AEM
description: Melhore a segurança dos formulários com o serviço hCaptcha&reg; sem esforço. Guia passo a passo no interior.
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
exl-id: eecb38d5-711e-4dc5-bc19-498e003f37e7
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 100%

---


# Componente do hCaptcha{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> Esse recurso faz parte do programa de adoção antecipada. Você pode escrever para aem-forms-ea@adobe.com da sua ID de email oficial para ingressar no programa de adoção antecipada e solicitar acesso ao recurso. </span>

O serviço hCaptcha® protege seus formulários contra bots, spam e abuso automatizado. O recurso representa um desafio de dispositivo de caixa de seleção e avalia a resposta do usuário para determinar se um humano ou um bot está interagindo com o formulário. Ele impede que o usuário prossiga se o teste falhar e ajuda a tornar as transações online seguras, evitando que os bots publiquem spam ou atividades mal-intencionadas.

![hCaptcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

{{traditional-aem}}

## Uso {#usage}

Existem várias vantagens de incluir um desafio hCaptcha em um processo de envio de formulário, como:

- **Prevenção de bots**: garante que o formulário seja enviado por uma pessoa, reduzindo spams e envios automatizados.

- **Segurança**: adiciona uma camada extra de segurança, verificando a legitimidade do envio de cada formulário e protegendo contra ataques mal-intencionados.

- **Integridade dos dados**: ao evitar envios múltiplos ou fraudulentos, ajuda a manter a integridade e a precisão dos dados coletados pelo formulário.

- **Verificação do usuário**: verifica a identidade do usuário que está enviando o formulário, garantindo que somente usuários autenticados possam concluir transações confidenciais.

- **Gerenciamento de carga**: ajuda a gerenciar a carga do servidor, controlando a taxa de envios de formulários, evitando a sobrecarga do sistema durante períodos de alto tráfego.

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente hCaptcha na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Para obter mais informações sobre o desenvolvimento dos componentes principais, consulte a [documentação do desenvolvedor dos componentes principais](/help/developing/overview.md).

Especifique as propriedades do componente hCaptcha usando a [caixa de diálogo de configuração](#configure-dialog). A caixa de diálogo de configuração faz parte dos componentes principais criados para facilitar a criação de formulários e fornecer uma maneira eficiente de criar formulários complexos.

## Versão e compatibilidade {#version-and-compatibility}


O componente hCaptcha de formulários adaptáveis foi lançado em maio de 2024 como parte dos [Componentes principais 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível | Compatível |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

## Caixa de diálogo de configuração {#configure-dialog}

É possível personalizar facilmente as propriedades do componente hCaptcha com a caixa de diálogo Configurar, que tem a guia Básico e a guia Validação para personalizar várias propriedades.

### Guia Básico {#basic-tab}

- **[!UICONTROL Nome]:** especifique o nome do componente hCaptcha. Você pode identificar facilmente um componente de formulário com seu nome exclusivo no formulário e no editor de regras.
- **[!UICONTROL Título]:** especifique o título do componente hCaptcha.
- **[!UICONTROL Configurações]:** selecione uma configuração na nuvem definida para o hCaptcha®.
- **Tamanho do Captcha:** você pode selecionar o tamanho de exibição da caixa de diálogo do desafio hCaptcha®. Use a opção **[!UICONTROL Compacto]** para exibir uma uma caixa de diálogo de desafio hCaptcha® de tamanho pequeno e a opção **[!UICONTROL Normal]** para exibir uma de tamanho relativamente grande.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![Guia Básico do hCaptcha](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Guia Validação {#validation-tab}

- **[!UICONTROL Mensagem de validação]:** forneça uma mensagem de validação para sua validação de Captcha no envio do formulário.
- **[!UICONTROL Mensagem de validação do script]**: use esta opção para inserir uma mensagem de prompt se a validação do script falhar.

  ![Guia Validação de hCaptcha](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha® é uma marca registrada da Intuition Machines, Inc.**

**Saiba mais** sobre outros **Componentes de Captcha** e seus serviços, como:

- [Usar o hCaptcha em um formulário adaptável para os componentes principais](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hcaptcha-core-components)

- [Usar o hCaptcha em um formulário adaptável para componentes de fundação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [Usar CAPTCHA Turnstile em um formulário adaptável para componentes de fundação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [Usar o Google reCAPTCHA em um formulário adaptável para componentes de fundação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}
