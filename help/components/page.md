---
title: Componente de página
description: O Componente de página é um componente de página extensível projetado para funcionar com o editor de modelo e permitir que o cabeçalho/rodapé da página e os componentes da estrutura sejam montados com o editor de modelo.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: fa8ead438093681071b6b6f8ccfbba523f6d3bee
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 3%

---


# Componente de página{#page-component}

O Componente de página é um componente de página extensível projetado para funcionar com o [editor de modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) e permite que o cabeçalho/rodapé da página e os componentes da estrutura sejam montados com o editor de modelo.

## Uso {#usage}

O Componente de página é a base de todas as páginas criadas com os Componentes principais, bem como modelos editáveis. Ao usar o Componente de página, os cabeçalhos, rodapés e a estrutura da página podem ser definidos como um modelo usando os outros Componentes principais.

Usando a caixa de diálogo [design](#design-dialog), as bibliotecas personalizadas do lado do cliente podem ser definidas para a página. Ao contrário de outros componentes que têm uma caixa de diálogo de edição acessível diretamente do componente, porque o Componente de página é a própria página, a [caixa de diálogo de edição](#edit-dialog) do Componente de página é a janela de propriedades da página.

## Suporte Progressivo a Aplicações Web {#pwa-support}

A versão 2.15.0 dos Componentes principais introduziu o suporte para o AEM as a Cloud Service incorporado [Progressive Web Apps (PWA).](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html) Com uma configuração simples no nível do site, transforme sua experiência de AEM em um PWA!

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de página é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | Compatível | Compatível | Compatível |
| [v1](v1/page-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de página [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_page_v2).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Editar Caixa de Diálogo {#edit-dialog}

Como o componente representa a página inteira, as configurações que normalmente estariam em uma caixa de diálogo de edição são encontradas na janela [Propriedades da página](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Caixa de diálogo Design {#design-dialog}

Como o componente representa a página inteira, a caixa de diálogo de design é acessada por **Informações da página -> Política da página** ao editar o modelo da página.

![Política da página](/help/assets/page-policy.png)

>[!NOTE]
>
>Em versões anteriores do AEM, a **Política de página** era chamada de **Design de página**.

### Guia Propriedades {#properties-tab}

Usando a janela Design da página, você pode definir as bibliotecas de clientes a serem carregadas, bem como a biblioteca de recursos da Web para a página.

* **Bibliotecas do cliente**  - Isso define as categorias da biblioteca do cliente a serem carregadas. O JavaScript é adicionado na extremidade do corpo e o CSS é adicionado ao cabeçalho da página.
* **Cabeçalho da página JavaScript de bibliotecas de clientes**  - Isso define as categorias da biblioteca do cliente JavaScript a serem carregadas no cabeçalho da página.
   * As categorias definidas aqui que também estão presentes no campo **Bibliotecas do cliente** terão o JavaScript carregado no cabeçalho da página em vez de no final do corpo.
   * Nenhum CSS será carregado, a menos que a categoria também esteja presente no campo **Bibliotecas do cliente**.

* **Biblioteca de clientes de recursos da Web**  - A categoria da biblioteca do cliente usada para fornecer recursos da Web, como favicons.

* **Pular para o seletor do elemento de conteúdo principal**  - Usado como um recurso de acessibilidade para ignorar diretamente o conteúdo principal da página

![Caixa de diálogo Design do componente de página](/help/assets/page-design.png)

As bibliotecas podem ser configuradas para os campos **Client Library** e **Client Library JavaScript Page Head** da seguinte maneira:

* Para adicionar um novo campo, clique ou toque no botão **Add** abaixo dos campos.
* Para remover um campo, clique ou toque no ícone da lixeira ao lado do campo a ser removido.
* Para reorganizar a ordem de carregamento, clique ou toque e arraste a alça ao lado do campo a ser movido.

Para obter mais informações sobre o uso de bibliotecas do lado do cliente, consulte [Usar bibliotecas do lado do cliente](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>A capacidade de definir bibliotecas de clientes separadamente para o cabeçalho da página foi introduzida com os componentes principais versão 2.2.0.

### Guia Estilos {#styles-tab}

O Componente de página suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

## Camada de dados do cliente Adobe {#data-layer}

O Componente de página oferece suporte à Camada de Dados do Cliente do Adobe.](/help/developing/data-layer/overview.md)[
