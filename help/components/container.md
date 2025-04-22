---
title: Componente de Contêiner
description: O componente de Contêiner, dos Componentes principais, permite a criação de um contêiner para vários componentes adicionais em uma página.
role: Architect, Developer, Admin, User
exl-id: 53c7190d-44cb-42ff-bc1a-483c7875bcf8
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 99%

---

# Componente de Contêiner{#container-component}

O componente de Contêiner, dos Componentes principais, permite a criação de um contêiner para vários componentes adicionais em uma página.

## Uso {#usage}

O componente de Contêiner, dos Componente principais, permite a criação de um contêiner para vários componentes adicionais em uma página e pode ser usado para agrupar outros componentes e aplicar um estilo ou layout comum.

* As propriedades do contêiner podem ser selecionadas na [caixa de diálogo de configuração](#configure-dialog).
* Os padrões do componente de Contêiner ao adicioná-lo a uma página podem ser definidos na [caixa de diálogo de design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Contêiner é a v1, que foi introduzida com a versão 2.5.0 dos Componentes principais em junho de 2019, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v1 | Compatível com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Contêiner, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_container_br).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Contêiner [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_container_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o item do contêiner e como ele se comportará e será exibido para um visitante da página.

![Caixa de diálogo de edição do componente de Contêiner](/help/assets/container-edit.png)

* **Layout** - Essa opção define o comportamento ou o comportamento do layout do componente de Contêiner.
   * **Simples** - Define um contêiner como uma coleção simples de componentes
   * **Grade responsiva** - Define um contêiner como um [Layout responsivo do AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html?lang=pt-BR)
* **Cor do plano de fundo** - Definível como valores RGB de forma livre ou usando o seletor de cores, [dependendo da configuração](#background-tab)
* **Imagem de plano de fundo** - Define uma cor de plano de fundo para o contêiner,  [dependendo da configuração](#background-tab)
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o componente de Contêiner.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** é usada para definir quais componentes podem ser adicionados como itens ao componente de Contêiner pelo autor de conteúdo.

Ela funciona da mesma maneira que a guia de mesmo nome ao [definir a política e as propriedades de um Contêiner de layout no Editor de modelo.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR)

### Guia Componentes padrão {#default-components-tab}

A guia Componentes padrão é usada para definir qual componente é adicionado ao componente quando um tipo de ativo específico é descartado no contêiner, de modo semelhante a [como os componentes padrão são definidos no modelo de página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR).

### Guia Configurações responsivas {#responsive-settings-tab}

![Guia Configurações responsivas da caixa de diálogo de design do componente de Contêiner](/help/assets/container-design-responsive.png)

* **Colunas** - Define o número de colunas na grade do contêiner resultante.

### Guia Plano de fundo {#background-tab}

![Guia Plano de fundo da caixa de diálogo de design do componente do Contêiner](/help/assets/container-design-background.png)

* **Imagem de plano de fundo**
   * **Ativar imagem de plano de fundo** - Selecione esta opção para permitir que o autor de conteúdo defina uma imagem de plano de fundo para o contêiner.
* **Cor do plano de fundo**
   * **Ativar cor de plano de fundo** - Selecione esta opção para permitir que o autor de conteúdo defina uma cor de plano de fundo para o contêiner.
   * **Somente amostras** - Selecione essa opção para permitir que o autor de conteúdo selecione apenas a partir de amostras de cores predefinidas para a cor de fundo do contêiner.
      * Disponível apenas quando **Ativar cor de plano de fundo** estiver selecionado
* **Amostras permitidas** - Defina as cores predefinidas a partir das quais o autor de conteúdo pode selecionar a cor do plano de fundo do contêiner
   * Use o botão **Adicionar** para adicionar uma amostra de cor predefinida. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:
   * **Valor** - defina a cor manualmente por meio dos valores RGB
      * Toque ou clique no seletor de cores para selecionar uma cor mais facilmente, ajustando valores RGB individuais ou definindo um valor hexadecimal.
   * **Excluir** - Toque ou clique para excluir uma amostra.
   * **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem das amostras.

### Guia Estilos {#styles-tab}

O componente de Contêiner é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
