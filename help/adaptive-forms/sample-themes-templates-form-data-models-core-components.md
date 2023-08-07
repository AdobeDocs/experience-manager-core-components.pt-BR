---
title: Como obter temas de amostra e modelos para o AEM Forms?
description: Os Componentes principais do AEM Forms fornecem exemplos de temas de formulário adaptável, modelos e modelos de dados de formulário
solution: Experience Manager Forms
topic: Administration
role: Admin, User
hide: true
hidefromtoc: true
level: Intermediate
source-git-commit: ebbe3471164341076fe085bbef9c93fcb1fe382a
workflow-type: tm+mt
source-wordcount: '1259'
ht-degree: 5%

---


# Modelos, temas e modelos de dados de formulário de amostra {#sample-themes-templates-and-data-models}

[!DNL AEM Forms] Os Componentes principais fornecem exemplos de temas, modelos e modelos de dados de formulário prontos para uso para criar formulários adaptáveis versáteis rapidamente. Isso também ajuda os autores de formulários a aprender a extensibilidade, adaptabilidade e capacidade de resposta do [Componentes principais do AEM Forms](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-br) criar formulários simples, rápidos e complexos facilmente enquanto se conecta ao banco de dados de maneira simples.

Os exemplos de temas, modelos e modelos de dados de formulário incluídos no pacote de conteúdo de referência são:

| Modelos | Temas | Modelos de dados de formulário |
---------|----------|---------
| [Básico](#Basic) | [Tela](#Canvas) | Microsoft® Dynamics 365 |
| [Em branco](#Blank) | [WKND](#WKND) | Salesforce |
| [Entre em contato](#Contact-Us) | [Cavalete](#Easel) |  |
| [Atualização dos detalhes de contato](#Contact-Details-Update) |   |   |
| [Formulário de consentimento](#Consent-Form) | |  |
| [Registrar solicitação de serviço](#Log-Service-Request) |  |  |
| [Fornecer feedback](#Give-Feedback) |  |  |
| [Inscrição em benefícios](#Benefits-Enrollment) |  |   |
| [Resumo de benefícios do funcionário](#Employee-Benefits-Summary) |   |   |
| [Solicitação de demonstrativo da conta](#Request-for-Account-Statement) |   |   |
| [Formulário de inspeção de segurança](#Safety-Inspection) |   |   |
| [Inspeção de controle de qualidade](#Quality-Control-Inspection) |   |   |
| [Solicitação de compra](#Purchase-Request) |  |  |

## Temas de exemplo {#Sample-Themes}

Temas de amostra de referência ajudam os autores a definir e personalizar o estilo para formulários, os autores com até mesmo um conhecimento básico de CSS podem personalizar o tema de acordo com os requisitos.

**Como obter estes temas?**
* Para ativar esses temas **Forms as a Cloud Service** ambiente, [ativar os Componentes principais adaptáveis do Forms](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=pt-BR) e use o [pipeline de front-end](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html) para implantar esses temas.
* Para obter esses temas em uma **AEM 6.5 Forms** ambiente, [ativar os Componentes principais adaptáveis do Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html) e use o [gerenciador de pacotes](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components) para implantar esses temas.

A variável **pronto para uso** [Componentes principais do formulário adaptável](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-br) os temas são:

![Temas OOTB](/help/adaptive-forms/assets/OOTB-themes.png)

### Tela {#Canvas}

O tema da tela de desenho é o tema padrão para formulários e enfatiza o uso de cores básicas, transparência e ícones planos. Na captura de tela abaixo, você pode ver a aparência do tema da Tela.

![Tema da tela de desenho](/help/adaptive-forms/assets/Safety-Inspection-Theme-Canvas.png)

### WKND {#WKND}

O tema da WKND incorpora um design animado, imaginativo e envolvente para mostrar uma aparência elegante para seus formulários. O tema é baseado na aparência e estilo de [Site da WKND](https://wknd.site/us/en.html) que é um site de viagem e aventura criado na [Componentes principais do Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-br).

![Tema WKND](/help/adaptive-forms/assets/Safety-Inspection-Form-Theme.png)


### Cavalete {#Easel}

O tema de cavalete ajuda a criar uma aparência de formulário atraente e fácil de configurar, ele é personalizado para simplicidade e facilidade de uso. O tema do cavalete é baseado no conceito em que um suporte portátil usado por artistas para suportar uma tela enquanto trabalham em suas pinturas.

![Tema do cavalete](/help/adaptive-forms/assets/Safety-Inspection-Theme-Easel.png)

## Modelos de amostra {#Sample-templates}

Os modelos definem a estrutura do formulário inicial, o conteúdo e as ações a serem replicadas no formulário ou usam uma estrutura de modelo semelhante ao formulário, por exemplo, o formulário de Consentimento, o formulário de inscrição em Benefícios e muito mais.

**Como obter esses modelos?**
É possível obter os modelos implantando um [Arquétipo AEM 43 ou projeto posterior](https://github.com/adobe/aem-project-archetype) ao seu **AEM Forms as a Cloud Service** ou **AEM 6.5** ambiente do Forms.

A variável **pronto para uso** [Componentes principais do formulário adaptável](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-br) os modelos são:

![Modelos de referência](/help/adaptive-forms/assets/reference-templates-core-components.png)

### Básico {#Basic}

O modelo básico ajuda a criar rapidamente um formulário de experiência de inscrição. Também é possível usá-lo para visualizar a funcionalidade do [Componentes principais adaptáveis do Forms](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-br). Ele fornece um layout de assistente para a apresentação de dados seção a seção.

![Modelo básico](/help/adaptive-forms/assets/Basic-template-desktop-view.png)

### Em branco {#Blank}

Um modelo de tela em branco é usado para criar uma estrutura de formulário adaptável, conteúdo e regras do zero. Nenhum componente de formulário é pré-incorporado no modelo em branco.

![Modelo em branco](/help/adaptive-forms/assets/Blank-temp-desktop-view.png)

### Entre em contato {#Contact-Us}

O modelo de formulário Fale conosco é usado para criar um formulário para facilitar a comunicação entre os visitantes do site e os administradores do formulário. Os usuários podem enviar consultas, feedback ou solicitações de suporte por meio do formulário.

![Modelo Fale Conosco](/help/adaptive-forms/assets/Contact-us-desktop-view.png)

### Atualização de detalhes de contato {#Contact-Details-Update}

Os autores do modelo de atualização de detalhes de contato ajudam a criar um formulário para atualização de endereço e detalhes de contato dos clientes. O formulário também auxilia os clientes na atualização de informações pessoais relacionadas a assinaturas ou benefícios para garantir comunicação contínua e acesso ininterrupto aos serviços ou benefícios.

![Contact-details-update](/help/adaptive-forms/assets/Contact-details-update.png)

### Formulário de consentimento {#Consent-Form}

O modelo de formulário de consentimento é usado para criar um formulário para obter um documento legal dos participantes que participam de uma atividade específica, estudo de pesquisa, procedimento médico ou qualquer situação em que suas informações pessoais ou direitos possam estar envolvidos. O formulário garante a transparência, protege os direitos do participante e estabelece uma compreensão clara do que o indivíduo está concordando.

![Formulário de consentimento](/help/adaptive-forms/assets/Consent-form-desktop-view.png)

### Solicitação de serviço de log {#Log-Service-Request}

O modelo de solicitação de serviço de log ajuda a criar um formulário que solicita serviços de log específicos de um provedor de serviços. O formulário serve como uma solicitação formal para criar um ticket para eventos, atividades ou dados registrados para status de monitoramento ou rastreamento.

![Modelo de Solicitação de Serviço de Log](/help/adaptive-forms/assets/Log-service-request-desktop-view.png)


### Fornecer Feedback {#Give-Feedback}

Fornecer o modelo de formulário de feedback ajuda a criar um formulário para fornecer feedback construtivo a outra pessoa ou equipe. O formulário ajuda a garantir que o feedback seja claro, específico e acionável, promovendo a comunicação aberta e o aprimoramento.

![Fornecer Modelo de Feedback](/help/adaptive-forms/assets/Give-feedback-desktop-view.png)


### Inscrição em Benefícios {#Benefits-Enrollment}

O modelo de formulário de inscrição de benefícios é usado para criar um formulário para coletar informações essenciais de seus funcionários sobre seus benefícios preferidos e opções de cobertura. Normalmente, acompanha o período anual de inscrição de benefícios.

![Modelo de Inscrição de Benefícios](/help/adaptive-forms/assets/Benefits-enrollment-form-template.png)


### Resumo dos Benefícios do Funcionário {#Employee-Benefits-Summary}

O modelo de formulário de resumo de benefícios do funcionário é usado para criar um formulário para reunir detalhes essenciais sobre os benefícios de um indivíduo. Ele ajuda a avaliar a cobertura de forma rápida e precisa, fornecendo uma visão geral abrangente para assistência e suporte eficientes.
![Resumo dos Benefícios do Funcionário](/help/adaptive-forms/assets/Employee-benefits-summary.png)


### Solicitação de Extrato de Conta {#Request-for-Account-Statement}

O modelo de solicitação de demonstrativo de conta ajuda a criar um formulário que inicia o processo de obtenção de um demonstrativo preciso e atualizado dos clientes. O demonstrativo fornece um registro detalhado de transações financeiras, atividades ou outras informações relevantes sobre clientes que usam este formulário.

![Solicitação de extrato de conta](/help/adaptive-forms/assets/Request-for-account-statment.png)

### Inspeção de segurança {#Safety-Inspection}

O modelo de formulário de inspeção de segurança ajuda a criar um formulário para inserir detalhes de um ambiente de trabalho seguro. Através da realização de inspeções regulares utilizando esta forma, podem ser identificados potenciais perigos. O formulário abrange vários aspectos, como saídas de emergência, segurança contra incêndio, segurança elétrica, materiais perigosos, equipamento de proteção individual, ergonomia de estação de trabalho para a segurança e o bem-estar de funcionários, visitantes e clientes.

![Formulário de inspeção de segurança](/help/adaptive-forms/assets/Safety-inspection-form.png)

### Inspeção de Controle de Qualidade {#Quality-Control-Inspection}

O modelo de formulário de inspeção de controle de qualidade é usado para criar um formulário para avaliar e documentar a aparência visual, as dimensões, a funcionalidade, a documentação, os resultados de testes e a qualidade geral de um produto ou item. Ajuda a identificar defeitos, não-conformidades e ações corretivas necessárias para garantir a adesão aos padrões de qualidade.

![Inspeção de Controle de Qualidade](/help/adaptive-forms/assets/Quality-Control-Inspection.png)


### Solicitação de compra {#Purchase-Request}

O modelo de formulário de solicitação de compra ajuda a criar um formulário para iniciar o processo de aquisição e permite que os funcionários solicitem formalmente a compra de mercadorias ou serviços necessários para seu trabalho. O formulário captura detalhes essenciais como descrição do item, quantidade, fornecedor preferido (se aplicável), alocação de orçamento, justificativa para compra, informações de distribuição e aprovações necessárias.

![purchase-request-form](/help/adaptive-forms/assets/Purchase-request-form.png)

## Modelos de dados do formulário de referência {#reference-models}

Depois de criar um formulário adaptável com base em [Componente principal](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-br), você pode conectar seu formulário ao banco de dados Microsoft® Dynamics 365 e servidores Salesforce para habilitar fluxos de trabalho de negócios. Por exemplo:

* Grave dados no Microsoft® Dynamics 365 e Salesforce no envio do Formulário adaptável.
* Grave dados no Microsoft® Dynamics 365 e Salesforce por meio de entidades personalizadas definidas no Modelo de dados de formulário e vice-versa.
* Consulte o servidor Microsoft® Dynamics 365 e Salesforce para obter dados e preencher previamente o Forms adaptável.
* Ler dados do servidor Microsoft® Dynamics 365 e Salesforce.

Você pode obter os seguintes Modelos de dados de formulário instalando o [Pacote de conteúdo de referência](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-forms-reference-content.ui.content-2.1.0.zip):

* Microsoft® Dynamics 365
* Salesforce

Para obter informações sobre como usar esses modelos, consulte [Configurar os serviços em nuvem do Microsoft® Dynamics 365 e Salesforce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/configure-msdynamics-salesforce.html#configure-dynamics-cloud-service)
