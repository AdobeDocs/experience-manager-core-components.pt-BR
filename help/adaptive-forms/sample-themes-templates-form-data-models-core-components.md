---
title: Como obter temas de amostra e modelos para o AEM Forms?
description: Os Componentes principais do AEM Forms fornecem temas de amostra de formulários adaptáveis, modelos e modelos de dados de formulário
solution: Experience Manager Forms
topic: Administration
role: Admin, User
hide: true
hidefromtoc: true
level: Intermediate
source-git-commit: ebbe3471164341076fe085bbef9c93fcb1fe382a
workflow-type: ht
source-wordcount: '1259'
ht-degree: 100%

---


# Temas de amostra, modelos e modelos de dados de formulário {#sample-themes-templates-and-data-models}

Os Componentes principais do [!DNL AEM Forms] fornecem temas de amostra, modelos e modelos de dados de formulário prontos para uso para a criação de formulários adaptáveis versáteis com rapidez. Isso também ajuda os autores de formulários a entender a extensibilidade, adaptabilidade e capacidade de resposta dos [Componentes principais do AEM Forms](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-BR) para criar formulários simples e complexos de forma rápida e fácil enquanto se conectam ao banco de dados de forma contínua.

Os temas de amostra, modelos e modelos de dados de formulário incluídos no pacote de conteúdo de referência são:

| Modelos | Temas | Modelos de dados de formulário |
---------|----------|---------
| [Básico](#Basic) | [Tela de desenho](#Canvas) | Microsoft® Dynamics 365 |
| [Em branco](#Blank) | [WKND](#WKND) | Salesforce |
| [Fale conosco](#Contact-Us) | [Cavalete](#Easel) |  |
| [Atualização dos detalhes de contato](#Contact-Details-Update) |   |   |
| [Formulário de consentimento](#Consent-Form) | |  |
| [Solicitação de serviço de log](#Log-Service-Request) |  |  |
| [Fornecimento de feedback](#Give-Feedback) |  |  |
| [Inscrição em benefícios](#Benefits-Enrollment) |  |   |
| [Resumo de benefícios do funcionário](#Employee-Benefits-Summary) |   |   |
| [Solicitação de demonstrativo de conta](#Request-for-Account-Statement) |   |   |
| [Formulário de inspeção de segurança](#Safety-Inspection) |   |   |
| [Inspeção de controle de qualidade](#Quality-Control-Inspection) |   |   |
| [Solicitação de compra](#Purchase-Request) |  |  |

## Temas de amostra {#Sample-Themes}

Temas de amostra de referência ajudam autores a definir e personalizar o estilo de formulários, mesmo autores com apenas um conhecimento básico de CSS podem personalizar o tema como necessário.

**Como obter estes temas?**
* Para obter esses temas no ambiente do **Forms as a Cloud Service**, [habilite os Componentes principais dos Formulários Adaptáveis](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=pt-BR) e use o [pipeline de front-end](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=pt-BR) para implantar esses temas.
* Para obter esses temas em um ambiente **AEM Forms 6.5**, [habilite os Componentes principais dos Formulários adaptáveis](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html?lang=pt-BR) e use o [gerenciador de pacotes](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components?lang=pt-BR) para implantar esses temas.

Os temas de [Componentes principais de Formulários adaptáveis](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-BR) **prontos para uso** são:

![Temas OOTB](/help/adaptive-forms/assets/OOTB-themes.png)

### Tela de desenho {#Canvas}

O tema Tela de desenho é o tema padrão para formulários e enfatiza o uso de cores básicas, transparência e ícones planos. Na captura de tela abaixo, é possível ver a aparência do tema Tela de desenho.

![Tema Tela de desenho](/help/adaptive-forms/assets/Safety-Inspection-Theme-Canvas.png)

### WKND {#WKND}

O tema WKND incorpora um design animado, imaginativo e envolvente para dar uma aparência elegante aos seus formulários. O tema é baseado na aparência e estilo do [Site WKND](https://wknd.site/us/en.html), que é um site de viagens e aventura criado com os [Componentes principais do Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-BR).

![Tema WKND](/help/adaptive-forms/assets/Safety-Inspection-Form-Theme.png)


### Cavalete {#Easel}

O tema Cavalete ajuda a criar uma aparência de formulário atraente e fácil de configurar, sendo personalizado para simplicidade e facilidade de uso. O tema Cavalete é baseado no conceito do suporte portátil usado por artistas para sustentar uma tela enquanto trabalham em suas pinturas.

![Tema Cavalete](/help/adaptive-forms/assets/Safety-Inspection-Theme-Easel.png)

## Modelos de amostra {#Sample-templates}

No formulário, os modelos definem a estrutura inicial, o conteúdo e as ações a serem replicadas, ou usam uma estrutura de modelo semelhante ao formulário, por exemplo, o formulário de consentimento, o formulário de inscrição de benefícios e muito mais.

**Como obter esses modelos?**
É possível obter os modelos implantando um [projeto baseado no Arquétipo AEM 43 ou posterior](https://github.com/adobe/aem-project-archetype) no seu ambiente do **AEM Forms as a Cloud Service** ou do **AEM Forms 6.5**.

Os modelos **prontos para uso** dos [Componentes principais de Formulário Adaptável](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-BR) são:

![Modelos de referência](/help/adaptive-forms/assets/reference-templates-core-components.png)

### Básico {#Basic}

O modelo básico ajuda a criar rapidamente um formulário de experiência de inscrição. Também é possível usá-lo para visualizar a funcionalidade dos [Componentes principais dos Formulários adaptáveis](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-BR). O modelo básico fornece um layout de assistente para a apresentação de dados seção a seção.

![Modelo básico](/help/adaptive-forms/assets/Basic-template-desktop-view.png)

### Em branco {#Blank}

Um modelo de tela em branco é usado para criar a estrutura, o conteúdo e as regras de um formulário adaptável do zero. Nenhum componente de formulário é pré-incorporado ao modelo em branco.

![Modelo em branco](/help/adaptive-forms/assets/Blank-temp-desktop-view.png)

### Fale conosco {#Contact-Us}

O modelo de formulário Fale conosco é usado na criação de um formulário para facilitar a comunicação entre os visitantes do site e os administradores do formulário. Os usuários podem enviar consultas, feedback ou solicitações de suporte por meio do formulário.

![Modelo Fale Conosco](/help/adaptive-forms/assets/Contact-us-desktop-view.png)

### Atualização de detalhes de contato {#Contact-Details-Update}

O modelo de atualização de detalhes de contato ajuda autores a criar um formulário para atualização de endereço e detalhes de contato de clientes. O formulário também auxilia clientes na atualização de informações pessoais relacionadas a assinaturas ou benefícios para garantir comunicação contínua e acesso ininterrupto aos serviços ou benefícios.

![Contact-details-update](/help/adaptive-forms/assets/Contact-details-update.png)

### Formulário de consentimento {#Consent-Form}

O modelo de formulário de Consentimento é usado na criação de um formulário para obter um documento legal de participantes que fazem parte de uma atividade específica, pesquisa, procedimento médico ou qualquer situação em que suas informações pessoais ou direitos possam estar envolvidos. O formulário garante a transparência, protege os direitos do participante e estabelece uma compreensão clara do que o indivíduo está concordando.

![Formulário de Consentimento](/help/adaptive-forms/assets/Consent-form-desktop-view.png)

### Solicitação de serviço de log {#Log-Service-Request}

O modelo de solicitação de serviço de log ajuda a criar um formulário que solicita serviços de registro de logs específicos de um provedor de serviços. O formulário serve como uma solicitação formal para criar um ticket de eventos, atividades ou dados registrados para o monitoramento ou acompanhamento de status.

![Modelo de Solicitação de serviço de log](/help/adaptive-forms/assets/Log-service-request-desktop-view.png)


### Fornecimento de feedback {#Give-Feedback}

O modelo de formulário de Fornecimento de feedback ajuda na criação de um formulário para fornecer feedback construtivo a outra pessoa ou equipe. O formulário ajuda a garantir que o feedback seja claro, específico e acionável, promovendo uma comunicação aberta e o aprimoramento.

![Modelo de Fornecimento de feedback](/help/adaptive-forms/assets/Give-feedback-desktop-view.png)


### Inscrição em benefícios {#Benefits-Enrollment}

O modelo de formulário de Inscrição em benefícios é usado na criação de um formulário para coletar informações essenciais de funcionários sobre seus benefícios preferenciais e opções de cobertura. Normalmente, acompanha o período anual de inscrição em benefícios.

![Modelo de Inscrição em benefícios](/help/adaptive-forms/assets/Benefits-enrollment-form-template.png)


### Resumo de benefícios do funcionário {#Employee-Benefits-Summary}

O modelo de formulário de Resumo de benefícios do funcionário é usado na criação de um formulário para reunir detalhes essenciais sobre os benefícios de um indivíduo. O formulário ajuda a avaliar a cobertura de forma rápida e precisa, fornecendo uma visão geral abrangente para assistência e suporte eficientes.
![Resumo de benefícios do funcionário](/help/adaptive-forms/assets/Employee-benefits-summary.png)


### Solicitação de demonstrativo de conta {#Request-for-Account-Statement}

O modelo de Solicitação de demonstrativo de conta ajuda a criar um formulário que inicia o processo de obtenção de um demonstrativo preciso e atualizado de clientes. O demonstrativo fornece um registro detalhado de transações financeiras, atividades ou outras informações relevantes sobre clientes que usam este formulário.

![Request-for-account-statment](/help/adaptive-forms/assets/Request-for-account-statment.png)

### Inspeção de segurança {#Safety-Inspection}

O modelo de formulário de Inspeção de segurança ajuda a criar um formulário onde serão inseridos detalhes para um ambiente de trabalho seguro. Através da realização de inspeções regulares utilizando este formulário, será possível identificar perigos em potencial. O formulário abrange vários aspectos, como saídas de emergência, segurança contra incêndio, segurança elétrica, materiais perigosos, equipamento de proteção individual e ergonomia da estação de trabalho para a segurança e o bem-estar de funcionários, visitantes e clientes.

![Formulário de Inspeção de segurança](/help/adaptive-forms/assets/Safety-inspection-form.png)

### Inspeção de controle de qualidade {#Quality-Control-Inspection}

O modelo de formulário de Inspeção de controle de qualidade é usado na criação de um formulário para avaliar e documentar a aparência visual, as dimensões, a funcionalidade, a documentação, os resultados de testes e a qualidade geral de um produto ou item. Ajuda a identificar defeitos, não-conformidades e ações corretivas necessárias para garantir a adesão aos padrões de qualidade.

![Inspeção de controle de qualidade](/help/adaptive-forms/assets/Quality-Control-Inspection.png)


### Solicitação de compra {#Purchase-Request}

O modelo de formulário de Solicitação de compra ajuda a criar um formulário para iniciar o processo de aquisição e permitir que funcionários solicitem formalmente a compra de mercadorias ou serviços necessários para seu trabalho. O formulário captura detalhes essenciais como descrição do item, quantidade, fornecedor preferido (se aplicável), alocação de orçamento, justificativa para compra, informações de distribuição e aprovações necessárias.

![purchase-request-form](/help/adaptive-forms/assets/Purchase-request-form.png)

## Modelos de dados de formulário de referência {#reference-models}

Depois de criar um formulário adaptável com base nos [Componentes principais](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=pt-BR), você pode conectar o formulário ao banco de dados dos servidores do Microsoft® Dynamics 365 e do Salesforce para habilitar os fluxos de trabalho comerciais. Por exemplo:

* Grave dados no Microsoft® Dynamics 365 e Salesforce no envio de um Formulário adaptável.
* Grave dados no Microsoft® Dynamics 365 e Salesforce por meio de entidades personalizadas definidas no Modelo de dados de formulário e vice-versa.
* Consulte o servidor do Microsoft® Dynamics 365 e do Salesforce para obter dados e preencher previamente os formulários adaptáveis.
* Leia dados do servidor do Microsoft® Dynamics 365 e do Salesforce.

É possível obter os seguintes Modelos de dados de formulário instalando o [Pacote de conteúdo de referência](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-forms-reference-content.ui.content-2.1.0.zip):

* Microsoft® Dynamics 365
* Salesforce

Para obter informações sobre como usar esses modelos, consulte [Configuração dos serviços na nuvem do Microsoft® Dynamics 365 e do Salesforce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/configure-msdynamics-salesforce.html?lang=pt-BR#configure-dynamics-cloud-service)
