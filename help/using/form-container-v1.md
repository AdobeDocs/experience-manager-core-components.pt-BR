---
title: Componente do contêiner de formulário (v 1)
seo-title: Componente do contêiner de formulário (v 1)
description: O componente do contêiner de formulário do componente principal permite a criação de formulários de envio simples.
seo-description: O componente do contêiner de formulário do componente principal permite a criação de formulários de envio simples.
uuid: 075 d 83 ed-de 40-414 e-a 18 f -46 b 3 a 857 acba
content-type: referência
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 800 c 064 e -2 ad 5-41 f 3-9 cef-b 025 a 555 efd 9
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Componente do contêiner de formulário (v 1){#form-container-component-v}

O componente do contêiner de formulário do componente principal permite a criação de formulários de envio simples.

## Uso {#usage}

O Componente do contêiner de formulários ativou a criação de formulários e recursos de envio de informações simples, compatíveis com formulários WCM simples e com uma estrutura aninhada para permitir componentes de formulário adicionais.

Ao usar a [caixa de diálogo](form-container-v1.md#main-pars_title) de configuração, o editor de conteúdo pode definir o tipo de acionador de envio de formulário de ação, no qual o conteúdo enviado deve ser armazenado e se um fluxo de trabalho deve ser acionado. O autor do modelo pode usar a [caixa de diálogo](form-container-v1.md#main-pars_title_1995166862) de design para definir os componentes permitidos e seus mapeamentos similares à caixa de diálogo de design do contêiner de layout [padrão no editor de modelo](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve v 1 do Componente do contêiner de formulário originalmente introduzido com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v 1 do Componente do contêiner de formulário.

| Versão do AEM | Componente do contêiner de formulário v 1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve v 1 do componente do contêiner de formulário.
>
>Para obter detalhes sobre a versão atual do Componente do contêiner de formulário, consulte o [documento Componente](form-container.md) do contêiner de formulário.

## Caixa de diálogo Configurações {#settings-dialog}

A caixa de diálogo de configurações permite que o autor do conteúdo defina quais ações são executadas quando o componente é enviado.

![](assets/chlimage_1.png)

Dependendo do Tipo **de ação selecionado**, as opções disponíveis no contêiner serão alteradas. Os tipos de ação disponíveis são:

* [Email](form-container-v1.md#main-pars_title_966511656)
* [Armazenar conteúdo](form-container-v1.md#main-pars_title_2065985840)
* [Enviar pedido](form-container-v1.md#main-pars_title_686874527)
* [Atualizar pedido](form-container-v1.md#main-pars_title_410109286)

Independentemente do tipo, há configurações [gerais](form-container-v1.md#main-pars_title_375403046) que se aplicam a cada ação.

### Email {#mail}

Quando o formulário é enviado, o tipo de ação de email enviará um email para os destinatários designados.

![](assets/chlimage_1-1.png)

* **Assunto** - O assunto do email que será enviado no envio do formulário
* **De** - O endereço de email do email que será enviado no envio do formulário
* **Como** - Os endereços dos destinatários que receberão um email após o envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais.
   * Toque ou clique no **botão Excluir** para remover um endereço de e-mail
* **CC** - Os endereços dos destinatários que receberão uma cópia de carbono no e-mail enviado após o envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais.
   * Toque ou clique no **botão Excluir** para remover um endereço de e-mail

### Armazenar conteúdo {#store-content}

Quando o formulário é enviado, o conteúdo do formulário será armazenado em um local de repositório designado.

![](assets/chlimage_1-2.png)

* **Caminho do conteúdo** - Caminho de repositório de conteúdo onde o conteúdo enviado é armazenado
* **Exibir dados** - toque ou clique para exibir dados enviados armazenados como JSON
* **Iniciar fluxo de trabalho** - Configurar para iniciar um fluxo de trabalho com o conteúdo armazenado como carga na submissão do formulário

### Enviar pedido {#submit-order}

Quando o formulário é enviado, a ordem será enviada.

![](assets/chlimage_1-3.png)

### Atualizar pedido {#update-order}

Quando o formulário é enviado, a ordem será atualizada.

![](assets/chlimage_1-4.png)

### Configurações gerais {#general-settings}

Independentemente do tipo de ação selecionado, uma página de agradecimento pode ser sempre definida.

![](assets/chlimage_1-5.png)

O usuário será redirecionado para a página especificada após a conclusão do envio do formulário.

* Use a caixa de diálogo de seleção para selecionar um recurso no AEM.
* Se a página de agradecimento não estiver no AEM, especifique o URL absoluto. Urls não absolutos serão interpretados em relação ao AEM.
* Deixe em branco para reexibir o formulário após o envio.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os componentes permitidos e seus mapeamentos para o contêiner semelhante à caixa de diálogo de design do contêiner de layout [padrão no editor de modelo](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do contêiner de formulário [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

Todo o projeto de componentes principais pode ser baixado de github.

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).
