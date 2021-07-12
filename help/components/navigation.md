---
title: Componente de navegação
description: O Componente de navegação permite que os usuários naveguem facilmente em uma estrutura de site globalizada.
role: Architect, Developer, Admin, User
exl-id: 9154f2a3-3d1e-4865-a413-298748fa66d3
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 1%

---

# Componente de navegação{#navigation-component}

O Componente de navegação permite que os usuários naveguem facilmente em uma estrutura de site globalizada.

## Uso {#usage}

O componente de navegação lista uma árvore de páginas para que os usuários de um site possam navegar facilmente pela estrutura do site.

O Componente de navegação pode detectar automaticamente a estrutura globalizada do site e [adaptar-se automaticamente a uma página localizada.](#localized-site-structure) Além disso, ele pode suportar qualquer estrutura de site arbitrária usando  [páginas de redirecionamento de ](#shadow-structure) sombra para representar outra estrutura diferente da estrutura de conteúdo principal.

A caixa de diálogo [edit](#edit-dialog) permite que o autor de conteúdo defina a página raiz de navegação junto com a profundidade da navegação. A caixa de diálogo [design](#design-dialog) permite que o autor do modelo defina valores padrão para a raiz e a profundidade de navegação.

## Suporte à estrutura do site localizado {#localized-site-structure}

Geralmente, sites são fornecidos em vários idiomas para diferentes regiões. Normalmente, cada página localizada contém um elemento de navegação que é incluído como parte do modelo da página. O Componente de navegação permite colocá-lo uma vez em um modelo para todas as páginas do site e ele se adaptará automaticamente para as páginas localizadas individuais com base na estrutura do site globalizado.

* Para obter um exemplo de como o recurso de localização do Componente de navegação funciona, consulte [a seção abaixo](#example-localization).
* Para obter um exemplo de como os recursos de localização dos Componentes principais funcionam juntos, consulte a página [Recursos de localização dos Componentes principais](/help/get-started/localization.md).

### Exemplo {#example-localization}

Digamos que seu conteúdo é semelhante a:

```
/content
+-- wknd
   +-- language-masters
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- es
      +-- fr
      \-- it
   +-- us
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      \-- es
   \-- ch
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Para a WKND do site, você provavelmente gostaria de colocar o Componente de navegação em um modelo de página como parte do cabeçalho. Depois de fazer parte do modelo, você pode definir a **Raiz de navegação** do componente para `/content/wknd/language-masters/en`, pois é aí que o conteúdo principal desse site começa. Talvez você também queira definir a **Profundidade da estrutura de navegação** como `2`, pois provavelmente não quer que a árvore de conteúdo inteira seja mostrada pelo componente, mas sim os dois primeiros níveis, de modo que sirva como uma visão geral.

Com o valor **Raiz de Navegação**, o Componente de Navegação sabe que, depois de `/content/wknd/language-masters/en` que a navegação começa e pode gerar opções de navegação ao repetir a estrutura do site em dois níveis abaixo (conforme definido pelo valor **Profundidade da Estrutura de Navegação**).

Independentemente da página localizada que um usuário esteja visualizando, o componente de Navegação pode encontrar a página localizada correspondente, sabendo o local da página atual, trabalhando de volta para a raiz e, em seguida, encaminhando para a página correspondente.

Portanto, se um visitante estiver visualizando `/content/ch/de/experience/arctic-surfing-in-lofoten`, o componente saberá gerar a estrutura de navegação com base em `/content/wknd/language-masters/de`. Da mesma forma que se o visitante estiver visualizando `/content/us/en/experience/arctic-surfing-in-lofoten`, o componente saberá gerar a estrutura de navegação com base em `/content/wknd/language-masters/en`.

## Suporte à estrutura de site de sombra {#shadow-structure}

Às vezes, é necessário criar um menu de navegação para o visitante que seja diferente da estrutura real do site. Talvez uma promoção deva destacar determinado conteúdo no menu, reorganizando a listagem de conteúdo. Usando páginas sombra, que simplesmente redirecionam para outras páginas de conteúdo, o componente de navegação pode gerar qualquer estrutura de navegação arbitrária necessária.

Para fazer isso, é necessário:

1. Crie páginas sombra como páginas vazias que representam a estrutura do site desejado. Geralmente, isso é chamado de estrutura de site de sombra.
1. Defina os valores de **Redirect** nas propriedades da página nessas páginas para apontar para as páginas de conteúdo reais.
1. Defina a opção **Hide in Navigation** nas propriedades da página das páginas sombra.
1. Defina o valor **Raiz de Navegação** do Componente de Navegação para apontar para a raiz da nova estrutura de site de sombra.

O Componente de navegação renderizará o menu com base na estrutura do site de sombra. Os links renderizados pelo componente são para as páginas de conteúdo real para as quais as páginas de sombra redirecionam e não para as próprias páginas de sombra. Além disso, o componente exibe os nomes das páginas reais, bem como destaca a página ativa corretamente, mesmo quando a navegação se baseia em páginas de sombra. O Componente de navegação torna as páginas sombra totalmente transparentes para o visitante.

>[!NOTE]
>As páginas sombra tornam as opções de navegação muito mais flexíveis, mas lembre-se de que a manutenção dessa estrutura é então completamente manual. Se você reorganizar o conteúdo real do site ou adicionar/remover conteúdo, precisará atualizar manualmente a estrutura de sombra, conforme necessário.

>[!NOTE]
>Ao renderizar uma estrutura de site de sombra, somente as páginas de sombra são recursivas pela lógica de navegação. A lógica não repete a estrutura dos destinos de redirecionamento.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de navegação é a v1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de navegação e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_navigation).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de navegação [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_navigation_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

>[!NOTE]
>
>A partir dos Componentes principais versão 2.1.0, o Componente de navegação oferece suporte a [schema.org microdata](https://schema.org).

## Editar caixa de diálogo {#edit-dialog}

Na caixa de diálogo de edição, o autor de conteúdo pode definir a página raiz para navegação e a profundidade da estrutura de navegação.

### Guia Propriedades {#properties-tab}

![Guia de propriedades da caixa de diálogo de edição do Componente de navegação](/help/assets/navigation-edit-properties.png)

* **Raiz de navegação**  - A página raiz, que será usada para gerar a árvore de navegação.
* **Excluir níveis de raiz**  - Geralmente, a raiz não deve ser incluída na navegação. Essa opção permite especificar quantos níveis acima da raiz você deseja excluir. Por exemplo:
   * 0 = mostrar o nível raiz
   * 1 = excluir o nível raiz
   * 2 = excluir a raiz e 1 nível superior
   * etc.
* **Coletar todas as páginas filhas**  - Colete todas as páginas que são descendentes da raiz de navegação.
* **Profundidade da estrutura de navegação**  - Define quantos níveis abaixo da árvore de navegação o componente deve exibir em relação à raiz de navegação (disponível apenas quando  **Coletar todas as** páginas filhas não selecionadas).
* **Desativar sombreamento**  - Se a página na hierarquia for um redirecionamento, o nome da página de redirecionamento será exibido em vez do destino. Consulte o [Suporte à Estrutura de Site de Sombra](#shadow-structure) para obter mais informações.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

### Guia Acessibilidade {#accessibility-tab}

![Guia de acessibilidade da caixa de diálogo do componente de navegação](/help/assets/navigation-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para os rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo**  - Valor de um atributo de rótulo ARIA para o componente

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os valores padrão para a página raiz de navegação e a profundidade de navegação apresentadas aos autores de conteúdo.

### Guia Propriedades {#properties-tab-design}

![Caixa de diálogo de design do componente de navegação](/help/assets/navigation-design.png)

* **Raiz de navegação**  - O valor padrão da página raiz da estrutura de navegação, que será usada para gerar a árvore de navegação e assumirá como padrão quando o autor de conteúdo adicionar o componente à página.
* **Excluir níveis de raiz**  - Geralmente, a raiz não deve ser incluída na navegação. Essa opção permite especificar o padrão de quantos níveis acima da raiz você deseja excluir. Por exemplo:
   * 0 = mostrar o nível raiz
   * 1 = excluir o nível raiz
   * 2 = excluir a raiz e 1 nível superior
   * etc.
* **Coletar todas as páginas filhas**  - O valor padrão da opção para coletar todas as páginas que são descendentes da raiz de navegação.
* **Profundidade da estrutura de navegação**  - o valor padrão da profundidade da estrutura de navegação.
* **Desativar sombreamento**  - O valor padrão de se sombreamento deve ser desativado ao adicionar um componente de navegação

### Guia Estilos {#styles-tab}

O Componente de navegação suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

## Camada de dados do cliente Adobe {#data-layer}

O Componente de Navegação suporta a Camada de Dados do Cliente do Adobe.](/help/developing/data-layer/overview.md)[
