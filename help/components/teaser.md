---
title: Componente de Teaser
description: O componente de Teaser pode mostrar uma imagem, um título, um rich text e, opcionalmente, vincular a conteúdo adicional.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: cfc86203051739cbcdc30be0fb10ccffa7d583a5
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 100%

---

# Componente de Teaser {#teaser-component}

O componente de Teaser, do Componentes principais, pode mostrar uma imagem, um título, um rich text e, opcionalmente, um link para conteúdo adicional.

## Uso {#usage}

O componente de Teaser permite que o autor do conteúdo crie facilmente um teaser para conteúdo adicional usando uma imagem, título ou rich text e vinculando a conteúdo adicional ou outras ações.

O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir se as opções para criar frases de chamariz e adicionar links estão disponíveis, bem como desativar várias opções de exibição. O autor do conteúdo pode usar o [a caixa de diálogo de configuração](#configure-dialog) para configurar uma imagem, definir CTAs, definir títulos e descrições e configurar links para o teaser individual. A [caixa de diálogo de edição](image.md#edit-dialog) do [componente de Imagem](image.md) pode ser acessada para modificar a imagem do teaser.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de teaser é a v2, introduzida com a versão 2.18.0 dos componentes principais em fevereiro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | - | Compatível | Compatível |
| [v1](v1/teaser.md) | Compatível | Compatível | Compatível |

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Teaser, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_teaser_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Teaser [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

O autor do conteúdo pode usar a caixa de diálogo de configuração para definir as propriedades do teaser individual. Também há uma [caixa de diálogo de edição](#edit-dialog) para modificar a imagem do teaser, se essa opção estiver selecionada.

### Guia Links {#links-tab}

![Guia Links da caixa de diálogo de edição do componente de teaser](/help/assets/teaser-edit-links.png)

O título, a descrição e a imagem do teaser podem ser herdados da página vinculada ou da página vinculada na primeira frase de chamariz. Se não for especificado um link ou uma frase de chamariz, o título, a descrição e a imagem serão herdados da página atual.

* **Link** - Este arquivo vincula à uma página de conteúdo, um URL externo ou uma âncora de página.
* **Abrir link em nova guia** - Se habilitada, o link será aberto em uma nova guia do navegador.
* **Frases de chamariz** - Esta opção permite vincular a vários destinos.
   * A página vinculada na primeira frase de chamariz é usada ao herdar o título, a descrição ou a imagem do teaser.

### Guia Texto {#text-tab}

![Guia Texto da caixa de diálogo de edição do componente de Teaser](/help/assets/teaser-edit-text.png)

* **Pre-título** - O pre-título será exibido antes do título do teaser.
* **Título** - Define um título a ser exibido como o título do teaser.
   * **Obter título da página vinculada** - Quando marcado, o título será preenchido com o título da página vinculada.
* **Descrição** - Define uma descrição a ser exibida como o subtítulo do teaser.
   * **Obter descrição da página vinculada** - Quando marcada, a descrição será preenchida com a descrição da página vinculada.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Guia Ativo {#asset-tab}

![Guia Imagem da caixa de diálogo de edição do componente de teaser](/help/assets/teaser-edit-image.png)

* **Herdar imagem em destaque da página** - Use a imagem definida nas propriedades da página vinculada ou da página atual, se nenhuma for encontrada.
* **Ativo de imagem** - Solte um ativo do [navegador de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR) ou toque na opção **procurar** para fazer upload a partir de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=pt-BR) no editor de ativos.
* **Texto alternativo para acessibilidade** - Este campo permite definir uma descrição da imagem para usuários com deficiências visuais.
   * **Herdar texto alternativo da página** - Esta opção utiliza a descrição alternativa do valor do ativo vinculado dos metadados `dc:description` no DAM ou da página atual, se nenhum ativo estiver vinculado.
* **Não fornecer um texto alternativo** - Esta opção marca a imagem a ser ignorada por tecnologias assistivas, como leitores de tela, nos casos em que a imagem é meramente decorativa ou não transmite informações adicionais para a página.

### Guia Estilos {#styles-tab-edit}

![Guia Estilos da caixa de diálogo de edição do componente de lista de teaser](/help/assets/teaser-edit-styles.png)

O componente de teaser é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que o menu suspenso fique disponível.

## Caixa de diálogo de edição {#edit-dialog}

O componente de Teaser delega a renderização da imagem ao [componente de Imagem](image.md). Portanto, a [caixa de diálogo de edição](image.md#edit-dialog) do componente de Imagem está disponível ao autor de conteúdo para manipular a imagem do teaser.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de teaser que o autor do conteúdo terá ao usar esse componente.

### Guia Teaser {#teaser-tab}

![Caixa de diálogo de design do componente de Teaser](/help/assets/teaser-design.png)

* **Frases de chamariz**
   * **Desabilitar frases de chamariz** - Ocultar a opção **Frases de chamariz** para autores de conteúdo
* **Elementos**
   * **Ocultar pre-título** - Oculta a opção de **Pre-título** para autores de conteúdo
   * **Ocultar título** - Oculta a opção de **Título** para autores de conteúdo
      * Quando selecionado, o **Tipo de Título** fica oculto
   * **Ocultar descrição** - Oculta a opção de **Descrição** para autores de conteúdo
* **Tipo de título padrão** - Define a tag H a ser usada pelo título do teaser.
* **Delegar imagem** - Exibição informativa indicando para qual componente o Teaser delega o manuseio de imagem.

### Guia Estilos {#styles-tab}

O componente de Teaser é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Teaser é compatível com a [Camada de dados de clientes Adobe.](/help/developing/data-layer/overview.md)
