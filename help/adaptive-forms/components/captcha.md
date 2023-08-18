---
title: 'Componente principal de formulários adaptáveis: container de formulário'
description: Adicionar um formulário adaptável a uma página da web.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: 8db061f3d6f1041336c379b34f3b6b7f03083560
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 44%

---


# Google reCPATCHA {#google-recaptcha}

CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart) é um programa comumente usado em transações on-line para distinguir entre humanos e programas ou bots automatizados. Ele representa um desafio e avalia a resposta do usuário para determinar se é um humano ou um bot interagindo com o site. Ele impede que o usuário continue se o teste falhar e ajuda a tornar as transações online seguras, impedindo que os bots publiquem spam ou fins mal-intencionados.

O AEM Forms as a Cloud Service é compatível com o Google reCAPTCHA v2 no Adaptive Forms. Você pode usá-lo para apresentar um desafio de CAPTCHA no envio do formulário

## Uso {#reasons-to-use-google-recaptcha}


- **Prevenção de spam e bot**: um dos principais motivos para usar o reCAPTCHA é evitar que envios de spam e bots mal-intencionados inundem seu formulário. Os algoritmos avançados do reCAPTCHA podem detectar tentativas automáticas de envio do formulário, garantindo que somente usuários legítimos possam interagir com ele.

- **Segurança aprimorada**: ao implementar o reCAPTCHA, você adiciona uma camada extra de segurança ao formulário adaptável. Isso ajuda a proteger informações confidenciais e impedir que usuários mal-intencionados explorem vulnerabilidades.

- **Experiência do usuário**: Embora os CAPTCHAs possam, às vezes, ser vistos como um inconveniente, a abordagem adaptável do reCAPTCHA significa que a maioria dos usuários recebe uma experiência simplificada e amigável que requer o mínimo de interação. Isso pode ajudar a manter uma experiência do usuário positiva enquanto ainda desencoraja os bots.

- **Adaptabilidade**: o mecanismo adaptável do reCAPTCHA analisa o comportamento e as interações do usuário para determinar se são humanas ou não. Isso significa que o nível de desafio apresentado ao usuário pode variar com base na probabilidade de ser um bot. Essa adaptabilidade reduz o atrito para usuários genuínos, mantendo uma forte segurança.

- **Moderação manual reduzida**: ao reduzir significativamente o número de envios de spam e o conteúdo gerado por bots, o reCAPTCHA pode economizar tempo e recursos que, de outra forma, seriam gastos na moderação e na limpeza manuais.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal do Forms Google reCAPTCHA adaptável foi lançado em agosto de 2023 como parte da &quot;versão&quot; dos componentes principais. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível com a <br>[versão 2.0.4](/help/versions.md) e posteriores | Compatível | Compatível |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal Forms Google reCAPTCHA adaptável na documentação técnica sobre [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência do Google reCAPTCHA para visitantes com a caixa de diálogo de configuração. Você também pode definir as opções do Google reCAPTCHA com facilidade para obter uma experiência perfeita para o usuário.

### Guia Básico {#basic-tab}

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Ocultar Título**: Selecione a opção para ocultar o Título do componente.

- **Configuração** -

- **Tipo** -

- **Ocultar componente**: Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. Os dados do componente desativado não são enviados. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Validação {#validation-tab}

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

