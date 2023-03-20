---
title: Componente principal adaptável do Forms - Texto
description: Uso ou personalização do Componente principal de texto adaptável do Forms.
role: Architect, Developer, Admin, User
exl-id: b8de68e4-ca0d-4ae5-9a04-104cc617f1be
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 3%

---

# Texto {#text-adaptive-forms-core-component}

Em um formulário adaptável, o texto se refere ao conteúdo exibido no formulário para o usuário ler. Isso pode incluir o texto usado para rotular um grupo de elementos de formulário, como campos de texto, bem como quaisquer instruções ou informações adicionais fornecidas ao usuário.

Isso também pode ajudar a dividir a estrutura de um formulário em seções lógicas, tornando mais fácil para os usuários compreender e preencher o formulário. Além disso, ele pode ser usado para fins de acessibilidade para fornecer uma breve descrição do elemento ao qual está associado. Normalmente, esse campo de texto é exibido próximo aos componentes do formulário, como antes ou depois dele.

**Exemplo**

![](/help/adaptive-forms/assets/text.png)

## Uso {#reasons-to-use-text-label}

Há vários motivos para usar o texto em um formulário:

* **Fornecer instruções**: O texto pode ser usado para fornecer instruções sobre como preencher o formulário ou quais informações são necessárias.

* **Fornecer contexto**: O texto pode ser usado para fornecer contexto para o formulário, como explicar a finalidade do formulário ou a organização que coleta as informações.

* **Divida o formulário em seções lógicas**: O texto pode ser usado para dividir um formulário em seções lógicas, tornando mais fácil para os usuários compreender e preencher o formulário.

* **Identidade e identidade da marca**: O texto pode ser usado para fins de identidade e identidade, como incluir o nome da organização no formulário.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal Adaptive Forms Accordion foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, AEM compatibilidade e links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível  com<br>[versão 2.0.4](/help/adaptive-forms/version.md) e posterior | Compatível com<br>[versão 1.1.12](/help/adaptive-forms/version.md) e posterior, mas inferior a 2.0.0. |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/adaptive-forms/version.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as últimas informações sobre o Componente principal de texto adaptável do Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/text/v1/text). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de texto para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de texto com facilidade para uma experiência do usuário contínua.

![Guia Básica](/help/adaptive-forms/assets/text_properties.png)

* **Nome** - É possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não deve conter espaços ou caracteres especiais.

* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.
* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Somente leitura** - Selecione a opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.


## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente Texto.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar estilos de CSS de um componente. O Componente principal de texto adaptável do Forms é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Caixa de diálogo de design](/help/adaptive-forms/assets/reset_designdialog.png)

* **Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal de texto adaptável do Forms.

* **Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.
