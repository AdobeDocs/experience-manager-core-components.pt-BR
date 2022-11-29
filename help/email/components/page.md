---
title: Componente Página de email
description: O componente Página de email
role: Architect, Developer, Admin, User
exl-id: 17fd0f5e-2b85-41a1-abaf-8ad190a5341a
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 40%

---


# Componente Página de email {#email-page-component}

O Componente de página de email é um componente de página extensível projetado para funcionar com o [editor de modelos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR) e permite que o cabeçalho/rodapé da página e os componentes da estrutura sejam montados com o editor de modelo, personalizados para criar conteúdo do Adobe Campaign.

## Uso {#usage}

O componente Página de email forma a base de todas as páginas criadas com os Componentes principais de email e modelos editáveis. Ao usar o Componente de página de email, os cabeçalhos, rodapés e a estrutura da página podem ser definidos como um modelo usando os outros Componentes principais de email.

* Usar o [diálogo de design,](#design-dialog) bibliotecas personalizadas do lado do cliente podem ser definidas para a página.
* Diferente de outros componentes que têm uma caixa de diálogo de edição acessível diretamente do componente, pois o Componente de página de email é a própria página, a variável [caixa de diálogo editar](#edit-dialog) do Componente de página de email é a janela de propriedades da página.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de página de email é a v1, que foi introduzida com a versão X dos Componentes principais de email em outubro de 2022, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | Compatível |

Para obter mais informações sobre versões e versões do Componente principal de email, consulte o documento [Versões dos Componentes principais de email](/help/email/versions.md)

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Página [pode ser encontrada no GitHub.](https://adobe.com/go/aem_cmp_tech_email_page_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

Como o componente representa a página inteira, as configurações que normalmente estariam em uma caixa de diálogo de edição são encontradas na janela [Propriedades da página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=pt-BR).

### Guia Cloud Services {#cloud-services}

Para que os Componentes principais de email possam recuperar variáveis de campanha e dados, a página deve estar vinculada a uma configuração do Adobe Campaign.

![Propriedades da página de email](/help/email/assets/email-page-properties.png)

Em **Configuração Cloud Service** , na seleção suspensa **Adicionar configuração**.

Em **Adobe Campaign** , selecione a configuração da sua integração com o Adobe Campaign.

Consulte o documento [Usar componentes principais de email](/help/email/using.md) para obter mais informações sobre como configurar os Componentes principais de email.

### Guia Email {#email-tab}

A guia Email define as propriedades dos emails enviados pelo Adobe Campaign com base no conteúdo dessa página, como o assunto do email e o conteúdo de texto simples.

![Propriedades da página de email](/help/email/assets/email-page-properties-email.png)

* **Assunto** - O assunto do email enviado pelo Adobe Campaign com base nesta página
   * Clique no botão **Selecionar variável Adobe Campaign** ícone para abrir o [Selecionar variável Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Pré-cabeçalho**
   * Clique no botão **Selecionar variável Adobe Campaign** ícone para abrir o [Selecionar variável Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Texto sem formatação** - A versão em texto simples do email enviado pelo Adobe Campaign
   * Clique no botão **Selecionar variável Adobe Campaign** ícone para abrir o [Selecionar variável Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.
* **Url De Referência**

## Caixa de diálogo de design {#design-dialog}

Como o componente representa a página inteira, a caixa de diálogo de design é acessada por meio de **Informações da página -> Política da página** ao editar o modelo da página.

![Política da página](/help/assets/page-policy.png)

### Guia Propriedades {#properties-tab}

Usando a janela Design da página, você pode definir as bibliotecas de clientes a serem carregadas, bem como a biblioteca de recursos da Web para a página.

![Caixa de diálogo Design do componente Página de email](/help/email/assets/email-page-design.png)

* **Bibliotecas do cliente** - Isso define as categorias das bibliotecas de clientes a serem carregadas. O JavaScript é adicionado na extremidade do corpo e o CSS é adicionado ao cabeçalho da página.
* **Cabeçalho da página JavaScript de bibliotecas de clientes** - Isso define as categorias da biblioteca do cliente JavaScript a serem carregadas no cabeçalho da página.
   * As categorias definidas aqui que também estão presentes no campo **Bibliotecas do cliente** terão o JavaScript carregado no cabeçalho da página em vez de no final do corpo.
   * Nenhum CSS será carregado, a menos que a categoria também esteja presente no campo **Bibliotecas do cliente**.
* **Carregar bibliotecas JavaScript de forma assíncrona** - Se estiver habilitado, as bibliotecas JavaScript personalizadas serão carregadas de forma assíncrona.
* **Biblioteca cliente de recursos da Web** - A categoria de bibliotecas de clientes usada para servir recursos da Web, como favicons.
* **Ir para o conteúdo principal - seletor de elemento** - Usado como um recurso de acessibilidade para ignorar diretamente o conteúdo principal da página.

As bibliotecas podem ser configuradas para os campos **Bibliotecas do cliente** e **Cabeçalho da página JavaScript de bibliotecas do cliente** da seguinte maneira:

* Para adicionar um novo campo, clique ou toque no botão **Adicionar** abaixo dos campos.
* Para remover um campo, clique ou toque no ícone da lixeira ao lado do campo a ser removido.
* Para reorganizar a ordem de carregamento, clique ou toque e arraste a alça ao lado do campo a ser movido.

Para obter mais informações sobre o uso de bibliotecas do lado do cliente, consulte [Usar bibliotecas do lado do cliente.](https://helpx.adobe.com/br/experience-manager/6-5/sites/developing/using/clientlibs.html)

### Guia Estilos {#styles-tab}

O componente de Página é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
