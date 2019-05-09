---
title: Componente de Teaser
seo-title: Componente de Teaser
description: O componente de teaser pode mostrar uma imagem, um título, rich text e, opcionalmente, um link para outro conteúdo.
seo-description: O componente de teaser pode mostrar uma imagem, um título, rich text e, opcionalmente, um link para outro conteúdo.
uuid: 46989314-df 37-448 b -8562-c 707043 f 2160
contentOwner: bohnert
content-type: referência
topic-tags: componentes principais
discoiquuid: e 597 c 18 e -3643-41 be -9878-4 a 7872 f 1 ab 90
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de Teaser{#teaser-component}

O componente de Teaser principal do componente pode mostrar uma imagem, um título, rich text e, opcionalmente, um link para outro conteúdo.

## Uso {#usage}

O Componente de Teaser permite que o autor do conteúdo crie facilmente um teaser para mais conteúdo usando uma imagem, um título ou texto formatado e links para mais conteúdo ou outras ações.

O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir se as opções para criar chamadas de chamada e adicionar links estão disponíveis e desativar várias opções de exibição. O autor do conteúdo pode usar a caixa [de diálogo](#configure-dialog) Configurar para definir uma imagem, definir ctas, definir títulos e descrições e configurar links para o teaser individual. A caixa de diálogo [de edição](image.md#edit-dialog) do Componente [de imagem](image.md) pode ser acessada para modificar a imagem de teaser.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente Teaser é v 1, que foi introduzida com a versão 2.1.0 dos Componentes principais em julho de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v1 | Compatível | Compatível | Compatível |

## Exemplo de saída do componente {#sample-component-output}

A seguir está uma amostra tirada de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/screen_shot_2018-07-04at145042.png)

### Biblioteca de componentes

Para experimentar o componente de Teaser, bem como ver exemplos de suas opções de configuração, além de HTML e saída JSON, visite a Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/teaser.html).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Teaser [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Configurar caixa de diálogo {#configure-dialog}

O autor do conteúdo pode usar a caixa de diálogo Configurar para definir as propriedades do teaser individual. Também há uma caixa de diálogo [de edição](#edit-dialog) para modificar a imagem de teaser se houver uma selecionada.

### Imagem {#image}

![](assets/screen_shot_2018-07-03at104125.png)

* **Ativos da imagem**
   * Solte um ativo do navegador [de ativos](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) ou toque na opção **Procurar** para fazer upload de um sistema de arquivos local.
   * Toque ou clique **em Limpar** para desmarcar a imagem selecionada no momento.
   * Toque ou clique **em Editar** para [editar as representações do ativo](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) no editor de ativos.

### Text {#text}

![](assets/screen_shot_2018-07-03at104138.png)

* **Título**
Define um título para exibir como o cabeçalho do teaser.
* **Obter título de página
vinculada** Quando marcado, o título será preenchido com o título da página vinculada.
* **Descrição**
Define uma descrição a ser exibida como o artigo do teaser.
* **Obter descrição de página
vinculada** quando marcada, a descrição será preenchida com a descrição da página vinculada.

### Links e ações {#links-actions}

![](assets/screen_shot_2018-07-03at104146.png)

* **Link Link**
aplicado ao teaser. Use o navegador de caminho para selecionar o destino do link.
* **Ativar chamadas de chamada** quando marcadas, permite a definição de chamada de ações. O primeiro link de Chamada de ação na lista é usado como link para outros elementos de teaser.

## Editar caixa de diálogo {#edit-dialog}

O componente de Teaser delega a renderização de imagens ao componente [de imagem](image.md). Portanto, [a caixa de diálogo]Editar (image. md # edit-dialog do componente de imagem está disponível para o autor do conteúdo para manipular a imagem de teaser.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de teaser que o autor do conteúdo tem ao usar este componente.

### Guia Teaser {#teaser-tab}

![](assets/screen_shot_2018-07-03at105958.png)

* **Frases de chamariz**
   * **Desativar chamadas de chamada** para ocultar a **opção** de chamada para autores de conteúdo
* **Elementos**
   * **Ocultar título**
      * Oculta a **opção Título** para autores de conteúdo
      * Quando selecionado o **Tipo** de título está oculto
   * **Ocultar descrição**
Oculta a opção **Descrição** para autores de conteúdo
* **Tipo
de título** Define a tag H a ser usada pelo título do teaser.
* **Links**
   * **Não vincular a imagem**
Quando selecionada, a imagem de teaser não é vinculada
   * **Não vincular o título**
Quando selecionado, o título de teaser não é vinculado

### Guia Estilos {#styles-tab}

O componente de Teaser é compatível com o Sistema [de estilo do AEM](authoring.md#component-styling).
