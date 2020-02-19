---
title: Componente do carrossel
description: O componente carrossel permite que o autor do conteúdo apresente conteúdo em um carrossel rotativo.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Componente do carrossel{#carousel-component}

O componente principal do carrossel permite que o autor do conteúdo apresente conteúdo em um carrossel navegável.

## Uso {#usage}

Usando o componente carrossel, o autor do conteúdo para organizar o conteúdo em um carrossel rotativo de slides.

A caixa de diálogo [de](#edit-dialog) edição permite que o autor do conteúdo crie, nomeie e solicite vários slides, além de ativar a transição automática com atraso. Usando a caixa de diálogo [de](#design-dialog)design, o autor do modelo pode definir quais componentes podem ser adicionados ao carrossel, ativar ou desativar transições automáticas e personalizar os estilos.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente carrossel é a v1, que foi introduzida com a versão 2.2.0 dos componentes principais em outubro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como Cloud Service |
|--- |--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](/help/versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o componente carrossel e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_carousel)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente do carrossel [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Edit Dialog {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo adicione, renomeie e reorganize slides, além de definir as configurações de transição automática.

### Guia Itens {#items-tab}

![](/help/assets/screen-shot-2019-08-29-12.01.39.png)

Use o botão **Adicionar** para abrir o seletor de componentes e escolher qual componente adicionar como guia. Depois de adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:

* **Ícone** - o ícone do tipo de componente da guia para facilitar a identificação na lista. Passe o mouse sobre o mouse para ver o nome completo do componente como uma dica de ferramenta.
* **Descrição** - A descrição usada como o texto da guia, padronizando com o nome do componente selecionado para a guia.
* **Excluir** - Toque ou clique para excluir a guia do componente de guias.
* **Reordenar** - Toque ou clique e arraste para ordenar as guias.

>[!TIP]
>
>Se o visor da página for reduzido para que a caixa de diálogo de edição se torne tela cheia, o botão **Adicionar** ficará oculto. Os componentes ainda podem ser adicionados ao componente do carrossel, [arrastando-se do navegador de componentes e soltando-o no componente do carrossel no editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component-from-the-components-browser)de páginas.

### Guia Propriedades {#properties-tab}

![](/help/assets/screen-shot-2019-08-29-12.01.57.png)

Na guia **Propriedades** , o autor do conteúdo pode definir os slides para transição automática.

* **Transição automática de slides** - quando ativo, o componente avançará automaticamente para o próximo slide após um atraso especificado.
* **Atraso** na transição - Quando os slides de transição automática são selecionados, esse valor é usado para definir o atraso entre as transições (em milissegundos).
* **Desativar pausa automática ao passar o mouse** - Quando os slides **de transição** automática forem selecionados, a transição do carrossel pausará automaticamente sempre que o cursor passar sobre o carrossel. Selecione essa opção para que a transição não pause.

>[!NOTE]
>
>Os controles de avanço do slide não são ativados no modo **Editar** . Use o modo [**Visualizar **ou a opção](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)Visualizar como publicado **[](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)**para interagir com o carrossel como um leitor do conteúdo publicado.
>
>O recurso de avanço automático não é ativado no modo **Editar** . Use a opção **[Exibir como publicado](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)**para ver o recurso de avanço automático como um leitor do conteúdo publicado.

### Guia Acessibilidade {#accessibility-tab}

![](/help/assets/screen-shot-2019-08-29-12.02.22.png)

Na guia **Acessibilidade** , os valores podem ser definidos para rótulos de acessibilidade [](https://www.w3.org/WAI/standards-guidelines/aria/) ARIA para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

## Select Panel {#select-panel}

O autor do conteúdo pode usar a opção **Selecionar painel** na barra de ferramentas do componente para mudar para um slide diferente para edição, bem como para reorganizar facilmente a ordem dos slides.

![](/help/assets/screenshot_2018-10-11at165417.png)

Depois de selecionar a opção **Selecionar painel** na barra de ferramentas do componente, os slides configurados são exibidos como um menu suspenso.

* A lista é ordenada pela organização atribuída dos slides e é refletida na numeração.
* O tipo de componente do slide é exibido primeiro, seguido pela descrição do slide com uma fonte mais leve.

![](/help/assets/opera_snapshot_2018-11-28141537localhost.png)

* Tocar ou clicar em uma entrada na lista suspensa alterna a visualização no editor para esse slide.
* O slide pode ser reorganizado no local usando as alças de arrastar.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais componentes podem ser adicionados como slides ao componente do carrossel, bem como definir padrões de transição automática e quais estilos personalizados estão disponíveis para o autor do conteúdo.

### Guia Propriedades {#properties-tab-1}

A guia **Propriedades** é usada para definir as configurações padrão para as transições de slides quando um autor de conteúdo adiciona o componente carrossel a uma página.

![](/help/assets/screenshot_2018-11-28at141824.png)

* **Transição automática de slides** - define se, por padrão, a opção de avançar automaticamente o carrossel para o próximo slide está ativada quando o autor do conteúdo adiciona o componente do carrossel a uma página.
* **Atraso** na transição - Define o valor padrão do atraso de transição entre slides (em milissegundos) quando um autor de conteúdo adiciona o componente carrossel a uma página.
* **Desativar pausa automática ao passar o mouse** - Define se, por padrão, a opção para desativar a pausa automática do slide está ativada quando os slides **de transição** automática estão selecionados pelo autor do conteúdo.

### Guia Componentes permitidos {#allowed-components-tab}

A guia Componentes **** permitidos é usada para definir quais componentes podem ser adicionados como slides ao componente carrossel pelo autor do conteúdo.

A guia Componentes permitidos funciona da mesma maneira que a guia do mesmo nome ao [definir a política e as propriedades de um Contêiner de layout no Editor de modelos.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Guia Estilos {#styles-tab}

O componente carrossel suporta o sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
