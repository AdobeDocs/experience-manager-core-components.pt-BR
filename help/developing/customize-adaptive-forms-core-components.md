---
title: Personalizar os componentes principais adaptáveis do Forms
description: Saiba como estender ou criar um Componente principal adaptável do Forms para implementar a funcionalidade personalizada para sua organização.
role: Architect, Developer, Admin
source-git-commit: 9a80b453d6a6cf7b347128654d3b5e673a063505
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 3%

---


# Personalizar os componentes principais adaptáveis do Forms

A personalização dos Componentes principais do Adaptive Forms permite que você personalize as funcionalidades prontas para uso para atender às suas necessidades específicas. Este guia o orienta pelo processo de personalização desses componentes para criar uma experiência mais personalizada.

## Pré-requisito

Antes de mergulhar na personalização dos Componentes principais do Forms adaptável,

* Saiba mais sobre o [arquitetura de um Core Components](customizing.md#customizing-the-markup-customizing-the-markup) e passe pelo [documentação oficial dos Componentes principais do Adobe Experience Manager](customizing.md). Esses recursos abrangentes servem como guia durante todo o processo de personalização.
* Configurar o ambiente de desenvolvimento Isso garante um fluxo de trabalho suave para fazer alterações nos componentes principais. Ao configurar o ambiente de desenvolvimento, use um projeto do Arquétipo AEM com base no projeto do Arquétipo AEM mais recente. Com base em seu ambiente, você pode:

   * [Configurar um ambiente de desenvolvimento local para o Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html).
   * [Configurar um ambiente de desenvolvimento local para o AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=pt-BR)

## Personalizar um componente principal adaptável do Forms

Siga as etapas abaixo para modificar a aparência, o comportamento e a funcionalidade de um Componente principal adaptável do Forms.

1. **Identificar e duplicar o Componente principal**

   Ao configurar o ambiente de desenvolvimento, você criou um projeto baseado em Arquétipo. No Projeto do arquétipo AEM, identifique o Componente principal específico que deseja personalizar. Depois de identificado, crie uma duplicata do componente no projeto com base no Arquétipo AEM. Mantenha-o em paralelo a outros componentes principais adaptáveis do Forms. Essa etapa garante que seus esforços de personalização não afetem o componente original, permitindo que você experimente livremente.

1. **Personalizar o componente copiado**

   Abra o componente duplicado e comece a fazer as modificações necessárias de acordo com suas necessidades:

   * **Personalizar estrutura de HTML**: adapte a estrutura de HTML para atender às suas necessidades de design, respeitando [BEM (Modificador de elemento de bloco)](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) práticas de estilo para código mantido e escalável.
   * **Atualizar rótulo**: atualize o rótulo do componente para fornecer um nome claro e descritivo para a versão personalizada. Consulte as [Modelo de rótulo OOTB (pronto para uso)](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html) por questões de coerência.
   * **Personalizar widget**: ajuste o widget usado no componente (listas suspensas, caixas de seleção) para alinhar-se ao seu caso de uso específico. Veja, o [exemplo de implementação de widget](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html) para referência.
   * **Texto de ajuda e dicas**: personalize o texto de ajuda ou as dicas de ferramentas associadas ao componente para oferecer contexto e orientação aos usuários. Use o [Modelo de texto de ajuda OOTB](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html) como ponto de partida.
   * **Atributos de dados**: incorpore todos os atributos de dados necessários nos elementos HTML do componente. Esses atributos são cruciais para o funcionamento adequado do componente no tempo de execução. Consulte o [documentação](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput) para entender a função dos atributos de dados nos Componentes principais do Forms adaptável.

1. **Implementar a lógica de back-end**

   Se sua personalização exigir lógica de backend, é possível estender modelos sling existentes. Consulte as [exemplo](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java) para integrar perfeitamente a funcionalidade desejada ao componente personalizado.

1. **Configurar a caixa de diálogo do componente**

   Configure a caixa de diálogo associada ao componente personalizado. Use o exemplo [caixa de diálogo componente](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml) fornecido na documentação para garantir que as interações e as configurações do usuário sejam gerenciadas adequadamente.

1. **Implante e teste o componente no seu ambiente de desenvolvimento local**

   Uso [maven para criar e implantar o componente](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html#building-and-installing) no ambiente de desenvolvimento local. Depois que o componente for implantado, crie um Formulário adaptável para testar o componente personalizado.

1. **Implante o componente personalizado no seu ambiente de produção**

   Depois de testar o componente no ambiente de desenvolvimento local, implante o componente nos ambientes de produção.

