---
title: Componente de página de e-mail
description: O componente de página de e-mail
role: Architect, Developer, Admin, User
exl-id: 17fd0f5e-2b85-41a1-abaf-8ad190a5341a
source-git-commit: c16dd8696e89f89c7b178ece11f57a565d73588b
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 100%

---


# Componente de página de e-mail {#email-page-component}

O componente de página de e-mail é um componente de página extensível projetado para funcionar com o [editor de modelos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR). Ele permite que o cabeçalho/rodapé da página e os componentes da estrutura sejam organizados com o editor de modelo e ajustados para criação de conteúdo do Adobe Campaign.

## Uso {#usage}

O componente de página de e-mail forma a base de todas as páginas criadas com os componentes principais de e-mail e modelos editáveis. Ao utilizar o componente de página de e-mail, os cabeçalhos, rodapés e a estrutura da página podem ser definidos como um modelo utilizando os outros componentes principais de e-mail.

* Usando a [caixa de diálogo de design](#design-dialog), as bibliotecas personalizadas do lado do cliente podem ser definidas para a página.
* Ao contrário de outros componentes que têm uma caixa de diálogo de edição acessível diretamente do componente, o componente de página de e-mail é a própria página. Portanto, a [caixa de diálogo de edição](#edit-dialog) do componente de página de e-mail é a janela de propriedades da página.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de página de e-mail é a v1, introduzida com o lançamento X dos componentes principais de e-mail em outubro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | - |

Para mais informações sobre as versões e lançamentos do componente principal de e-mail, consulte o documento [Versões dos componentes principais de e-mail](/help/email/versions.md)

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de página [pode ser encontrada no GitHub.](https://adobe.com/go/aem_cmp_tech_email_page_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

Como o componente representa a página inteira, as configurações que normalmente estariam em uma caixa de diálogo de edição são encontradas na janela [Propriedades da página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=pt-BR).

### Guia do Serviços na nuvem {#cloud-services}

Para que os componentes principais de e-mail possam recuperar dados e variáveis de campanha, a página deve estar vinculada a uma configuração do Adobe Campaign.

![Propriedades da página de e-mail](/help/email/assets/email-page-properties.png)

No cabeçalho **Configurações do serviço de nuvem**, selecione **Adicionar configuração** no menu suspenso.

No cabeçalho **Adobe Campaign**, selecione a configuração da sua integração com o Adobe Campaign.

Consulte o documento [Utilizando os componentes principais de e-mail](/help/email/using.md) para obter mais informações sobre como configurar os componentes principais de e-mail.

### Guia E-mail {#email-tab}

A guia E-mail define as propriedades dos e-mails enviados pelo Adobe Campaign com base no conteúdo dessa página, como o assunto do e-mail e o conteúdo de texto sem formatação.

![Propriedades da página de e-mail](/help/email/assets/email-page-properties-email.png)

* **Assunto** - O assunto do e-mail enviado pelo Adobe Campaign com base nessa página
   * Clique no ícone **Selecionar variável do Adobe Campaign** e abra a caixa de diálogo [Selecionar variável do Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Pré-cabeçalho**
   * Clique no ícone **Selecionar variável do Adobe Campaign** e abra a caixa de diálogo [Selecionar variável do Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Texto sem formatação** - A versão em texto sem formatação do e-mail enviado pelo Adobe Campaign
   * Clique no ícone **Selecionar variável do Adobe Campaign** e abra a caixa de diálogo [Selecionar variável do Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **URL de referência**

## Caixa de diálogo de design {#design-dialog}

Como o componente representa a página inteira, a caixa de diálogo de design é acessada por meio de **Informações da página -> Política da página** ao editar o modelo da página.

![Política da página](/help/assets/page-policy.png)

### Guia Propriedades {#properties-tab}

Usando a janela Design da página, você pode definir as bibliotecas de clientes a serem carregadas, bem como a biblioteca de recursos da Web para a página.

![Caixa de diálogo de design do componente de página de e-mail](/help/email/assets/email-page-design.png)

* **Bibliotecas do cliente** - Isso define as categorias das bibliotecas de clientes a serem carregadas. O JavaScript é adicionado na extremidade do corpo e o CSS é adicionado ao cabeçalho da página.
* **Cabeçalho da página do JavaScript das bibliotecas do cliente** - Isto define as categorias da biblioteca JavaScript do cliente que serão carregadas no cabeçalho da página.
   * As categorias definidas aqui que também estão presentes no campo **Bibliotecas do cliente** terão o JavaScript carregado no cabeçalho da página em vez de no final do corpo.
   * Nenhum CSS será carregado, a menos que a categoria também esteja presente no campo **Bibliotecas do cliente**.
* **Carregar bibliotecas JavaScript de forma assíncrona** - Se habilitado, as bibliotecas JavaScript personalizadas serão carregadas de forma assíncrona.
* **Biblioteca cliente de recursos na Web** - A categoria de bibliotecas de clientes usada para servir recursos da Web, como favicons.
* **Ir para o conteúdo principal - seletor de elemento** - Usado como um recurso de acessibilidade para ignorar diretamente o conteúdo principal da página.

As bibliotecas podem ser configuradas para os campos **Bibliotecas do cliente** e **Cabeçalho da página do JavaScript das bibliotecas do cliente** da seguinte maneira:

* Para adicionar um novo campo, clique ou toque no botão **Adicionar** abaixo dos campos.
* Para remover um campo, clique ou toque no ícone da lixeira próximo do campo a ser removido.
* Para reorganizar a ordem de carregamento, clique ou toque e arraste a alça ao lado do campo a ser movido.

Para mais informações sobre o uso de bibliotecas do lado do cliente, consulte [Utilizando bibliotecas do lado do cliente.](https://helpx.adobe.com/br/experience-manager/6-5/sites/developing/using/clientlibs.html)

### Guia Estilos {#styles-tab}

O componente de Página é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
