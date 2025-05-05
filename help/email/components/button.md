---
title: Componente do Botão de email
description: O Componente do Botão de email permite a configuração e a exibição de um item de botão em seu conteúdo.
role: Architect, Developer, Admin, User
exl-id: b144e8d1-1097-475d-b2eb-3353c176afb9
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: ht
source-wordcount: '517'
ht-degree: 100%

---


# Componente do Botão de email {#email-button-component}

O Componente do Botão de email permite a configuração e a exibição de um item de botão em seu conteúdo.

## Uso {#usage}

O Componente do Botão de email permite a inclusão de um botão em seu conteúdo, clicável pelo reader de conteúdo, vinculado a recursos adicionais.

* As propriedades do botão podem ser selecionadas na [caixa de diálogo de configuração.](#configure-dialog)
* Os estilos do Componente de Botão de email podem ser definidos na [caixa de diálogo de design.](#design-dialog)

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de Botão de email é a v1, introduzida com a versão x dos Componentes Principais do email em outubro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | - | - |

Para mais informações sobre as versões e novidades dos componentes principais, consulte o documento [Versões dos Componentes principais de email.](/help/email/versions.md)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de Botão de email [pode ser encontrada no GitHub.](https://adobe.com/go/aem_cmp_tech_email_button_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o botão e como ele se comporta e é exibido para um leitor de seu conteúdo.

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do componente de Botão](/help/email/assets/email-button-edit-properties.png)

* **Texto** - O texto a ser exibido no botão
   * Clique no ícone Campaign para abrir o diálogo [Selecionar variável do Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Link** - Link para uma página de conteúdo no AEM, um recurso externo ou uma âncora
   * Use a **Caixa de diálogo de seleção** para escolher um caminho dentro do AEM.
   * Clique no ícone Campaign para abrir o diálogo [Selecionar variável do Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Ícone** - Identificador para exibir um ícone no botão
* **ID** - Esta opção permite controlar o identificador exclusivo do componente no HTML.
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração de ID pode afetar o CSS.
* **Abrir link em nova guia** - Se marcada, o link será aberto em uma nova guia do navegador.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade da caixa de diálogo de edição do componente de Botão](/help/email/assets/email-button-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

### Guia Estilos {#styles-tab-edit}

O Componente de Botão do email é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para este componente na [caixa de diálogo de design](#design-dialog) para que a guia fique disponível.

## Caixa de diálogo de design {#design-dialog}

### Guia Estilos {#styles-tab}

O Componente de Botão de email é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
