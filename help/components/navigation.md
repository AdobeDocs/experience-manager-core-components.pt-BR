---
title: Componente de Navegação
description: O componente de Navegação permite que os usuários naveguem facilmente em uma estrutura de site globalizada.
role: Architect, Developer, Admin, User
exl-id: 9154f2a3-3d1e-4865-a413-298748fa66d3
source-git-commit: 395a1669cf3e17f649c23852addc37316b923bfd
workflow-type: ht
source-wordcount: '1544'
ht-degree: 100%

---

# Componente de Navegação{#navigation-component}

O componente de Navegação permite que os usuários naveguem facilmente em uma estrutura de site globalizada.

## Uso {#usage}

O componente de Navegação lista uma árvore de páginas para que os usuários de um site possam navegar facilmente pela estrutura do site.

O componente de Navegação pode detectar automaticamente a estrutura globalizada do site e [adaptar-se automaticamente a uma página localizada.](#localized-site-structure) Além disso, ele pode suportar qualquer estrutura de site arbitrária usando [páginas de redirecionamento de sombra](#shadow-structure) para representar outra estrutura diferente da estrutura de conteúdo principal.

A [caixa de diálogo de edição](#edit-dialog) permite que o autor do conteúdo defina a página raiz de navegação junto com a profundidade da navegação. A [caixa de diálogo de design](#design-dialog) permite que o autor do modelo defina valores padrão para a raiz e a profundidade de navegação.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de navegação é a v2, introduzida com a versão 2.18.0 dos componentes principais em fevereiro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | - | Compatível | Compatível |
| [v1](v1/navigation.md) | Compatível | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Suporte localizado à estrutura do site {#localized-site-structure}

Geralmente, os sites são fornecidos em vários idiomas para diferentes regiões. Normalmente, cada página localizada contém um elemento de navegação que é incluído como parte do modelo da página. O componente de Navegação permite colocá-lo uma vez em um modelo para todas as páginas do site e ele se adaptará automaticamente às páginas localizadas individuais com base na estrutura do site globalizado.

* Para obter um exemplo de como o recurso de localização do componente de Navegação funciona, consulte [a seção abaixo](#example-localization).
* Para obter um exemplo de como os recursos de localização dos Componentes principais funcionam juntos, consulte a [página Recursos de localização dos Componentes principais](/help/get-started/localization.md).

### Exemplo {#example-localization}

Digamos que seu conteúdo seja mais ou menos assim:

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

Para o site da WKND, você provavelmente colocaria o componente de Navegação em um modelo de página como parte do cabeçalho. Depois de fazer parte do modelo, você pode definir a **Raiz de navegação** do componente para `/content/wknd/language-masters/en`, pois é onde o conteúdo principal desse site começa. Talvez você também queira definir a **Profundidade da estrutura de navegação** como `2`, pois não vai querer que a árvore de conteúdo inteira seja mostrada pelo componente, mas sim os dois primeiros níveis, de modo que sirva como uma visão geral.

Com o valor **Raiz de Navegação**, o componente de Navegação sabe que depois de `/content/wknd/language-masters/en`, a navegação começa e pode gerar opções de navegação ao repetir a estrutura do site em dois níveis abaixo (conforme definido pelo valor **Profundidade da estrutura de navegação**).

Independentemente da página localizada que um usuário esteja visualizando, o componente de Navegação pode encontrar a página localizada correspondente, conhecendo o local da página atual, trabalhando de trás para frente até a raiz e, em depois, para frente, até a página correspondente.

Portanto, se um visitante estiver visualizando `/content/ch/de/experience/arctic-surfing-in-lofoten`, o componente saberá gerar a estrutura de navegação com base em `/content/wknd/language-masters/de`. Da mesma forma que se o visitante estiver visualizando `/content/us/en/experience/arctic-surfing-in-lofoten`, o componente saberá gerar a estrutura de navegação com base em `/content/wknd/language-masters/en`.

## Suporte à estrutura de shadow sites {#shadow-structure}

Às vezes, é necessário criar um menu de navegação para o visitante que seja diferente da estrutura real do site. Talvez uma promoção deva destacar determinado conteúdo no menu, reorganizando a listagem de conteúdo. Usando páginas sombra, que simplesmente redirecionam para outras páginas de conteúdo, o componente de navegação pode gerar qualquer estrutura de navegação arbitrária necessária.

Para fazer isso, é necessário:

1. criar páginas sombra como páginas vazias que representam a estrutura do site desejado. Geralmente, isso é chamado de estrutura de shadow site.
1. definir os valores de **Redirecionamento** nas propriedades da página para apontar para as páginas de conteúdo reais.
1. definir a opção **Ocultar na navegação** nas propriedades da página das páginas sombra.
1. Defina o valor **Raiz de Navegação** do componente de Navegação para apontar para a raiz da nova estrutura de shadow site.

O componente de Navegação renderizará o menu com base na estrutura do shadow site. Os links renderizados pelo componente são para as páginas de conteúdo real para as quais as páginas sombra redirecionam e não para as próprias páginas sombra. Além disso, o componente exibe os nomes das páginas reais, e destaca corretamente a página ativa, mesmo quando a navegação se baseia em páginas sombra. O componente de Navegação torna as páginas sombra totalmente transparentes para o visitante.

>[!NOTE]
>As páginas sombra tornam as opções de navegação muito mais flexíveis, mas lembre-se de que depois a manutenção dessa estrutura é completamente manual. Se você reorganizar o conteúdo real do site ou adicionar/remover conteúdo, precisará atualizar manualmente a estrutura de sombra, conforme necessário.

>[!NOTE]
>Ao renderizar uma estrutura de shadow site, somente as páginas sombra são recursivas pela lógica de navegação. A lógica não repete a estrutura dos destinos de redirecionamento.

## Redirecionamentos na navegação {#redirects}

Quando uma página tem um destino de redirecionamento (independentemente de estar apontando para um URL externo ou para outra página do AEM), um componente de navegação que contém links para aquele aponta diretamente para o URL do destino de redirecionamento.

### Exemplo {#redirect-example}

* Crie uma página A que redirecione para a página B.
* Crie uma página C que redireciona para `https://aemcomponents.dev`
* Em uma página D, insira um componente de navegação ou que contenha as páginas A e C
* Os respectivos links que são gerados, apontam diretamente para a página B e `https://aemcomponents.dev`

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Navegação, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_navigation_br).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Navegação [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_navigation_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

>[!NOTE]
>
>A partir dos Componentes principais versão 2.1.0, o componente de Navegação é compatível com os [microdados schema.org](https://schema.org).

## Caixa de diálogo de edição {#edit-dialog}

Na caixa de diálogo de edição, o autor de conteúdo pode definir a página raiz para navegação e a profundidade da estrutura de navegação.

### Guia Propriedades {#properties-tab}

![Guia Propriedades da caixa de diálogo de edição do componente de Navegação](/help/assets/navigation-edit-properties.png)

* **Raiz de navegação** - A página raiz, que será usada para gerar a árvore de navegação.
* **Excluir níveis de raiz** - Geralmente, a raiz não deve ser incluída na navegação. Essa opção permite especificar quantos níveis acima da raiz você deseja excluir. Por exemplo:
   * 0 = mostrar o nível raiz
   * 1 = excluir o nível raiz
   * 2 = excluir a raiz e 1 nível superior
   * etc.
* **Coletar todas as páginas secundárias** - Coleta todas as páginas descendentes da raiz de navegação.
* **Profundidade da estrutura de navegação** - Define quantos níveis abaixo da árvore de navegação o componente deve exibir em relação à raiz de navegação (disponível apenas quando **Coletar todas as páginas secundárias** não estiver selecionada).
* **Desativar sombreamento** - Se a página na hierarquia for um redirecionamento, o nome da página de redirecionamento será exibido em vez do destino. Consulte o [Suporte à estrutura de shadow site](#shadow-structure) para mais informações.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Guia Acessibilidade {#accessibility-tab}

![Guia Acessibilidade da caixa de diálogo de edição do componente de Navegação](/help/assets/navigation-edit-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

### Guia Estilos {#styles-tab-edit}

O componente de navegação é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que o menu suspenso fique disponível.

![Guia Estilos da caixa de diálogo de edição do componente de navegação](/help/assets/navigation-edit-styles.png)

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os valores padrão para a página raiz de navegação e a profundidade de navegação apresentadas aos autores de conteúdo.

### Guia Propriedades {#properties-tab-design}

![Caixa de diálogo de design do componente de Navegação](/help/assets/navigation-design.png)

* **Raiz de navegação** - O valor padrão da página raiz da estrutura de navegação, que será usada para gerar a árvore de navegação e assumirá como padrão quando o autor de conteúdo adicionar o componente à página.
* **Excluir níveis de raiz** - Geralmente, a raiz não deve ser incluída na navegação. Essa opção permite especificar o padrão de quantos níveis acima da raiz você deseja excluir. Por exemplo:
   * 0 = mostrar o nível raiz
   * 1 = excluir o nível raiz
   * 2 = excluir a raiz e 1 nível superior
   * etc.
* **Coletar todas as páginas secundárias** - O valor padrão da opção para coletar todas as páginas que sejam descendentes da raiz de navegação.
* **Profundidade da estrutura de navegação** - o valor padrão da profundidade da estrutura de navegação.
* **Desativar sombreamento** - O valor padrão caso o sombreamento deva ser desativado ao adicionar um componente de navegação

### Guia Estilos {#styles-tab}

O componente de Navegação é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Navegação é compatível com a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
