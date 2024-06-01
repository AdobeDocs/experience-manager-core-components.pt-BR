---
title: Captcha no AEM Adaptive Forms
description: Melhore a segurança dos formulários com o serviço do hCaptcha&reg; sem esforço. Guia passo a passo no interior!
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
source-git-commit: 08d44e4db42594fb5aaf33d7d42df6fe19c70f59
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 12%

---

# Componente do Captcha{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> Esse recurso está sob o Early Adoter Program. Você pode escrever para aem-forms-ea@adobe.com a partir de sua ID de e-mail oficial para participar do programa de adoção antecipada e solicitar acesso ao recurso. </span>

O serviço de Captcha® protege seus formulários contra bots, spam e abuso automatizado. Ele apresenta um desafio de widget de caixa de seleção e avalia a resposta do usuário para determinar se é um humano ou um bot interagindo com o formulário. Ele impede que o usuário continue se o teste falhar e ajuda a tornar as transações online seguras, impedindo que os bots publiquem spam ou atividades mal-intencionadas.

![Captcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## Uso {#usage}

Há vários motivos pelos quais é benéfico incluir um desafio de hCaptcha em um processo de envio de formulário. São eles:

- **Prevenção de bot**: garante que o formulário seja enviado por um usuário, reduzindo o spam e os envios automatizados.

- **Segurança**: adiciona uma camada extra de segurança, verificando a legitimidade do envio de cada formulário e protegendo contra ataques mal-intencionados.

- **Integridade dos dados**: ao evitar envios múltiplos ou fraudulentos, ele ajuda a manter a integridade e a precisão dos dados coletados por meio do formulário.

- **Verificação do usuário**: ele verifica a identidade do usuário que está enviando o formulário, garantindo que somente usuários autenticados possam concluir transações confidenciais.

- **Gerenciamento de carga**: ajuda a gerenciar a carga do servidor, controlando a taxa de envios de formulários, evitando a sobrecarga do sistema durante períodos de alto tráfego.

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente Captcha na documentação técnica sobre o [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

Especifique as propriedades do componente Captcha usando o [caixa de diálogo de configuração](#configure-dialog). A caixa de diálogo de configuração faz parte dos componentes principais que são criados para facilitar a criação de formulários e fornecer uma maneira eficiente de criar formulários complexos.

## Versão e compatibilidade {#version-and-compatibility}


O componente Captcha do Forms adaptável foi lançado em maio de 2024 como parte da [Componentes principais 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível | Compatível |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

## Caixa de diálogo de configuração {#configure-dialog}

É possível personalizar facilmente as propriedades do componente Captcha com a caixa de diálogo Configurar, que tem a guia Básico e a guia Validação para personalizar várias propriedades.

### Guia Básico {#basic-tab}

- **[!UICONTROL Nome]:** Especifique o nome do componente Captcha. Você pode identificar facilmente um componente de formulário com seu nome exclusivo no formulário e no editor de regras.
- **[!UICONTROL Título]:** Especifique o título do componente Captcha.
- **[!UICONTROL Configurações]:** Selecione uma Configuração na nuvem configurada para o hCaptcha®.
- **Tamanho do Captcha:** Você pode selecionar o tamanho de exibição da caixa de diálogo Desafio hCaptcha®. Use o **[!UICONTROL Compacto]** opção para exibir um tamanho pequeno e a variável **[!UICONTROL Normal]** opção para exibir uma caixa de diálogo de desafio do hCaptcha® de tamanho relativamente grande.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![Guia Básico do Captcha](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Guia Validação {#validation-tab}

- **[!UICONTROL Mensagem de validação]:** Forneça uma mensagem de validação para sua validação de Captcha no envio do formulário.
- **[!UICONTROL Mensagem de validação do script]** - Use esta opção para inserir uma mensagem de prompt, se a validação do script falhar.

  ![Guia Validação de Captcha](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**Captcha® é uma marca registrada da Intuition Machines, Inc.**

**Saiba mais** sobre outro **Componentes do Captcha** e seus serviços, como:

- [Usar o hCaptcha em um formulário adaptável para os componentes principais](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hCaptcha-core-components)

- [Usar o Captcha em um formulário adaptável para componentes de base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [Usar CAPTCHA de estrutura giratória em um formulário adaptável para componentes de base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [Usar o Google reCAPTCHA em um formulário adaptável para componentes de base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}