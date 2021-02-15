---
title: Componente da página
description: O Componente de página é um componente de página extensível projetado para trabalhar com o editor de modelo e permitir que os componentes de cabeçalho/rodapé e estrutura da página sejam montados com o editor de modelo.
translation-type: tm+mt
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 2%

---


# Componente de página{#page-component}

O Componente de página é um componente de página extensível projetado para funcionar com o [editor de modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) e permite que os componentes de cabeçalho/rodapé e estrutura da página sejam montados com o editor de modelo.

## Uso {#usage}

O componente de página forma a base de todas as páginas projetadas com os componentes principais, bem como modelos editáveis. Usando o componente de página, os cabeçalhos, rodapés e a estrutura da página podem ser definidos como um modelo usando os outros componentes principais.

Usando a caixa de diálogo [design](#design-dialog), bibliotecas personalizadas do lado do cliente podem ser definidas para a página. Ao contrário de outros componentes que têm uma caixa de diálogo de edição acessível diretamente do componente, como o componente é a própria página, a [caixa de diálogo de edição](#edit-dialog) do componente de página é a janela de propriedades da página.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de página é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | Compatível | Compatível | Compatível |
| [v1](v1/page-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de página [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_page_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Editar caixa de diálogo {#edit-dialog}

Como o componente representa a página inteira, as configurações que normalmente estariam em uma caixa de diálogo de edição são encontradas na janela [Propriedades da página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Caixa de diálogo Design {#design-dialog}

Como o componente representa a página inteira, a caixa de diálogo de design é acessada por **Informações da página -> Política da página** ao editar o modelo da página.

![Política da página](/help/assets/page-policy.png)

>[!NOTE]
>
>Em versões anteriores do AEM, **Política de página** era chamado **Design de página**.

### Guia Propriedades {#properties-tab}

Usando a janela Design de página, você pode definir as bibliotecas do cliente a serem carregadas, bem como a biblioteca de recursos da Web para a página.

* **Bibliotecas**  do cliente: define as categorias da biblioteca do cliente a serem carregadas. O JavaScript é adicionado na extremidade do corpo e o CSS é adicionado ao cabeçalho da página.
* **Cabeçalho**  da página JavaScript das bibliotecas do cliente: define as categorias da biblioteca do cliente JavaScript a serem carregadas no cabeçalho da página.
   * As categorias definidas aqui que também estão presentes no campo **Bibliotecas do cliente** terão o JavaScript carregado no cabeçalho da página em vez de no final do corpo.
   * Nenhum CSS será carregado a menos que a categoria também esteja presente no campo **Bibliotecas do cliente**.

* **Biblioteca**  do cliente de recursos da Web - a categoria da biblioteca do cliente usada para fornecer recursos da Web, como favicons.

* **Ignorar para o seletor**  do elemento de conteúdo principal - Usado como um recurso de acessibilidade para pular diretamente para o conteúdo principal da página

![Caixa de diálogo de design do componente de página](/help/assets/page-design.png)

As bibliotecas podem ser configuradas para os campos **Bibliotecas do cliente** e **Cabeçalho de página JavaScript das bibliotecas do cliente** da seguinte forma:

* Para adicionar um novo campo, clique ou toque no botão **Adicionar** abaixo dos campos.
* Para remover um campo, clique ou toque no ícone da lixeira ao lado do campo a ser removido.
* Para reorganizar a ordem de carregamento, clique ou toque e arraste a alça ao lado do campo a ser movido.

Para obter mais informações sobre o uso de bibliotecas do lado do cliente, consulte [Usando bibliotecas do lado do cliente](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>A capacidade de definir separadamente as bibliotecas do cliente para o cabeçalho da página foi introduzida com os componentes principais versão 2.2.0.

### Guia Estilos {#styles-tab}

O Componente de página suporta o Sistema de estilo AEM [](/help/get-started/authoring.md#component-styling).

## Camada de Dados do Cliente Adobe {#data-layer}

O Componente de Página suporta a [Camada de Dados do Cliente Adobe.](/help/developing/data-layer/overview.md)
