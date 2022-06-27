---
title: Componente Índice
description: O Componente de índice cria um ToC com base nos títulos do conteúdo da página, permitindo que os leitores naveguem rapidamente pela página.
role: Architect, Developer, Admin, User
exl-id: 006adde2-ebff-4e74-8e79-325cccd43e8f
source-git-commit: 394a8b968d7bcde7e766ed719c5914ec5cb60744
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 22%

---

# Componente Índice {#table-of-contents-component}

O Componente de índice cria um ToC com base nos títulos do conteúdo da página, permitindo que os leitores naveguem rapidamente pela página.

## Uso {#usage}

O componente Índice oferece aos visitantes do site a capacidade de navegar rapidamente pelo conteúdo de sua página por meio de um ToC gerado com eficiência, com base nos títulos do conteúdo das páginas.

* O ToC é gerado no lado do servidor.
* Ele é totalmente armazenado em cache pelo dispatcher para entrega rápida.
* Funciona com todos os componentes na página, não apenas os Componentes principais.

O [caixa de diálogo editar](#edit-dialog) permite que o autor de conteúdo defina o intervalo de títulos a serem usados no ToC. Usar o [caixa de diálogo de design](#design-dialog), o autor do modelo pode definir o valor padrão para os títulos quando um autor de conteúdo adiciona um Componente de índice a uma página, bem como restringir os títulos incluídos no ToC com base em nomes de classe.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de índice é a v1, que foi introduzida com a versão 2.20.0 dos Componentes principais em maio de 2022, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente de índice, bem como ver exemplos de suas opções de configuração, bem como a saída do HTML e JSON, visite o [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_tableofcontents).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de índice [pode ser encontrado no GitHub](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo defina os intervalos de níveis de título que o Componente de índice deve renderizar como ToC.

![Caixa de diálogo de edição do componente Índice](/help/assets/tableofcontents-edit.png)

**Tipo de lista** - Essa opção define se a lista deve ser uma lista com marcadores ou uma lista numerada.
* **Nível inicial do título** - Essa opção define o nível mais alto de títulos que o Componente de índice deve renderizar.
* **Nível de interrupção do título** - Essa opção define o nível mais baixo de títulos que o Componente de índice deve renderizar.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

## Caixa de diálogo de design {#design-dialog}

Usando a caixa de diálogo de design, o autor do modelo pode definir o valor padrão para o intervalo de título do Componente do Índice, bem como restringir títulos incluídos no ToC com base em nomes de classe.

### Guia Propriedades {#properties-tab}

![Caixa de diálogo de design do componente de Pesquisa rápida](/help/assets/tableofcontents-design.png)

* **Restringir tipo de lista** - Essa opção define o tipo de lista que o componente gerará. Selecionar essa opção restringe a capacidade do autor de conteúdo de escolher um tipo de lista diferente.
* **Restringir o nível inicial** - Essa opção define o nível de título mais alto que o autor de conteúdo pode selecionar para definir a ToC.
* **Restringir o nível de parada** - Essa opção define o nível de título mais baixo que o autor de conteúdo pode selecionar para definir a ToC.
* **Incluir nomes de classe** - Se esta opção estiver definida, somente os títulos com os nomes de classe especificados ou contidos em elementos dos nomes de classe especificados serão considerados pelo Componente de Índice.
   * Toque ou clique no botão **Adicionar** ícone para adicionar um ou mais nomes de classe.
   * Toque ou clique no botão **Excluir** ícone ao lado de um nome de classe para excluí-lo.
* **Ignorar Nomes de Classe** - Se esta opção estiver definida, os títulos com os nomes de classe especificados ou contidos em elementos dos nomes de classe especificados serão ignorados pelo Componente de Índice.
   * Toque ou clique no botão **Adicionar** ícone para adicionar um ou mais nomes de classe.
   * Toque ou clique no botão **Excluir** ícone ao lado de um nome de classe para excluí-lo.

### Guia Estilos {#styles-tab}

O componente Índice suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

## Camada de dados de clientes Adobe {#data-layer}

O componente Índice suporta o [Camada de dados do cliente Adobe.](/help/developing/data-layer/overview.md)
