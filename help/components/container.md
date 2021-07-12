---
title: Componente do contêiner
description: O componente Contêiner do componente principal permite a criação de um contêiner para vários componentes adicionais em uma página.
role: Architect, Developer, Admin, User
exl-id: 53c7190d-44cb-42ff-bc1a-483c7875bcf8
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 2%

---

# Componente do contêiner{#container-component}

O componente Contêiner do componente principal permite a criação de um contêiner para vários componentes adicionais em uma página.

## Uso {#usage}

O componente Contêiner do componente principal permite a criação de um contêiner para vários componentes adicionais em uma página e pode ser usado para agrupar outros componentes e aplicar um estilo ou layout comum.

* As propriedades do contêiner podem ser selecionadas na caixa de diálogo [configurar](#configure-dialog).
* Os padrões do Componente de contêiner ao adicioná-lo a uma página podem ser definidos na caixa de diálogo [design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de contêiner é a v1, que foi introduzida com a versão 2.5.0 dos Componentes principais em junho de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de contêiner, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_container).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do contêiner [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_container_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o item do contêiner e como ele se comportará e será exibido para um visitante da página.

![Caixa de diálogo Editar componente do contêiner](/help/assets/container-edit.png)

* **Layout**  - essa opção define o comportamento ou o comportamento do layout do Componente de contêiner.
   * **Simples**  - Define um contêiner como uma coleção simples de componentes
   * **Grade responsiva**  - Define um contêiner como um Layout responsivo  [AEM](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)
* **Cor do Plano de Fundo**  - Definível como valores RGB de forma livre ou usando o seletor de cores,  [dependendo da configuração](#background-tab)
* **Imagem de plano de fundo**  - Define uma cor de plano de fundo para o contêiner,   [dependendo da configuração](#background-tab)
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o Componente de contêiner.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** é usada para definir quais componentes podem ser adicionados como itens ao Componente de contêiner pelo autor de conteúdo.

A guia Componentes permitidos funciona da mesma maneira que a guia do mesmo nome ao [definir a política e as propriedades de um Contêiner de layout no Editor de modelo.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Guia Componentes padrão {#default-components-tab}

A guia Componentes padrão é usada para definir qual componente é adicionado ao componente quando um tipo de ativo específico é descartado no contêiner, de modo semelhante a [como os componentes padrão são definidos no modelo de página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Guia Configurações responsivas {#responsive-settings-tab}

![Guia Configurações responsivas da caixa de diálogo de design do Componente de contêiner](/help/assets/container-design-responsive.png)

* **Colunas**  - Define o número de colunas na grade do contêiner resultante.

### Guia Plano de Fundo {#background-tab}

![Guia Plano de Fundo da caixa de diálogo Design do Componente do Contêiner](/help/assets/container-design-background.png)

* **Imagem de plano de fundo**
   * **Ativar imagem de plano de fundo**  - Selecione esta opção para permitir que o autor de conteúdo defina uma imagem de plano de fundo para o contêiner.
* **Cor do Plano de Fundo**
   * **Ativar cor de plano de fundo**  - Selecione esta opção para permitir que o autor de conteúdo defina uma cor de plano de fundo para o contêiner.
   * **Amostras somente**  - Selecione essa opção para permitir que o autor de conteúdo selecione apenas a partir de amostras de cores predefinidas para a cor de fundo do contêiner.
      * Disponível apenas quando **Ativar cor de fundo** está selecionado
* **Amostras permitidas**  - Defina as cores predefinidas a partir das quais o autor de conteúdo pode selecionar a cor de fundo do contêiner
   * Use o botão **Add** para adicionar uma amostra de cor predefinida. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:
   * **Valor**  - defina a cor manualmente por meio dos valores RGB
      * Toque ou clique no seletor de cores para selecionar uma cor mais facilmente, ajustando valores RGB individuais ou definindo um valor hexadecimal.
   * **Excluir**  - Toque ou clique para excluir uma amostra.
   * **Reorganizar**  - Toque ou clique e arraste para reorganizar a ordem das amostras.

### Guia Estilos {#styles-tab}

O Componente de contêiner é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).
