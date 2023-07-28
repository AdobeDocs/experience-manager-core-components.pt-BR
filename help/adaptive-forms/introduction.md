---
title: Introdução aos Componentes principais dos Formulários adaptáveis do AEM
description: Crie experiências de inscrição atraentes (formulários) usando a flexibilidade dos Componentes principais dos Formulários adaptáveis e as disponibilize com a eficiência do Adobe Experience Manager.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: ht
source-wordcount: '1262'
ht-degree: 100%

---

# Introdução aos Componentes principais dos Formulários adaptáveis {#adaptive-forms-core-components-introduction}

Usando os Componentes principais dos Formulários adaptáveis no Adobe Experience Manager, você pode criar experiências de inscrição atraentes utilizando as opções de flexibilidade e personalização disponíveis.

## Componentes principais  {#overview}

No Adobe Experience Manager (AEM), os componentes são os elementos usados para criar páginas e formulários. Eles fornecem uma maneira simples e eficiente para os autores criarem e gerenciarem conteúdo, além de fornecerem aos desenvolvedores a flexibilidade e a extensibilidade necessárias para criar componentes personalizados. Eles foram projetados para acelerar o tempo de desenvolvimento e reduzir os custos de manutenção de sites e formulários, ser flexíveis e poder ser facilmente personalizados para atender às necessidades específicas de um site e formulário.

Os Componentes principais também foram projetados para serem responsivos e oferecerem suporte a uma grande variedade de dispositivos, incluindo desktops, tablets e smartphones. Eles também seguem os padrões da Web e as práticas recomendadas mais recentes, tornando-os uma solução robusta e confiável para a criação de conteúdo da Web.

Em geral, os Componentes principais são uma ferramenta essencial para criar e gerenciar conteúdo da Web no AEM, fornecendo uma solução eficiente e flexível que pode ajudar a reduzir o tempo de desenvolvimento e os custos de manutenção, além de fornecer uma excelente experiência do usuário aos visitantes do site.

## Componentes principais dos Formulários adaptáveis

Os Componentes principais dos Formulários adaptáveis são um conjunto de 24 componentes de código aberto compatíveis com BEM, criados na base dos Componentes principais do WCM no Adobe Experience Manager. Eles foram especificamente projetados para serem usados na criação dos Formulários adaptáveis, que são formulários que se adaptam ao dispositivo, navegador e tamanho da tela do usuário.

Esses componentes podem ser usados para criar experiências excepcionais de captura e registro de dados, fornecendo uma grande variedade de opções de campos de formulário, incluindo campos de texto, caixas de seleção, menus suspensos e muito mais. Eles também incluem recursos como validação, lógica condicional e design responsivo, que podem ser usados para criar formulários fáceis de usar e intuitivos.

Além disso, como esses componentes são de código aberto, os desenvolvedores têm a capacidade de personalizar e estender facilmente os componentes para atender às necessidades específicas de sua organização. Além disso, esses componentes são criados com base na metodologia BEM, que garante a capacidade de expansão e manutenção.

![](assets/sample-adaptive-form.png)

## Recursos {#features}

|  |  |
|---|---|
| Prontos para produção | Os Componentes principais dos Formulários adaptáveis são 24 componentes WCM robustos. |
| Prontos para nuvem | Disponível para o [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=pt-BR). |
| Versáteis | Os componentes representam conceitos genéricos com os quais os autores do Forms podem reunir quase qualquer layout. |
| Configuráveis | As [políticas de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=pt-BR#content-policies) no nível do modelo definem quais recursos podem ser ou não usados. |
| Acessíveis | Eles fornecem rótulos ARIA, são compatíveis com a navegação por teclado e o texto para tecnologias de assistência, como leitores de tela. |
| Tema | Os componentes implementam o [Sistema de Estilos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=pt-BR), e a marcação segue as [convenções de CSS de BEM.](https://getbem.com/) |
| Personalizáveis | Vários padrões permitem fácil personalização, desde o ajuste do HTML até a reutilização de funcionalidade avançada. |
| Versões | A [política de controle de versão](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garante que os Componentes principais não interrompam seu site ao melhorar coisas que podem afetar você. |
| Código aberto | Se algo não sair como deveria, contribua com melhorias. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Benefícios {#benefits}

As experiências de captura de dados são cruciais para a geração de leads e inscrição, e os Componentes principais dos Formulários adaptáveis fornecem uma solução eficiente para criar formulários otimizados para captura de dados. Alguns dos motivos para usar os Componentes principais para criar essas experiências em componentes de base são:

* **Disponibilidade no GitHub e documentação abrangente**: os Componentes principais dos Formulários adaptáveis do AEM são de código aberto e estão disponíveis no GitHub, juntamente com uma documentação abrangente. Isso facilita para os desenvolvedores compreender os componentes e como eles funcionam, além de contribuir para seu desenvolvimento. O site [aemcomponents.dev](https://www.aemcomponents.dev/) também é um recurso valioso, em que os desenvolvedores podem ver os componentes em ação e acessar a documentação detalhada.

* **Modelo BEM para estilo**: os Componentes principais seguem o modelo BEM (Modificador de elemento de bloco) para estilo, que é uma metodologia bem estabelecida e amplamente usada para organizar o CSS. Isso facilita para os desenvolvedores entender como os estilos são organizados e como modificá-los para atender às suas necessidades específicas.

* **Sem dependência de bibliotecas de terceiros**: uma das vantagens dos Componentes principais é que eles não têm dependência de bibliotecas JavaScript de terceiros, incluindo JQuery e Underscore. Isso torna os componentes mais rápidos e leves, além de facilitar a integração em uma implementação existente do AEM.

* **Foco no desempenho e na acessibilidade**: os Componentes principais são construídos pensando no desempenho e na acessibilidade, o que se reflete em suas altas pontuações do Google Lighthouse e Web Vitals. Isso facilita para os desenvolvedores criarem páginas da Web acessíveis e de alto desempenho, o que é cada vez mais importante no cenário digital atual.

* **Componentes de formulários no Modelo e Temas do Sites 30**: os Componentes principais fornecem suporte para componentes de formulário no modelo e temas do Sites 30, facilitando para os desenvolvedores criarem e personalizarem formulários no AEM.

* **Mais fácil de criar estilo**: é mais fácil criar estilos nos Componentes principais do que os componentes básicos. O processo de criação de temas é semelhante ao Sites, com a capacidade de herdar o mesmo tema/CSS da página principal do Sites. Além disso, o modelo BEM para estilo facilita a compreensão e a modificação dos estilos.

* **Acessibilidade**: os Componentes principais dos Formulários adaptáveis são compatíveis com padrões e diretrizes de acessibilidade para garantir que os formulários possam ser usados por pessoas com deficiência, inclusive quem usa tecnologias de assistência, como leitores de tela

## Componentes principais dos formulários adaptáveis {#components}

A versão atual dos Componentes principais de Formulários adaptáveis apresenta os componentes listados abaixo.

* [Acordeão](/help/adaptive-forms/components/accordion.md)
* [Botão](/help/adaptive-forms/components/button.md)
* [Grupo de Caixa de seleção](/help/adaptive-forms/components/checkbox-group.md)
* [Seletor de data](/help/adaptive-forms/components/date-picker.md)
* [Lista suspensa](/help/adaptive-forms/components/drop-down.md)
* [Entrada de email](/help/adaptive-forms/components/email-input.md)
* [Containeres de formulário](/help/adaptive-forms/components/form-container.md)
* [Anexo de arquivo](/help/adaptive-forms/components/file-attachment.md)
* [Rodapé](/help/adaptive-forms/components/footer.md)
* [Cabeçalho](/help/adaptive-forms/components/header.md)
* [Guias horizontais](/help/adaptive-forms/components/horizontal-tabs.md)
* [Imagem](/help/adaptive-forms/components/image.md)
* [Entrada de número](/help/adaptive-forms/components/number-input.md)
* [Container do painel](/help/adaptive-forms/components/panel-container.md)
* [Botão de opção](/help/adaptive-forms/components/radio-button.md)
* [Botão Redefinir](/help/adaptive-forms/components/reset-button.md)
* [Botão Enviar](/help/adaptive-forms/components/submit-button.md)
* [Entrada de telefone](/help/adaptive-forms/components/telephone-input.md)
* [Entrada de texto](/help/adaptive-forms/components/text-input.md)
* [Texto](/help/adaptive-forms/components/text.md)
* [Título](/help/adaptive-forms/components/title.md)
* [Assistente](/help/adaptive-forms/components/wizard.md)

## Configuração dos Componentes principais dos formulários adaptáveis

A ativação dos Componentes principais dos formulários adaptáveis no AEM Forms as a Cloud Service permite criar, publicar e fornecer os Componentes principais baseados em formulários, adaptáveis e headless, usando as instâncias do AEM Forms Cloud Service para vários canais. Para obter instruções detalhadas sobre como habilitar os Componentes principais dos formulários adaptáveis, consulte [Habilitar componentes principais de formulários adaptáveis no AEM Forms as a Cloud Service e no ambiente de desenvolvimento local](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=pt-BR).

Os Componentes principais dos Formulários adaptáveis têm os seguintes requisitos.

| AEM Versão | Complemento do AEM Forms | Componentes principais dos formulários adaptáveis |
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
