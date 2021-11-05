---
title: Componente Carrossel
description: O componente Carrossel permite que o autor de conteúdo apresente conteúdo em um carrossel giratório.
role: Architect, Developer, Admin, User
exl-id: 3331214c-a05c-47e1-b54c-fbfd1045bd60
source-git-commit: 888719359f9a1d1c9dccff97fb639b332f2be54c
workflow-type: ht
source-wordcount: '1115'
ht-degree: 100%

---

# Componente Carrossel{#carousel-component}

O componente Carrossel, dos Componentes principais, permite que o autor do conteúdo apresente conteúdo em um carrossel navegável.

## Uso {#usage}

Com o componente Carrossel, o autor do conteúdo pode organizar o conteúdo em um carrossel giratório de slides.

A [caixa de diálogo de edição](#edit-dialog) permite que o autor de conteúdo crie, nomeie e ordene vários slides e habilite a transição automática com atraso. Usando a [caixa de diálogo de design](#design-dialog), o autor do modelo pode definir quais componentes podem ser adicionados ao carrossel, ativar ou desativar transições automáticas e personalizar os estilos.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente Carrossel é a v1, introduzida com a versão 2.2.0 dos Componentes principais em outubro de 2018, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Carrossel, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_carousel_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Carrossel [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo adicione, renomeie e reorganize os slides e defina as configurações de transição automática.

### Guia Itens {#items-tab}

![Guia Itens da caixa de diálogo de edição do componente Carrossel](/help/assets/carousel-edit-items.png)

Use o botão **Adicionar** para abrir o seletor de componentes e escolher que componente adicionar como guia. Uma vez adicionado, uma entrada é adicionada à lista, contendo as seguintes colunas:

* **Ícone** - O ícone do tipo de componente da guia para facilitar a identificação na lista. Passe o mouse sobre o ícone para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição** - A descrição usada como o texto da guia, padronizando o nome do componente selecionado para a guia.
* **Excluir** - Toque ou clique para excluir a guia do componente de Guias.
* **Reordenar** - Toque ou clique e arraste para ordenar as guias.

>[!TIP]
>
>Se a janela de visualização da página for reduzida para que a caixa de diálogo de edição se torne tela cheia, o botão **Adicionar** ficará oculto. Também é possível adicionar componentes ao componente Carrossel ao [arrastar do navegador de componentes e soltar no componente Carrossel no editor de páginas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR#inserting-a-component-from-the-components-browser).

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do componente Carrossel](/help/assets/carousel-edit-properties.png)

Na guia **Propriedades**, o autor de conteúdo pode definir os slides para fazer a transição automática.

* **Fazer transição automática de slides** - Quando ativo, o componente avança automaticamente para o próximo slide após um atraso especificado.
* **Atraso de transição** - Quando Fazer transição automática de slides é selecionado, esse valor é usado para definir o atraso entre as transições (em milissegundos).
* **Desativar a pausa automática ao passar o cursor** - Quando a opção **Fazer transição automática de slides** estiver selecionado, a transição do carrossel será automaticamente pausada sempre que cursor for passado sobre o carrossel. Selecione essa opção para que a transição não seja pausada.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

>[!NOTE]
>
>Os controles de avanço de slides não são ativados quando estão no modo **Editar**. Use o modo [**Visualização**](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR#preview-mode) ou a opção **[Visualizar como publicado](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR#view-as-published)** para interagir com o carrossel como um leitor do conteúdo publicado.
>
>O recurso de avanço automático não é ativado quando está no modo **Editar**. Use a opção **[Exibir como publicado](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR#view-as-published)** para ver o recurso de avanço automático como um leitor do conteúdo publicado.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade da caixa de diálogo de edição do componente Carrossel](/help/assets/carousel-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

## Selecionar painel {#select-panel}

O autor de conteúdo pode usar a opção **Selecionar painel** na barra de ferramentas do componente para alterar para um slide diferente para edição, e para reorganizar facilmente a ordem dos slides.

![Ícone Selecionar painel](/help/assets/select-panel-icon.png)

Depois de optar por **Selecionar painel** na barra de ferramentas do componente, os slides configurados são exibidos como uma lista suspensa.

* A lista é ordenada pela disposição atribuída dos slides e é refletida na numeração.
* O tipo de componente do slide é exibido primeiro, seguido pela descrição do slide com fonte mais clara.

![Selecionar painel](/help/assets/select-panel-popover.png)

* Tocar ou clicar em uma entrada na lista suspensa altera a exibição do editor para esse slide.
* O slide pode ser reordenado no local usando as alças de arrastar.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais componentes podem ser adicionados como slides ao componente Carrossel, os padrões de transição automática e quais estilos personalizados estão disponíveis para o autor de conteúdo.

### Guia Propriedades {#properties-tab-1}

A guia **Propriedade** é usada para definir as configurações padrão para as transições de slides quando um autor de conteúdo adiciona o componente Carrossel a uma página.

![Caixa de diálogo de design do componente Carrossel](/help/assets/carousel-design.png)

* **Fazer a transição automática de slides** - Define se, por padrão, a opção de avançar automaticamente o carrossel para o próximo slide é ativada quando o autor de conteúdo adiciona o componente Carrossel a uma página.
* **Atraso de transição** - Define o valor padrão do atraso de transição entre os slides (em milissegundos) quando um autor de conteúdo adiciona o componente Carrossel a uma página.
* **Desativar a pausa automática ao passar o cursor** - Define se, por padrão, a opção para desativar a pausa automática de slides é ativada quando a opção **Fazer a transição automática de slides** é selecionada pelo autor de conteúdo.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** é usada para definir quais componentes podem ser adicionados como slides ao componente Carrossel pelo autor de conteúdo.

Ela funciona da mesma maneira que a guia de mesmo nome ao [definir a política e as propriedades de um Contêiner de layout no Editor de modelo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR).

### Guia Estilos {#styles-tab}

O componente Carrossel é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente Carrossel é compatível com a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
