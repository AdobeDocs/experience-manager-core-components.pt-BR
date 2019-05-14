---
title: Componente do contêiner de formulário
seo-title: Componente do contêiner de formulário
description: 'null'
seo-description: O componente do contêiner de formulário do componente principal permite a criação de formulários de envio simples.
uuid: 9 d 556 daf -3 fe 7-4 b 2 a-b 5 ae -6926 acb 267 a 9
contentOwner: Usuário
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 3 d 33 fe 60-a 0 ac -4 ff 2-a 865-d 600 b 5448 aeb
disttype: dist5
gnavtheme: light
groupsectionnavitems: não
hidemerchandisingbar: herdar
hidepromocomponent: herdar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 62643e5bd49ab006230f65004bb9374822dcc017

---


# Componente do contêiner de formulário{#form-container-component}

O componente do contêiner de formulário do componente principal permite a criação de formulários de envio simples.

## Uso {#usage}

O componente do contêiner de formulário permite a criação de formulários e recursos de envio de informações simples com suporte a formulários WCM simples e a uma estrutura aninhada para permitir componentes de formulário adicionais.

Ao usar a caixa [de diálogo](#configure-dialog) Configurar, o editor de conteúdo pode definir a ação acionada pelo envio do formulário, onde o conteúdo enviado deve ser armazenado e se um fluxo de trabalho deve ser acionado. O autor do modelo pode usar a [caixa de diálogo](#design-dialog) de design para definir os componentes permitidos e seus mapeamentos similares à caixa de diálogo de design do contêiner de layout [padrão no editor de modelo](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html).

>[!NOTE]
>
>Os componentes principais do Contêiner de contêiner de formulários são compatíveis apenas com o uso dos componentes do formulário principais componentes (botão, texto, oculto etc.). Não [há suporte para o uso de componentes](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) de formulário de componentes de base no contêiner de formulário de componentes principais (e vice-versa).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do contêiner de formulário é v 2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatível | Compatível | Compatível |
| [v1](form-container-v1.md) | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do contêiner de formulário [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo defina quais ações são executadas quando o componente é enviado.

![](assets/screen_shot_2018-01-12at122046.png)

Dependendo do Tipo **de ação selecionado**, as opções disponíveis no contêiner serão alteradas. Os tipos de ação disponíveis são:

* [Email](#mail)
* [Armazenar conteúdo](#store-content)
* [Enviar pedido](#submit-order)
* [Atualizar pedido](#update-order)

Independentemente do tipo, há configurações [gerais](#general-settings) que se aplicam a cada ação.

### Email {#mail}

Quando o formulário é enviado, o tipo de ação de email enviará um email para os destinatários designados.

![](assets/screen_shot_2018-01-12at122554.png)

* **Assunto**
do assunto do email que será enviado no envio do formulário
* **A partir**
do endereço de email do email que será enviado no envio do formulário
* **Para**
os endereços dos destinatários que receberão um email após o envio do formulário

   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais.
   * Toque ou clique no **botão Excluir** para remover um endereço de e-mail
* **CC**
Os endereços dos destinatários que receberão uma cópia de carbono o e-mail enviado após o envio do formulário
   * Toque ou clique no botão **Adicionar** para adicionar endereços adicionais.
   * Toque ou clique no **botão Excluir** para remover um endereço de e-mail

### Armazenar conteúdo {#store-content}

Quando o formulário é enviado, o conteúdo do formulário será armazenado em um local de repositório designado.

![](assets/screen_shot_2018-01-12at122538.png)

* **Caminho de repositório**de conteúdo do caminho
de conteúdo onde o conteúdo enviado é armazenado
* **Exibir**toque de dados
ou clicar para exibir dados enviados armazenados como JSON
* **Iniciar fluxo de trabalho**
Configurar para iniciar um fluxo de trabalho com o conteúdo armazenado como carga na submissão do formulário

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
* Deixe em branco para exibir novamente o formulário após o envio.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os componentes permitidos e seus mapeamentos para o contêiner semelhante à caixa de diálogo de design do contêiner de layout [padrão no editor de modelo](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html).