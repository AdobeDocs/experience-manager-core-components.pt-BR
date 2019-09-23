---
title: Componente da página
seo-title: Componente da página
description: O Componente de página é um componente de página extensível projetado para trabalhar com o editor de modelo e permitir que os componentes de cabeçalho/rodapé e estrutura da página sejam montados com o editor de modelo.
seo-description: O Componente de página é um componente de página extensível projetado para trabalhar com o editor de modelo e permitir que os componentes de cabeçalho/rodapé e estrutura da página sejam montados com o editor de modelo.
uuid: 7052a5b1-e7f1-4944-a55c-faf739b6e89c
contentOwner: Usuário
content-type: referência
topic-tags: autoria
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: cb1a745a-30c4-4ad6-a04f-fefb3666cd95
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Componente da página{#page-component}

O Componente de página é um componente de página extensível projetado para trabalhar com o editor [de](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) modelo e permite que os componentes de cabeçalho/rodapé e estrutura da página sejam montados com o editor de modelo.

## Uso {#usage}

O componente de página forma a base de todas as páginas projetadas com os componentes principais, bem como modelos editáveis. Usando o componente de página, os cabeçalhos, rodapés e a estrutura da página podem ser definidos como um modelo usando os outros componentes principais.

Usando a caixa de diálogo [de](#design-dialog)design, bibliotecas personalizadas do lado do cliente podem ser definidas para a página. Ao contrário de outros componentes que têm uma caixa de diálogo de edição acessível diretamente do componente, como o componente é a própria página, a caixa de diálogo [de](#edit-dialog) edição do componente da página é a janela de propriedades da página.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de página é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| [v2](page-v1.md) | Compatível | Compatível | Compatível |
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

>[!NOTE]
>
>Para ativar o redirecionamento no `cq:Page` nível para a versão 2 do componente de página e AEM 6.3, é necessário o [service pack 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html) ou posterior. Esse redirecionamento não estava disponível em versões anteriores.

## Exemplo de saída de componente {#sample-component-output}

A seguir está uma amostra retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/chlimage_1.png)

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de página [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

## Edit Dialog {#edit-dialog}

Como o componente representa a página inteira, as configurações que normalmente estariam em uma caixa de diálogo de edição são encontradas na janela Propriedades [da](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-page-properties.html) página.

## Caixa de diálogo Design {#design-dialog}

Como o componente representa a página inteira, a caixa de diálogo de design é acessada por meio de Informações da **página -&gt; Política** da página ao editar o modelo da página.

![](assets/screen_shot_2018-04-03at113410.png)

>[!NOTE]
>
>Em versões anteriores do AEM, a Política **de** página era chamada de Design **de** página.

### Guia Propriedades {#properties-tab}

Usando a janela Design de página, você pode definir as bibliotecas do cliente a serem carregadas, bem como a biblioteca de recursos da Web para a página.

* **Bibliotecas** do clienteDefine as categorias da biblioteca do cliente a serem carregadas. O JavaScript é adicionado na extremidade do corpo e o CSS é adicionado ao cabeçalho da página.
* **Cabeçalho** da página JavaScript das bibliotecas do clienteDefine as categorias da biblioteca do cliente JavaScript a serem carregadas no cabeçalho da página.
   * As categorias definidas aqui que também estão presentes no campo Bibliotecas **do** cliente terão o JavaScript carregado no cabeçalho da página em vez de no final do corpo.
   * Nenhum CSS será carregado, a menos que a categoria também esteja presente no campo Bibliotecas **do** cliente.

* **Biblioteca** do cliente de recursos da Web A categoria da biblioteca do cliente usada para fornecer recursos da Web, como favicons.

![](assets/screenshot_2018-10-19at104949.png)

As bibliotecas podem ser configuradas para os campos **Client Libraries** e **Client Library JavaScript Page Head** da seguinte maneira:

* Para adicionar um novo campo, clique ou toque no botão **Adicionar** abaixo dos campos.
* Para remover um campo, clique ou toque no ícone da lixeira ao lado do campo a ser removido.
* Para reorganizar a ordem de carregamento, clique ou toque e arraste a alça ao lado do campo a ser movido.

Para obter mais informações sobre o uso de bibliotecas do lado do cliente, consulte [Uso de bibliotecas](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html)do lado do cliente.

>[!CAUTION]
>
>A capacidade de definir separadamente as bibliotecas do cliente para o cabeçalho da página foi introduzida com os componentes principais versão 2.2.0.

### Guia Estilos {#styles-tab}

O Componente de página suporta o Sistema [de](authoring.md#component-styling)estilo AEM.