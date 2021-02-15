---
title: Componente de navegação
description: O Componente de navegação permite que os usuários naveguem facilmente em uma estrutura de site globalizada.
translation-type: tm+mt
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 1%

---


# Componente de navegação{#navigation-component}

O Componente de navegação permite que os usuários naveguem facilmente em uma estrutura de site globalizada.

## Uso {#usage}

O componente de navegação lista uma árvore de páginas para que os usuários de um site possam navegar facilmente pela estrutura do site.

O Componente de navegação pode detectar automaticamente a estrutura do site globalizado do site e [adaptar-se automaticamente a uma página localizada.](#localized-site-structure) Além disso, ele pode suportar qualquer estrutura de site arbitrária usando  [páginas de redirecionamento de ](#shadow-structure) sombra para representar outra estrutura que não seja a estrutura de conteúdo principal.

A caixa de diálogo [edit](#edit-dialog) permite que o autor do conteúdo defina a página raiz de navegação junto com a profundidade da navegação. A caixa de diálogo [design](#design-dialog) permite que o autor do modelo defina valores padrão para a raiz e profundidade de navegação.

## Suporte Localizado à Estrutura do Site {#localized-site-structure}

Geralmente, os sites são fornecidos em vários idiomas para diferentes regiões. Normalmente, cada página localizada conterá um elemento de navegação que é incluído como parte do modelo da página. O Componente de navegação permite que você o coloque uma vez em um modelo para todas as páginas do site e ele se adapta automaticamente para as páginas individuais localizadas com base na estrutura do site globalizado.

* Para obter um exemplo de como o recurso de localização do Componente de navegação funciona, consulte [a seção abaixo](#example-localization).
* Para ver um exemplo de como os recursos de localização dos Componentes Principais trabalham juntos, consulte a [página Recursos de Localização dos Componentes Principais](/help/get-started/localization.md).

### Exemplo {#example-localization}

Digamos que seu conteúdo se parece com isso:

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

Para o WKND do site, você provavelmente gostaria de colocar o Componente de navegação em um modelo de página como parte do cabeçalho. Depois de fazer parte do modelo, você pode definir **Raiz de navegação** do componente como `/content/wknd/language-masters/en`, já que é onde seu conteúdo principal começa. Talvez você também queira definir a **Profundidade da estrutura de navegação** como `2`, pois provavelmente não deseja que a árvore de conteúdo inteira seja exibida pelo componente, mas sim os dois primeiros níveis para que ela sirva como uma visão geral.

Com o valor **Raiz de Navegação**, o Componente de Navegação sabe que depois de `/content/wknd/language-masters/en` a navegação começar e pode gerar opções de navegação ao repetir a estrutura do site em dois níveis abaixo (conforme definido pelo valor **Profundidade da Estrutura de Navegação**).

Independentemente da página localizada que um usuário esteja visualizando, o componente de Navegação pode encontrar a página localizada correspondente, sabendo o local da página atual, trabalhando para trás até a raiz e, em seguida, encaminhando para a página correspondente.

Portanto, se um visitante estiver visualizando `/content/ch/de/experience/arctic-surfing-in-lofoten`, o componente saberá que gera a estrutura de navegação com base em `/content/wknd/language-masters/de`. Da mesma forma, se o visitante estiver visualizando `/content/us/en/experience/arctic-surfing-in-lofoten`, o componente saberá que gera a estrutura de navegação com base em `/content/wknd/language-masters/en`.

## Suporte à estrutura do site sombra {#shadow-structure}

Às vezes, é necessário criar um menu de navegação para o visitante que seja diferente da estrutura real do site. Talvez uma promoção deva destacar determinado conteúdo no menu reorganizando a listagem do conteúdo. Usando páginas sombra, que simplesmente redirecionam para outras páginas de conteúdo, o componente de navegação pode gerar qualquer estrutura de navegação arbitrária necessária.

Para fazer isso, você precisará:

1. Crie páginas sombra como páginas vazias que representam a estrutura do site desejado. Isso é frequentemente chamado de uma estrutura de site sombra.
1. Defina os valores de **Redirecionar** nas propriedades da página nessas páginas para apontar para as páginas de conteúdo reais.
1. Defina a opção **Ocultar em Navegação** nas propriedades de página das páginas sombra.
1. Defina o valor **Raiz de navegação** do Componente de navegação para apontar para a raiz da nova estrutura de site sombra.

O Componente de navegação renderizará o menu com base na estrutura do site de sombra. Os links renderizados pelo componente são para as páginas de conteúdo real às quais as páginas de sombra são redirecionadas e não para as próprias páginas de sombra. Além disso, o componente exibe os nomes das páginas reais, bem como realça corretamente a página ativa, mesmo quando a navegação se baseia em páginas sombra. O Componente de navegação torna as páginas sombra totalmente transparentes para o visitante.

>[!NOTE]
>As páginas de sombra tornam suas opções de navegação muito mais flexíveis, mas lembre-se de que a manutenção dessa estrutura é completamente manual. Se você reorganizar o conteúdo real do site ou adicionar/remover conteúdo, precisará atualizar manualmente a estrutura de sombra, conforme necessário.

>[!NOTE]
>Ao renderizar uma estrutura de site de sombra, somente as páginas de sombra são recurtidas pela lógica de navegação. A lógica não recursa a estrutura dos destinos de redirecionamento.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de navegação é a v1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente de navegação e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_navigation).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de navegação [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_navigation_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

>[!NOTE]
>
>Desde a versão 2.1.0 dos Componentes principais, o Componente de navegação oferece suporte a [schema.org microdata](https://schema.org).

## Editar caixa de diálogo {#edit-dialog}

Na caixa de diálogo de edição, o autor do conteúdo pode definir a página raiz para navegação e a profundidade da estrutura de navegação.

### Guia Propriedades {#properties-tab}

![Guia de propriedades da caixa de diálogo de edição do componente de navegação](/help/assets/navigation-edit-properties.png)

* **Raiz**  de navegação - a página raiz, que será usada para gerar a árvore de navegação.
* **Excluir níveis**  raiz - Geralmente, a raiz não deve ser incluída na navegação. Essa opção permite especificar quantos níveis acima da raiz você deseja excluir. Por exemplo:
   * 0 = mostrar o nível raiz
   * 1 = excluir o nível raiz
   * 2 = excluir a raiz e mais 1 nível acima
   * etc.
* **Coletar todas as páginas**  secundárias - Coleta todas as páginas que são descendentes da raiz de navegação.
* **Profundidade**  da estrutura de navegação - Define quantos níveis abaixo da árvore de navegação o componente deve exibir em relação à raiz de navegação (disponível apenas quando  **Coleta todas as** páginas filhas não selecionadas).
* **Desativar sombreamento**  - Se a página na hierarquia for um redirecionamento, o nome da página de redirecionamento será exibido em vez do público alvo. Consulte o [Suporte à estrutura do site sombra](#shadow-structure) para obter mais informações.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [ de ](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

### Guia Acessibilidade {#accessibility-tab}

![Guia de acessibilidade da caixa de diálogo de edição do componente de navegação](/help/assets/navigation-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para os rótulos [ARIA accessibility](https://www.w3.org/WAI/standards-guidelines/aria/) do componente.

* **Rótulo**  - Valor de um atributo de rótulo ARIA para o componente

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os valores padrão para a página raiz de navegação e profundidade de navegação apresentados aos autores do conteúdo.

### Guia Propriedades {#properties-tab-design}

![Caixa de diálogo de design do componente de navegação](/help/assets/navigation-design.png)

* **Raiz**  de navegação - O valor padrão da página raiz da estrutura de navegação, que será usado para gerar a árvore de navegação e assumirá o padrão quando o autor do conteúdo adicionar o componente à página.
* **Excluir níveis**  raiz - Geralmente, a raiz não deve ser incluída na navegação. Essa opção permite especificar o padrão de quantos níveis acima da raiz você deseja excluir. Por exemplo:
   * 0 = mostrar o nível raiz
   * 1 = excluir o nível raiz
   * 2 = excluir a raiz e mais 1 nível acima
   * etc.
* **Coletar todas as páginas** -filho - O valor padrão da opção para coletar todas as páginas que são descendentes da raiz de navegação.
* **Profundidade**  da estrutura de navegação - O valor padrão da profundidade da estrutura de navegação.
* **Desativar sombreamento**  - O valor padrão de se o sombreamento deve ser desativado ao adicionar um componente de navegação

### Guia Estilos {#styles-tab}

O componente de navegação suporta o AEM [Sistema de estilo](/help/get-started/authoring.md#component-styling).

## Camada de Dados do Cliente Adobe {#data-layer}

O Componente de Navegação suporta a [Camada de Dados do Cliente Adobe.](/help/developing/data-layer/overview.md)
