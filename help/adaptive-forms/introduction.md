---
title: AEM Introdução aos Componentes principais adaptáveis do Forms
description: Crie experiências de inscrição atraentes (formulários) usando a flexibilidade dos Componentes principais do Adaptive Forms e forneça com o poder do Adobe Experience Manager.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 12%

---


# Introdução aos Componentes principais adaptáveis do Forms {#adaptive-forms-core-components-introduction}

Usando os Componentes principais adaptativos do Forms no Adobe Experience Manager, você pode criar experiências de inscrição atraentes utilizando as opções de flexibilidade e personalização disponíveis.

## Componentes principais   {#overview}

No Adobe Experience Manager (AEM), os componentes são os blocos de construção usados para criar páginas e formulários. Eles fornecem uma maneira simples e eficiente para os autores criarem e gerenciarem conteúdo, além de fornecerem aos desenvolvedores a flexibilidade e a extensibilidade necessárias para criar componentes personalizados.

Os são projetados para acelerar o tempo de desenvolvimento e reduzir os custos de manutenção de sites e formulários, ser flexíveis e poder ser facilmente personalizados para atender às necessidades específicas de um site e formulário.

Os Componentes principais também foram projetados para serem responsivos e oferecerem suporte a uma grande variedade de dispositivos, incluindo desktops, tablets e smartphones. Eles também seguem os padrões da Web e as práticas recomendadas mais recentes, tornando-os uma solução robusta e confiável para a criação de conteúdo da Web.

Em geral, os Componentes principais são uma ferramenta essencial para criar e gerenciar conteúdo da Web no AEM, fornecendo uma solução eficiente e flexível que pode ajudar a reduzir o tempo de desenvolvimento e os custos de manutenção, além de fornecer uma excelente experiência do usuário aos visitantes do site.

## Componentes principais adaptáveis do Forms

Os Componentes principais adaptáveis do Forms são um conjunto de 24 componentes de código aberto compatíveis com BEM, criados na base dos Componentes principais do WCM no Adobe Experience Manager. Eles foram especificamente projetados para serem usados na criação do Adaptive Forms, que são formulários que se adaptam ao dispositivo, navegador e tamanho da tela do usuário.

Esses componentes podem ser usados para criar experiências excepcionais de captura e registro de dados, fornecendo uma grande variedade de opções de campos de formulário, incluindo campos de texto, caixas de seleção, menus suspensos e muito mais. Eles também incluem recursos como validação, lógica condicional e design responsivo, que podem ser usados para criar formulários fáceis de usar e amigáveis.

Além disso, como esses componentes são de código aberto, os desenvolvedores têm a capacidade de personalizar e estender facilmente os componentes para atender às necessidades específicas de sua organização. Além disso, esses componentes são criados com base na metodologia BEM, que garante a escalabilidade e a manutenção.

![](assets/sample-adaptive-form.png)

## Recursos {#features}

|  |  |
|---|---|
| Prontos para produção | Os Componentes principais adaptáveis do Forms são 24 componentes WCM robustos. |
| Prontos para nuvem | Disponível para  [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html). |
| Versáteis | Os componentes representam conceitos genéricos com os quais os autores do Forms podem reunir quase qualquer layout. |
| Configuráveis | Nível do modelo [políticas de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=pt-BR#content-policies) defina quais recursos podem ser usados ou não. |
| Acessíveis | Cumprem o disposto no [WCAG 2.1 padrão](https://www.w3.org/TR/WCAG21/), fornecer rótulos ARIA, suportar navegação de teclado ([problemas conhecidos](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)) e texto para tecnologias de assistência, como leitores de tela. |
| Temáticos | Os componentes implementam o [Sistema de Estilos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=pt-BR), e a marcação segue as [convenções de CSS de BEM.](http://getbem.com/) |
| Personalizáveis | Vários padrões permitem fácil personalização, desde o ajuste do HTML até a reutilização de funcionalidade avançada. |
| Versões | A [política de controle de versão](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garante que os Componentes principais não interrompam seu site ao melhorar coisas que podem afetar você. |
| Código aberto | Se algo não é como deveria, contribua com sua melhoria. |

## Benefícios {#benefits}

As experiências de captura de dados são cruciais para a geração de leads e a inscrição, e os Componentes principais adaptativos da Forms fornecem uma solução poderosa para criar formulários otimizados para captura de dados. Alguns dos motivos para usar os Componentes principais para criar essas experiências em componentes de base:

* **Disponibilidade no GitHub e documentação abrangente**: Os Componentes principais adaptativos Forms AEM são de código aberto e estão disponíveis no GitHub, juntamente com uma documentação abrangente. Isso facilita para os desenvolvedores compreender os componentes e como eles funcionam, além de contribuir para seu desenvolvimento. O site aemcomponents.dev também é um recurso valioso, onde os desenvolvedores podem ver os componentes em ação e acessar a documentação detalhada.

* **Modelo BEM para estilo**: Os Componentes principais seguem o modelo BEM (Block Element Modifier) para estilo, que é uma metodologia bem estabelecida e amplamente usada para organizar o CSS. Isso facilita para os desenvolvedores entender como os estilos são organizados e como modificá-los para atender às suas necessidades específicas.

* **Sem dependência de bibliotecas de terceiros**: Uma das vantagens dos Componentes principais é que eles não têm dependência de bibliotecas JavaScript de terceiros, incluindo JQuery e Underscore. Isso torna os componentes mais rápidos e leves, além de facilitar a integração em uma implementação de AEM existente.

* **Concentre-se no desempenho e na acessibilidade**: Os Componentes principais são construídos tendo em mente o desempenho e a acessibilidade, o que se reflete em suas altas pontuações do Google Lighthouse e Web Vitals. Isso facilita para os desenvolvedores criarem páginas da Web acessíveis e de alto desempenho, o que é cada vez mais importante no cenário digital atual.

* **Componentes de Formulário no Modelo e Temas do Sites 30**: Os Componentes principais fornecem suporte para componentes de formulário no modelo e temas do Sites 30, facilitando para os desenvolvedores criarem e personalizarem formulários no AEM.

* **Estilo mais fácil**: Os Componentes principais são mais fáceis de criar estilos do que os componentes básicos. O processo de criação de temas é semelhante aos Sites, com a capacidade de herdar o mesmo tema/CSS da página Sites pai. Além disso, o modelo de BEM para estilo facilita a compreensão e a modificação dos estilos.

* **Acessibilidade**: Os Componentes principais adaptáveis do Forms são compatíveis com padrões e diretrizes de acessibilidade, como  [WCAG 2.1 padrão](https://www.w3.org/TR/WCAG21/), para garantir que os formulários possam ser usados por pessoas com deficiência, incluindo aqueles que usam tecnologias assistivas, como leitores de tela.

* **Alinhamento com a AEM Sites**: Os Componentes principais foram projetados para serem mais alinhados com o AEM Sites, tornando mais fácil para os usuários do Sites adotá-los e usá-los sem precisar aprender nada de novo. Os componentes usam o mesmo pipeline front-end que os Sites, facilitando o estilo e a modificação de sua aparência. Além disso, os pontos a seguir ilustram ainda mais esse alinhamento:

   * **Experiência de criação em linha com o editor de página**: Os Componentes principais têm uma experiência de criação alinhada ao editor de Sites, com caixas de diálogo e outras experiências semelhantes ao editor de Página. Isso facilita para os usuários do Sites a criação e o gerenciamento de formulários no contexto familiar do Editor de sites.

   * **Edição de formulário em linha no editor de Sites**: Os Componentes principais permitem a edição de formulários em linha no editor Sites, evitando a necessidade de alternar entre os editores. Isso simplifica a experiência de criação e facilita a criação e o gerenciamento de formulários.

   * **Herdar recursos do Sites no Forms**: A Forms criada em uma página Sites herda os mesmos recursos que os Sites. Isso fornece uma experiência contínua e integrada para criar e gerenciar formulários no contexto do AEM Sites

   <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->



## Requisitos {#requirements}

Os Componentes principais adaptáveis do Forms têm os seguintes requisitos.

| AEM | Complemento do AEM Forms | Componentes principais |
|---|---|---|
| AEM as a Cloud Service | Forms - Inscrição digital | [Versão 2.20.8](/help/versions.md)+ |


## Componentes principais adaptáveis do Forms {#components}

A versão atual dos Componentes principais adaptativos do Forms apresenta os seguintes componentes.

* Acordeão
* Botão
* Grupo de caixa de seleção
* Seletor de datas
* Lista suspensa
* Entrada de email
* Contêineres de formulário
* Anexo de arquivo
* Rodapé
* Cabeçalho
* Guias Horizontais
* Imagem
* Entrada do número
* Container do painel
* Botão de opção
* Botão Redefinir
* Botão enviar
* Entrada de telefone
* Entrada de texto
* Texto
* Título
* Assistente

