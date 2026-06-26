---
title: Componente de página (v2)
description: O componente de página é um componente de página extensível projetado para funcionar com o editor de modelo e permitir que o cabeçalho/rodapé da página e os componentes da estrutura sejam montados com o editor de modelo.
role: Developer, Admin, User
exl-id: e85fe4db-6de4-4a84-a54c-bd07a67efed3
index: false
TQID: https://experienceleague.adobe.com/p1V-3XLpA6H-rC-zWIYFqbPkd6HW7bBLWFXaj8aeNAs
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
subfeature_v2: id: f86a5563-8f73-4ec0-be7d-a1782604870a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2a9a69dd7eeade8cdc2f681a354350c4370d5d1b
workflow-type: tm+mt
source-wordcount: 753
ht-degree: 88%

---

# Componente de página (v2) {#page-component}

O componente de Página é um componente de página extensível projetado para funcionar com o [editor de modelo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR). Ele permite que o cabeçalho/rodapé da página e os componentes da estrutura sejam montados com o editor de modelo.

## Uso {#usage}

O componente de Página é a base de todas as páginas criadas com os Componentes principais e os modelos editáveis. Ao usar o componente de Página, os cabeçalhos, rodapés e a estrutura da página podem ser definidos como um modelo usando os outros Componentes principais.

Usando a [caixa de diálogo design](#design-dialog), as bibliotecas personalizadas do lado do cliente podem ser definidas para a página. Ao contrário de outros componentes que têm uma caixa de diálogo de edição acessível diretamente do componente, como o componente de Página é a própria página, a [caixa de diálogo de edição](#edit-dialog) do componente de Página é a janela de propriedades da página.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a versão v2 do componente de página, que foi introduzida com a versão 2.0.0 dos componentes principais em janeiro de 2018.

>[!CAUTION]
>
>Este documento descreve a versão v2 do componente de página.
>
>Para obter detalhes sobre a versão atual do componente de página, consulte o documento [Componente de página](/help/components/page.md).

## Compatível com o Aplicativo web progressivo {#pwa-support}

A versão 2.15.0 dos componentes principais introduziu suporte para os [recursos integrados de Aplicativos Web Progressivos (PWA).](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html?lang=pt-BR)do AEM as a Cloud Service. Com uma configuração simples no nível do site, transforme sua experiência com o AEM em um PWA.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Página [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_page_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

Como o componente representa a página inteira, as configurações que normalmente estariam em uma caixa de diálogo de edição são encontradas na janela [Propriedades da página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=pt-BR).

### Suporte a dados estruturados {#structured-data}

A [Versão 2.31.0](/help/versions.md) dos Componentes Principais introduziu o suporte a Dados Estruturados em nível de página (JSON-LD) dos tipos [schema.org](https://schema.org) para todas as versões do Componente de Página.  O AEM renderiza esses blocos no lado do servidor no cabeçalho da página.

A [Versão 2026.6.0 do AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap) adicionou a capacidade de os autores usarem a janela Propriedades da Página para adicionar um ou mais blocos JSON-LD a uma página na seção **SEO** da guia **Avançado**.

## Caixa de diálogo de design {#design-dialog}

Como o componente representa a página inteira, a caixa de diálogo de design é acessada por meio de **Informações da página -> Política da página** ao editar o modelo da página.

![Política da página](/help/assets/page-policy.png)

>[!NOTE]
>
>Em versões anteriores do AEM, a **Política de página** era chamada de **Design de página**.

### Guia Propriedades {#properties-tab}

Usando a janela Design da página, você pode definir as bibliotecas de clientes a serem carregadas, bem como a biblioteca de recursos da Web para a página.

* **Bibliotecas do cliente** - Isso define as categorias das bibliotecas de clientes a serem carregadas. O JavaScript é adicionado na extremidade do corpo e o CSS é adicionado ao cabeçalho da página.
* **Cabeçalho da página JavaScript de bibliotecas do cliente** - Isso define as categorias da biblioteca do cliente JavaScript a serem carregadas no cabeçalho da página.
   * As categorias definidas aqui que também estão presentes no campo **Bibliotecas do cliente** terão o JavaScript carregado no cabeçalho da página em vez de no final do corpo.
   * Nenhum CSS será carregado, a menos que a categoria também esteja presente no campo **Bibliotecas do cliente**.

* **Biblioteca cliente de recursos na Web** - A categoria de bibliotecas de clientes usada para servir recursos da Web, como favicons.

* **Ir para o conteúdo principal - seletor de elemento** - Usado como um recurso de acessibilidade para ignorar diretamente o conteúdo principal da página.

![Caixa de diálogo de design do componente de Página](/help/assets/page-design.png)

As bibliotecas podem ser configuradas para os campos **Bibliotecas do cliente** e **Cabeçalho da página JavaScript de bibliotecas do cliente** da seguinte maneira:

* Para adicionar um novo campo, clique ou toque no botão **Adicionar** abaixo dos campos.
* Para remover um campo, clique ou toque no ícone da lixeira ao lado do campo a ser removido.
* Para reorganizar a ordem de carregamento, clique ou toque e arraste a alça ao lado do campo a ser movido.

Para mais informações sobre o uso de bibliotecas do lado do cliente, consulte [Uso de bibliotecas do lado do cliente](https://helpx.adobe.com/br/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>A capacidade de definir bibliotecas de clientes separadamente para o cabeçalho da página foi introduzida com os Componentes principais versão 2.2.0.

### Guia Estilos {#styles-tab}

O componente de Página é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Página oferece suporte à [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
