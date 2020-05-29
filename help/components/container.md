---
title: Componente do Container
description: O componente de Container do componente principal permite a criação de um container para vários componentes adicionais em uma página.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 2%

---


# Componente do Container{#container-component}

O componente de Container do componente principal permite a criação de um container para vários componentes adicionais em uma página.

## Uso {#usage}

O componente Container do componente principal permite a criação de um container para vários componentes adicionais em uma página e pode ser usado para agrupar outros componentes e aplicar um estilo ou layout comum.

* As propriedades do container podem ser selecionadas na caixa de diálogo [](#configure-dialog)configurar.
* Os padrões do componente Container ao adicioná-lo a uma página podem ser definidos na caixa de diálogo [](#design-dialog)de design.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do Container é a v1, que foi introduzida com a versão 2.5.0 dos Componentes Principais em junho de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente do Container e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_container)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente do Container [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_container_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o item do container e como ele se comportará e aparecerá para um visitante da página.

![Editar caixa de diálogo do componente Container](/help/assets/container-edit.png)

* **Layout** - Essa opção define o comportamento ou o comportamento do layout do Componente do Container.
   * **Simples** - Define um container como uma coleção simples de componentes
   * **Grade** responsiva - Define um container como um layout responsivo do [AEM](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)
* **Cor** do Plano de Fundo - Definível como valores RGB de forma livre ou usando o seletor de cores, [dependendo da configuração](#background-tab)
* **Imagem** de plano de fundo - Define uma cor de plano de fundo para o container, [dependendo da configuração](#background-tab)
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor do conteúdo que usa o componente de Container.

### Allowed Components Tab {#allowed-components-tab}

A guia Componentes **** permitidos é usada para definir quais componentes podem ser adicionados como itens ao Componente do Container pelo autor do conteúdo.

A guia Componentes permitidos funciona da mesma maneira que a guia do mesmo nome ao [definir a política e as propriedades de um Container de layout no Editor de modelos.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Default Components Tab {#default-components-tab}

A guia Componentes padrão é usada para definir qual componente é adicionado ao componente quando um tipo de ativo específico é solto no container, de modo semelhante à [forma como os componentes padrão são definidos no modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)de página.

### Guia Configurações responsivas {#responsive-settings-tab}

![Guia Configurações responsivas da caixa de diálogo de design do Componente do Container](/help/assets/container-design-responsive.png)

* **Colunas** - Define o número de colunas na grade do container resultante.

### Guia Plano de fundo {#background-tab}

![Guia Plano de fundo da caixa de diálogo de design do componente Container](/help/assets/container-design-background.png)

* **Imagem de plano de fundo**
   * **Ativar imagem** de plano de fundo - Selecione esta opção para permitir que o autor do conteúdo defina uma imagem de plano de fundo para o container.
* **Cor do Plano de Fundo**
   * **Ativar cor** de plano de fundo - Selecione esta opção para permitir que o autor do conteúdo defina uma cor de plano de fundo para o container.
   * **Amostras apenas** - Selecione essa opção para permitir que o autor do conteúdo selecione apenas em amostras de cores predefinidas para a cor de fundo do container.
      * Disponível somente quando a opção **Ativar cor** de plano de fundo estiver selecionada
* **Amostras** Permitidas - Defina cores predefinidas a partir das quais o autor do conteúdo pode selecionar a cor de fundo do container
   * Use o botão **Adicionar** para adicionar uma amostra de cor predefinida. Depois de adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:
   * **Valor** - Defina a cor manualmente por meio de valores RGB
      * Toque ou clique no seletor de cores para selecionar mais facilmente uma cor ajustando valores RGB individuais ou definindo um valor hexadecimal.
   * **Excluir** - Toque ou clique para excluir uma amostra.
   * **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem das amostras.

### Guia Estilos {#styles-tab}

O componente Container suporta o AEM [Style System](/help/get-started/authoring.md#component-styling).
