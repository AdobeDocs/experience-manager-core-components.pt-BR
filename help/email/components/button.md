---
title: Componente do botão de email
description: O componente Botão de email permite a configuração e a exibição de um item de botão no seu conteúdo.
role: Architect, Developer, Admin, User
exl-id: b144e8d1-1097-475d-b2eb-3353c176afb9
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 43%

---


# Componente do botão de email {#email-button-component}

O componente Botão de email permite a configuração e a exibição de um item de botão no seu conteúdo.

## Uso {#usage}

O componente Botão de email permite a inclusão de um botão no seu conteúdo, clicável pelo leitor de conteúdo, vinculado a recursos adicionais.

* As propriedades do botão podem ser selecionadas na [caixa de diálogo de configuração.](#configure-dialog)
* Os estilos do componente Botão de email podem ser definidos na variável [caixa de diálogo de design.](#design-dialog)

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do botão de email é a v1, que foi introduzida com a versão x dos Componentes principais de email em outubro de 2022, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos Componentes principais de email.](/help/email/versions.md)

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente do botão de email, bem como ver exemplos de suas opções de configuração, bem como a saída do HTML e JSON, visite o [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_email_button)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do botão de email [pode ser encontrado no GitHub.](https://adobe.com/go/aem_cmp_tech_email_button_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o botão e como ele se comporta e é exibido para um leitor de seu conteúdo.

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do componente de Botão](/help/email/assets/email-button-edit-properties.png)

* **Texto** - O texto a ser exibido no botão
   * Clique no ícone Campanha para abrir o [Selecionar variável Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Link** - Link para uma página de conteúdo no AEM, um recurso externo ou uma âncora
   * Use a **Caixa de diálogo de seleção** para escolher um caminho dentro do AEM.
   * Clique no ícone Campanha para abrir o [Selecionar variável Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Ícone** - Identificador para exibir um ícone no botão
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML.
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração da ID pode afetar o CSS.
* **Abrir link em nova guia** - Se marcada, o link será aberto em uma nova guia do navegador.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade da caixa de diálogo de edição do componente de Botão](/help/email/assets/email-button-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

### Guia Estilos {#styles-tab-edit}

O componente Botão de email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling).

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que a guia esteja disponível.

## Caixa de diálogo de design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente Botão de email é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).
