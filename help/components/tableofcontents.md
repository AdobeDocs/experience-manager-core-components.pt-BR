---
title: Componente de índice
description: O Componente de índice cria um índice com base nos títulos do conteúdo da página, permitindo que os leitores naveguem rapidamente pela página.
role: Architect, Developer, Admin, User
exl-id: 006adde2-ebff-4e74-8e79-325cccd43e8f
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 100%

---


# Componente de índice {#table-of-contents-component}

O Componente de índice cria um índice com base nos títulos do conteúdo da página, permitindo que os leitores naveguem rapidamente pela página.

{{traditional-aem}}

## Uso {#usage}

O componente de índice oferece aos visitantes do site a capacidade de navegar rapidamente pelo conteúdo da página por meio de um índice gerado eficientemente com base nos títulos do conteúdo das páginas.

* O índice é gerado no lado do servidor.
* Ele é totalmente armazenado em cache pelo Dispatcher para entrega rápida.
* Ele funciona com todos os componentes na página, não apenas com os Componentes principais.

A [caixa de diálogo de edição](#edit-dialog) permite que o autor do conteúdo defina o intervalo de títulos que será usado no índice. Usando a [caixa de diálogo de design](#design-dialog), o autor do modelo pode definir o valor padrão para os títulos quando um autor de conteúdo adiciona um Componente de índice a uma página, bem como restringir os títulos incluídos no índice com base em nomes de classe.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de índice é a v1, introduzida com a versão 2.20.0 dos Componentes principais em maio de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

>[!NOTE]
>
>No AEM as a Cloud Service, seu administrador precisa ativar um filtro para o componente para que ele renderize o conteúdo do componente.
>
>[Consulte a documentação do componente no GitHub](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1) para obter mais informações.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de índice [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo defina os intervalos de níveis de título que o Componente de índice deve renderizar como índice.

![Caixa de diálogo de edição do Componente de índice](/help/assets/tableofcontents-edit.png)

**Tipo de lista**: essa opção define se a lista deve ser uma lista com marcadores ou uma lista numerada.
* **Nível inicial do título**: essa opção define o nível mais alto de títulos que o Componente de índice deve renderizar.
* **Nível de interrupção do título**: essa opção define o nível mais baixo de títulos que o Componente de índice deve renderizar.
* **ID**: Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

## Caixa de diálogo Design {#design-dialog}

Usando a caixa de diálogo de design, o autor do modelo pode definir o valor padrão para o intervalo de título do Componente de índice, bem como restringir títulos incluídos no índice com base em nomes de classe.

### Guia Propriedades {#properties-tab}

![Caixa de diálogo de design do componente de Pesquisa rápida](/help/assets/tableofcontents-design.png)

* **Tipo de lista restrita**: essa opção define o tipo de lista que o componente gerará. Selecionar essa opção restringe a capacidade do autor do conteúdo de escolher um tipo de lista diferente.
* **Restringir o nível inicial**: essa opção define o nível de título mais alto que o autor de conteúdo pode selecionar para definir o índice.
* **Restringir o nível de interrupção**: essa opção define o nível de título mais baixo que o autor do conteúdo pode selecionar para definir o índice.
* **Incluir nomes de classe**: se esta opção estiver definida, somente os títulos com os nomes de classe especificados ou contidos em elementos dos nomes de classe especificados serão considerados pelo Componente de índice.
   * Toque ou clique no ícone **Adicionar** para adicionar um ou mais nomes de classe.
   * Toque ou clique no ícone **Excluir** ao lado de um nome de classe para excluí-lo.
* **Ignorar nomes de classe**: se esta opção estiver definida, os títulos com os nomes de classe especificados ou contidos em elementos dos nomes de classe especificados serão ignorados pelo Componente de índice.
   * Toque ou clique no ícone **Adicionar** para adicionar um ou mais nomes de classe.
   * Toque ou clique no ícone **Excluir** ao lado de um nome de classe para excluí-lo.

### Guia Estilos {#styles-tab}

O componente de índice é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes da Adobe {#data-layer}

O componente de índice é compatível com a [Camada de dados de clientes da Adobe.](/help/developing/data-layer/overview.md)
