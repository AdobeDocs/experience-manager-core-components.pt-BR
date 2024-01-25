---
title: Versões dos componentes principais do AEM Forms
description: Os Componentes principais do AEM são publicados como versões que podem conter mais de uma versão dos mesmos componentes principais. Este documento explica quais são as versões e como entender a compatibilidade com os Componentes principais e o AEM.
role: Architect, Developer, Admin, User
exl-id: 8146a5b1-acf6-4b54-ad6b-6e1747a137f6
source-git-commit: 5ba402a0f781f73fe7eb5afc9b4beb47ba28851e
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 91%

---

# Versões dos Componentes principais {#core-components-versions}

A versão atual dos Componentes principais 2.0.10 é compatível com o [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=pt-BR) e a versão 1.1.12 dos Componentes principais é compatível com as instalações [locais e no AMS do AEM Forms 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html?lang=pt-BR).

## Histórico de versão do AEM as a Cloud Service {#aem-as-cs-version-history}

A tabela subsequente apresenta uma lista das versões dos componentes principais compatíveis com o AEM as a Cloud Service que estão disponíveis no [GitHub, juntamente com detalhes abrangentes desses lançamentos](https://github.com/adobe/aem-core-forms-components/releases).

| Versão | Descrição | AEM as a Cloud Service | Java™ | Data de lançamento |
|---|---|---|---|---|
| [2.0.76](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.76) | Com esta versão, a guia Estilo e a guia Propriedades personalizadas serão corrigidas para o componente Termos e condições. Essa versão também corrigiu o componente Botão de opção para salvar valor booleano no primeiro clique. | Contínuo | 8, 11 | 15 de novembro de 2023 |
| [2.0.74](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.74) | Com esta versão, o erro de envio foi atualizado para a Ação de envio no AEM Forms. | Contínuo | 8, 11 | 15 de novembro de 2023 |
| [2.0.70](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.70) | Esta versão adicionou suporte para manipular o idioma da página de sites no container de formulário. | Contínuo | 8, 11 | 10 de novembro de 2023 |
| [2.0.64](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.64) | Suporte a rich text para rótulos de componentes de caixa de seleção e botão de opção. Com esta versão, o suporte para o componente Switch também foi adicionado. Esta versão também inclui correções para o componente de Termos e condições. | Contínuo | 8, 11 | 6 de novembro de 2023 |
| [2.0.62](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.62) | Esta versão adiciona suporte para o componente de Termos e condições. Também foi adicionado suporte ao uso de nomes qualificados em componentes principais. | Contínuo | 8, 11 | 16 de outubro de 2023 |
| [2.0.60](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.60) | Esta versão inclui correções relacionadas ao recurso de propriedades personalizadas e aos componentes Assistente e Seletor de data. | Contínuo | 8, 11 | 12 de setembro de 2023 |
| [2.0.56](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.56) | Esta versão adiciona suporte a propriedades personalizadas para todos os componentes principais. | Contínuo | 8, 11 | 12 de setembro de 2023 |
| [2.0.54](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.54) | Esta versão corrigiu o problema relacionado à localização do componente Seletor de data. | Contínuo | 8, 11 | 30 de agosto de 2023 |
| [2.0.52](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.52) | Suporte ao uso do componente de caixa de seleção em um formulário adaptável. | Contínuo | 8, 11 | 25 de agosto de 2023 |
| [2.0.50](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.50) | Esta versão adiciona suporte para fragmentos de formulário em um formulário adaptável. | Contínuo | 8, 11 | 4 de agosto de 2023 |
| [2.0.48](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.48) | As principais melhorias desta versão estão relacionadas ao desempenho do Lighthouse. | Contínuo | 8, 11 | 25 de julho de 2023 |
| [2.0.42](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.42) | Esta versão adiciona melhorias para o ambiente de programação. | Contínuo | 8, 11 | 18 de julho de 2023 |
| [2.0.38](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.38) | Esta versão aprimorou o recurso de acessibilidade. | Contínuo | 8, 11 | 17 de julho de 2023 |
| [2.0.36](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.36) | Esta versão permite usar o manipulador de erros personalizado por meio do serviço de chamada do editor de regras. | Contínuo | 8, 11 | 3 de julho de 2023 |
| [2.0.34](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.34) | Adição de suporte de localização para mensagens de erro padrão, além do botão Adicionar/Remover para o componente repetível. | Contínuo | 8, 11 | 28 de junho de 2023 |
| [2.0.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.32) | Esta versão adiciona suporte de Captcha para formulários adaptáveis. | Contínuo | 8, 11 | 15 de junho de 2023 |
| [2.0.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.26) | Suporte para a adição de formulários adaptáveis no AEM Sites. | Contínuo | 8, 11 | 7 de junho de 2023 |
| [2.0.18](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.18) | Esta versão adiciona suporte para a repetição do componente de acordeão. Também foi adicionado um novo componente como guias verticais. | Contínuo | 8, 11 | 5 de junho de 2023 |
| [2.0.10](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.10) | Com esta versão, o suporte para um componente de container de formulário adaptável é introduzido no editor de sites. | Contínuo | 8, 11 | 17 de março de 2023 |
| [2.0.8](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.8) | O recurso de repetibilidade do componente Assistente foi introduzido nesta versão. | Contínuo | 8, 11 | 3 de março de 2023 |
| [2.0.6](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6) | Vários formatos para o componente principal de entrada numérica são introduzidos nesta versão. | Contínuo | 8, 11 | 08 de fevereiro de 2023 |
| [2.0.4](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6) | O suporte a componentes principais para o AEM as a Cloud Service é introduzido nesta versão. | Contínuo | 8, 11 | 30 de janeiro de 2023 |

## Histórico de versão do AEM Forms 6.5 {#aem-as-form-version-history}

A tabela subsequente apresenta uma lista das versões dos componentes principais compatíveis com o AEM 6.5 Forms no local e no AMS que estão disponíveis no [GitHub, juntamente com detalhes abrangentes desses lançamentos](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.12).

| Versão | Descrição | AEM 6.4 | AEM 6.5 | Java™ | Data de lançamento |
|---|---|---|---|---|---|
| [1.1.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.32) | Esta versão atualizou os detalhes do pacote de informações do Pacote de serviços do AEM 6.5.18.0. | - | 6.5.16.0+ | 8, 11 | 15 de outubro de 2023 |
| [1.1.28](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.28) | Suporte a rich text para rótulos de componentes de caixa de seleção e botão de opção. Esta versão também inclui suporte para o componente de Termos e condições e componentes de Switch. | - | 6.5.16.0+ | 8, 11 | 15 de outubro de 2023 |
| [1.1.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.26) | Com esta versão, foi adicionado suporte para o componente Caixa de seleção para Formulário adaptável e fragmentos de formulário. Ela também inclui melhorias no desempenho do Lighthouse. Esta versão também inclui um manipulador de erros personalizado que utiliza o serviço de chamada do Editor de regras. | - | 6.5.16.0+ | 8, 11 | 15 de outubro de 2023 |
| [1.1.24](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.24) | Adição de suporte de localização para mensagens de erro padrão, além do botão Adicionar/Remover para o componente repetível. Também foi adicionado suporte de recaptcha para formulários adaptáveis. | - | 6.5.16.0+ | 8, 11 | 29 de junho de 2023 |
| [1.1.22](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.22) | Suporte para a adição de formulários adaptáveis no AEM Sites. Adição da guia Itens na caixa de diálogo de edição dos componentes Assistente e Guias verticais. | - | 6.5.16.0+ | 8, 11 | 07 de junho de 2023 |
| [1.1.12](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.12) | O suporte a componentes principais para os AEM Forms no local e no AMS é introduzido nesta versão. | - | 6.5.16.0+ | 8, 11 | 08 de fevereiro de 2023 |

## Consulte também {#see-also}

{{see-also}}