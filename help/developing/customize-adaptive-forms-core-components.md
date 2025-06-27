---
title: Personalizar componentes principais dos formulários adaptáveis
description: Saiba como estender ou criar um componente principal para formulários adaptáveis e implementar funcionalidades personalizadas na sua organização.
role: Architect, Developer, Admin
exl-id: f3ab12aa-d48d-47e9-a965-15052cac6f18
source-git-commit: 5994133947ff697f7c866fe61598c58e37e77008
workflow-type: ht
source-wordcount: '562'
ht-degree: 100%

---

# Personalizar componentes principais dos formulários adaptáveis

Personalizar os componentes principais dos formulários adaptáveis permite adaptar as funcionalidades prontas para uso para que atendam a necessidades específicas. Este guia orienta você pelo processo de personalização desses componentes, a fim de criar uma experiência mais individual.

{{traditional-aem}}

## Pré-requisito

Antes de começar a personalizar os componentes principais dos formulários adaptáveis,

* Saiba mais sobre a [arquitetura de um componente principal](customizing.md#customizing-the-markup-customizing-the-markup) e consulte a [documentação oficial dos Componentes principais do Adobe Experience Manager](customizing.md). Esses recursos abrangentes servem como guia durante todo o processo de personalização.
* Configure o ambiente de desenvolvimento para garantir um fluxo de trabalho tranquilo para fazer alterações nos componentes principais. Ao configurar o ambiente de desenvolvimento, use um arquétipo de projeto do AEM com base no arquétipo mais recente do AEM. Com base em seu ambiente, você pode:

   * [Configurar um ambiente de desenvolvimento local para o Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html?lang=pt-BR).
   * [Configurar um ambiente de desenvolvimento local para o AEM Forms 6.5](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=pt-BR)

## Personalizar um componente principal dos formulários adaptáveis

Siga as etapas abaixo para modificar a aparência, o comportamento e a funcionalidade de um componente principal dos formulários adaptáveis.

1. **Identificar e duplicar o componente principal**

   Ao configurar o ambiente de desenvolvimento, você criou um projeto com base em um arquétipo. No projeto de arquétipo do AEM, identifique o componente principal específico que deseja personalizar. Depois de identificá-lo, crie uma duplicata do componente no projeto de arquétipo do AEM. Mantenha-o em paralelo a outros componentes principais de formulários adaptáveis. Essa etapa garante que seus esforços de personalização não afetem o componente original, permitindo uma livre experimentação.

1. **Personalizar o componente copiado**

   Abra o componente duplicado e comece a fazer as modificações necessárias de acordo com suas necessidades:

   * **Personalizar estrutura HTML**: adapte a estrutura HTML para atender às suas necessidades de design, respeitando as práticas de estilo do [BEM (Modificador de elemento de bloco)](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) para códigos com capacidade de manutenção e expansão.
   * **Atualizar rótulo**: atualize o rótulo do componente para fornecer um nome claro e descritivo para a versão personalizada. Consulte o [Modelo de rótulo OOTB (pronto para uso)](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html?lang=pt-BR) fornecido para obter consistência.
   * **Personalizar widget**: ajuste o widget usado no componente (listas suspensas, caixas de seleção) para alinhar-se ao seu caso de uso específico. Consulte o [exemplo de implementação de widget](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html?lang=pt-BR) para referência.
   * **Texto de ajuda e dicas de ferramentas**: personalize o texto de ajuda ou as dicas de ferramentas associadas ao componente para oferecer contexto e orientação aos usuários. Use o [Modelo de texto de ajuda OOTB](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html?lang=pt-BR) como ponto de partida.
   * **Atributos de dados**: incorpore todos os atributos de dados necessários nos elementos HTML do componente. Esses atributos são cruciais para o funcionamento adequado do componente no tempo de execução. Consulte a [documentação](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput) para entender a função dos atributos de dados nos componentes principais dos formulários adaptáveis.

1. **Implementar a lógica de back-end**

   Se sua personalização exigir uma lógica de back-end, é possível estender modelos do Sling existentes. Consulte o [exemplo](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java) fornecido para integrar de forma simples a funcionalidade desejada ao componente personalizado.

1. **Configurar a caixa de diálogo do componente**

   Configure a caixa de diálogo associada ao componente personalizado. Use a [caixa de diálogo de componente](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml) de exemplo fornecida na documentação para garantir que as interações e configurações do usuário sejam gerenciadas adequadamente.

1. **Implante e teste o componente no seu ambiente de desenvolvimento local**

   Use o [Maven para criar e implantar o componente](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html?lang=pt-BR#building-and-installing) no ambiente de desenvolvimento local. Depois que o componente for implantado, crie um formulário adaptável para testar o componente personalizado.

1. **Implante o componente personalizado no ambiente de produção**

   Depois de testar o componente no ambiente de desenvolvimento local, implante-o nos ambientes de produção.
