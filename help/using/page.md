---
title: Componente de página
seo-title: Componente de página
description: O componente de página é um componente de página extensível projetado para funcionar com o editor de modelo e permite que os componentes de cabeçalho/rodapé da página e componentes da estrutura sejam montados com o editor de modelo.
seo-description: O componente de página é um componente de página extensível projetado para funcionar com o editor de modelo e permite que os componentes de cabeçalho/rodapé da página e componentes da estrutura sejam montados com o editor de modelo.
uuid: 7052 a 5 b 1-e 7 f 1-4944-a 55 c-faf 739 b 6 e 89 c
contentOwner: Usuário
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: cb 1 a 745 a -30 c 4-4 ad 6-a 04 f-fefb 3666 cd 95
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de página{#page-component}

O componente de página é um componente de página extensível projetado para funcionar com o editor [de modelo](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) e permite que os componentes de cabeçalho/rodapé da página e componentes da estrutura sejam montados com o editor de modelo.

## Uso {#usage}

O componente de página é a base de todas as páginas projetadas com os componentes principais, bem como os modelos editáveis. Usando o componente de página, cabeçalhos, rodapés e a estrutura da página podem ser definidos como um modelo usando os outros componentes principais.

Usando a caixa [de diálogo de design](#design-dialog), as bibliotecas personalizadas do cliente podem ser definidas para a página. Ao contrário de outros componentes que têm uma caixa de diálogo de edição acessível diretamente do componente, visto que o componente é a própria página, a [caixa de diálogo Editar](#edit-dialog) do componente da página é a janela de propriedades da página.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de página é v 2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| [v2](page-v1.md) | Compatível | Compatível | Compatível |
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

>[!NOTE]
>
>Para ativar o redirecionamento no `cq:Page` nível para a versão verdo componente da página e o AEM 6.3, [service pack 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html) ou posterior é necessário. Esse redirecionamento não estava disponível em versões anteriores.

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/chlimage_1.png)

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de página [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Editar caixa de diálogo {#edit-dialog}

Como o componente representa a página inteira, as configurações que normalmente estariam em uma caixa de diálogo de edição são encontradas na [janela Propriedades](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-page-properties.html) da página.

## Caixa de diálogo de design {#design-dialog}

Como o componente representa a página inteira, a caixa de diálogo de design é acessada por **meio de Informações da página -&gt; Política** de página ao editar o modelo de página.

![](assets/screen_shot_2018-04-03at113410.png)

>[!NOTE]
>
>Em versões anteriores do AEM, **a Política** de página era chamada **de Design de página**.

### Guia Propriedades {#properties-tab}

Usando a janela Design de página, você pode definir as bibliotecas do cliente para ser carregado, bem como a biblioteca de recursos da Web para a página.

* **Bibliotecas
do cliente** Isso define as categorias da biblioteca de clientes para carregar. O javascript é adicionado no final do corpo e o CSS é adicionado ao cabeçalho da página.
* **Cabeçalho
de página do javascript Bibliotecas do cliente** Isso define as categorias da biblioteca do cliente javascript para carregar no cabeçalho da página.
   * As categorias definidas aqui também presentes no campo Bibliotecas **do cliente** terão o javascript carregado no cabeçalho da página em vez de no final do corpo.
   * Nenhum CSS será carregado, a menos que a categoria também esteja presente no **campo Bibliotecas** do cliente.

* **Recursos da Web Client Library**
A categoria da biblioteca de cliente usada para servir recursos da Web, como favicons.

![](assets/screenshot_2018-10-19at104949.png)

As bibliotecas podem ser configuradas para os campos de Cabeçalhos de página do **cliente Bibliotecas** do cliente e **Bibliotecas do cliente** da seguinte maneira:

* Para adicionar um novo campo, clique ou toque no **botão Adicionar** abaixo dos campos.
* Para remover um campo, clique ou toque no ícone de lixeira ao lado do campo a ser removido.
* Para reorganizar a ordem de carregamento, clique ou toque e arraste a alça ao lado do campo a ser movido.

Para obter mais informações sobre como usar bibliotecas do cliente, consulte [Usar bibliotecas do cliente](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>A capacidade de definir separadamente as bibliotecas do cliente para o cabeçalho da página foi introduzida com os componentes principais versão 2.2.0.

### Guia Estilos {#styles-tab}

O componente de página é compatível com o Sistema [de estilo AEM](authoring.md#component-styling).