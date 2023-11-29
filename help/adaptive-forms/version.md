---
title: Versões dos componentes principais do AEM Forms
description: Os Componentes principais do AEM são publicados como versões que podem conter mais de uma versão dos mesmos componentes principais. Este documento explica quais são as versões e como entender a compatibilidade com os Componentes principais e o AEM.
role: Architect, Developer, Admin, User
exl-id: 8146a5b1-acf6-4b54-ad6b-6e1747a137f6
source-git-commit: a567b5ad937d426abe16c34e039e19cd0b1af5b0
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 58%

---

# Versões dos Componentes principais {#core-components-versions}

A versão atual dos Componentes principais 2.0.10 é compatível com o [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=pt-BR) e a versão 1.1.12 dos Componentes principais é compatível com as instalações [locais e no AMS do AEM Forms 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html?lang=pt-BR).

## Histórico de versão do AEM as a Cloud Service {#aem-as-cs-version-history}

A tabela subsequente apresenta uma lista das versões dos componentes principais compatíveis com o AEM as a Cloud Service que estão disponíveis no [GitHub, juntamente com detalhes abrangentes desses lançamentos](https://github.com/adobe/aem-core-forms-components/releases).

| Versão | Descrição | AEM as a Cloud Service | Java™ | Data de lançamento |
|---|---|---|---|---|
| [2.0.74](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.74) | Com esta versão, o erro de envio é atualizado para a ação Enviar no AEM Forms. | Contínuo | 8, 11 | 15 de novembro de 2023 |
| [2.0.70](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.70) | Essa versão adicionou suporte para lidar com o idioma da página de sites no contêiner de formulário. | Contínuo | 8, 11 | 10 de novembro de 2023 |
| [2.0.64](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.64) | Suporte a rich text para rótulos para componentes de Rádio/caixa de seleção. Esta versão também inclui correções para o componente de Termos e condição. | Contínuo | 8, 11 | 6 de novembro de 2023 |
| [2.0.62](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.62) | Com esta versão, o suporte para o componente de Termos e condições foi adicionado. Também foi adicionado suporte para Nome qualificado nos Componentes principais. | Contínuo | 8, 11 | 16 de outubro de 2023 |
| [2.0.60](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.60) | Esta versão inclui correções relacionadas ao recurso de propriedades personalizadas, ao Assistente e ao componente Seletor de datas. | Contínuo | 8, 11 | 12 de setembro de 2023 |
| [2.0.56](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.56) | Com esta versão, é adicionado suporte a propriedades personalizadas para todos os componentes principais. | Contínuo | 8, 11 | 12 de setembro de 2023 |
| [2.0.54](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.54) | Essa versão corrigiu o problema relacionado à localização com o componente Seletor de datas. | Contínuo | 8, 11 | 30 de agosto de 2023 |
| [2.0.52](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.52) | Suporte para usar o componente Caixa de seleção em um Formulário adaptável. | Contínuo | 8, 11 | 25 de agosto de 2023 |
| [2.0.50](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.50) | Adição de suporte para fragmentos de formulário em um Formulário adaptável com esta versão. | Contínuo | 8, 11 | 4 de agosto de 2023 |
| [2.0.48](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.48) | As principais melhorias nesta versão estão relacionadas ao desempenho do Lighthouse. | Contínuo | 8, 11 | 25 de julho de 2023 |
| [2.0.42](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.42) | A versão incorpora melhorias no final da programação. | Contínuo | 8, 11 | 18 de julho de 2023 |
| [2.0.38](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.38) | O recurso de acessibilidade foi aprimorado nesta versão. | Contínuo | 8, 11 | 17 de julho de 2023 |
| [2.0.36](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.36) | Com esta versão, você pode usar o manipulador de erros personalizado usando o Serviço de chamada do Editor de regras. | Contínuo | 8, 11 | 3 de julho de 2023 |
| [2.0.34](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.34) | Foi adicionado suporte de localização para mensagens de erro padrão, juntamente com o botão Adicionar/Remover para o componente Repetível. | Contínuo | 8, 11 | 28 de junho de 2023 |
| [2.0.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.32) | Com esta versão, o suporte para Captcha foi adicionado para o Adaptive Forms. | Contínuo | 8, 11 | 15 de junho de 2023 |
| [2.0.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.26) | Suporte para adicionar formulários adaptáveis no AEM Sites. | Contínuo | 8, 11 | 7 de junho de 2023 |
| [2.0.18](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.18) | Com esta versão, há suporte para uma repetibilidade do componente Acordeão. Também foi adicionado um novo componente como guias verticais. | Contínuo | 8, 11 | 5 de junho de 2023 |
| [2.0.10](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.10) | Com esta versão, o suporte para um componente de container de formulário adaptável é introduzido no editor de sites. | Contínuo | 8, 11 | 17 de março de 2023 |
| [2.0.8](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.8) | O recurso de repetibilidade do componente Assistente é introduzido nesta versão. | Contínuo | 8, 11 | 3 de março de 2023 |
| [2.0.6](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6) | Vários formatos para o componente principal de entrada numérica são introduzidos nesta versão. | Contínuo | 8, 11 | 08 de fevereiro de 2023 |
| [2.0.4](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6) | O suporte a componentes principais para o AEM as a Cloud Service é introduzido nesta versão. | Contínuo | 8, 11 | 30 de janeiro de 2023 |

## Histórico de versão do AEM Forms 6.5 {#aem-as-form-version-history}

A tabela subsequente apresenta uma lista das versões dos componentes principais compatíveis com o AEM 6.5 Forms no local e no AMS que estão disponíveis no [GitHub, juntamente com detalhes abrangentes desses lançamentos](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.12).

| Versão | Descrição | AEM 6.4 | AEM 6.5 | Java™ | Data de lançamento |
|---|---|---|---|---|---|
| [1.1.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.32) | Esta versão atualizou as informações de pacote do AEM Service Pack 6.5.18.0. | - | 6.5.16.0+ | 8, 11 | 15 de outubro de 2023 |
| [1.1.28](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.28) | Suporte a rich text para rótulos para componentes de Rádio/caixa de seleção. Esta versão também inclui suporte para o componente de Termos e condições. | - | 6.5.16.0+ | 8, 11 | 15 de outubro de 2023 |
| [1.1.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.26) | Com esta versão, foi adicionado suporte para o componente Caixa de seleção para Formulário adaptável. Também inclui melhorias no desempenho do Lighthouse. O manipulador de erros personalizado que usa o Invoke Service do Editor de regras também está incluído nesta versão. | - | 6.5.16.0+ | 8, 11 | 15 de outubro de 2023 |
| [1.1.24](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.24) | Foi adicionado suporte de localização para mensagens de erro padrão, juntamente com o botão Adicionar/Remover para o componente Repetível. Também foi adicionado suporte para recaptcha no Adaptive Forms. | - | 6.5.16.0+ | 8, 11 | 29 de junho de 2023 |
| [1.1.22](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.22) | Suporte para adicionar formulários adaptáveis no AEM Sites. Guia Itens adicionados na caixa de diálogo de edição do assistente e componente Guias verticais. | - | 6.5.16.0+ | 8, 11 | 07 de junho de 2023 |
| [1.1.12](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.12) | O suporte a componentes principais para os AEM Forms no local e no AMS é introduzido nesta versão. | - | 6.5.16.0+ | 8, 11 | 08 de fevereiro de 2023 |

## Consulte também {#see-also}

{{see-also}}