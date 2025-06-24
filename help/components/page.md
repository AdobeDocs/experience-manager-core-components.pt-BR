---
title: Componente de Página
description: O componente de Página é um componente de página extensível projetado para funcionar com o editor de modelo e permitir que o cabeçalho/rodapé da página e os componentes da estrutura sejam montados com o editor de modelo.
role: Architect, Developer, Admin, User
exl-id: 2503e067-abed-427d-8a54-8b79e3451487
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 100%

---


# Componente de Página {#page-component}

O componente de Página é um componente de página extensível projetado para funcionar com o [editor de modelo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR). Ele permite que o cabeçalho/rodapé da página e os componentes da estrutura sejam montados com o editor de modelo.

{{traditional-aem}}

## Uso {#usage}

O componente de Página é a base de todas as páginas criadas com os Componentes principais e os modelos editáveis. Ao usar o componente de Página, os cabeçalhos, rodapés e a estrutura da página podem ser definidos como um modelo usando os outros Componentes principais.

Usando a [caixa de diálogo design](#design-dialog), as bibliotecas personalizadas do lado do cliente podem ser definidas para a página. Ao contrário de outros componentes que têm uma caixa de diálogo de edição acessível diretamente do componente, como o componente de Página é a própria página, a [caixa de diálogo de edição](#edit-dialog) do componente de Página é a janela de propriedades da página.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de página é a v3, introduzida com a versão 2.18.0 dos componentes principais em fevereiro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v3 | - | Compatível | Compatível | Compatível |
| [v2](v2/page.md) | Compatível | Compatível | - | Compatível |
| [v1](v1/page-v1.md) | Compatível | Compatível | - | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Compatível com o Aplicativo web progressivo {#pwa-support}

A versão 2.15.0 dos Componentes principais introduziu o suporte para recursos integrados de [Aplicativos web progressivos (PWA) do AEM as a Cloud Service.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html?lang=pt-BR) Com uma configuração simples no nível do site, transforme sua experiência AEM em um PWA!

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Página [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_page_v3_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

Como o componente representa a página inteira, as configurações que normalmente estariam em uma caixa de diálogo de edição são encontradas na janela [Propriedades da página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=pt-BR).

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

* **Biblioteca cliente de recursos da Web** - A categoria de bibliotecas de clientes usada para servir recursos da Web, como favicons.

* **Ir para o conteúdo principal - seletor de elemento** - Usado como um recurso de acessibilidade para ignorar diretamente o conteúdo principal da página.

* **Renderizar links de idiomas alternativos** - Se habilitada, os links para versões de idiomas alternativos da página no mesmo site serão adicionados ao cabeçalho da página.

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
